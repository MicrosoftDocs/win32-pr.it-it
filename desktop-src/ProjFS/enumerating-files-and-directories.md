---
title: Enumerazione di file e directory
description: Viene descritto il modo in cui un provider ProjFS partecipa all'enumerazione delle directory.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: 606b379e206cdbc64726e0ea97aed34e00f5253ecbffb7f8b7d42469b0cbb5fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792814"
---
# <a name="enumerating-files-and-directories"></a>Enumerazione di file e directory

Quando un provider crea per la prima volta una radice di virtualizzazione è vuota nel sistema locale.  Ciò significa che nessuno degli elementi nell'archivio dati di backup è ancora stato memorizzato nella cache su disco.  Ogni elemento aperto viene memorizzato nella cache, ma finché non viene aperto esiste solo nell'archivio dati di backup.

Poiché gli elementi non ancorati non hanno una presenza locale, la normale enumerazione della directory non rivela la propria esistenza all'utente.  Il provider deve quindi partecipare all'enumerazione delle directory tramite la restituzione a ProjFS delle informazioni sugli elementi nel relativo archivio dati di backup.  ProjFS unisce le informazioni del provider con ciò che si trova nel file system locale per presentare all'utente un elenco unificato del contenuto di una directory.

## <a name="directory-enumeration-callbacks"></a>Callback di enumerazione della directory

Per partecipare all'enumerazione di directory, il provider deve **[implementare](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)** PRJ_START_DIRECTORY_ENUMERATION_CB , **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** e **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** callback.  Quando viene enumerata una directory nella radice di virtualizzazione del provider, ProjFS esegue le azioni seguenti:

1. ProjFS chiama il callback PRJ_START_DIRECTORY_ENUMERATION_CB **provider** per avviare una sessione di enumerazione.

    Nell'ambito dell'elaborazione di questo callback, il provider deve preparare l'esecuzione dell'enumerazione .  Ad esempio, deve allocare la memoria necessaria per tenere traccia dello stato di avanzamento dell'enumerazione nell'archivio dati di backup.

    ProjFS identifica la directory enumerata nel **membro FilePathName** del parametro _callbackData del_ callback.  Viene specificato come percorso relativo alla radice di virtualizzazione.  Ad esempio, se la radice di virtualizzazione si trova in e la directory enumerata è , il `C:\virtRoot` `C:\virtRoot\dir1\dir2` membro **FilePathName** conterrà `dir1\dir2` .  Il provider si prepara a enumerare il percorso nell'archivio dati di backup.  A seconda delle funzionalità dell'archivio di backup di un provider, può essere opportuno eseguire l'enumerazione dell'archivio di backup nel callback **PRJ_START_DIRECTORY_ENUMERATION_CB** di backup.

    Poiché più enumerazioni possono verificarsi in parallelo nella stessa directory, ogni callback di enumerazione ha un argomento _enumerationId_ per consentire al provider di associare le chiamate di callback in una singola sessione di enumerazione.

    Se il provider restituisce S_OK dal callback **PRJ_START_DIRECTORY_ENUMERATION_CB,** deve mantenere le informazioni sulla sessione di enumerazione che contiene fino a quando ProjFS non richiama il callback **PRJ_END_DIRECTORY_ENUMERATION_CB** con lo stesso valore per _enumerationId_.  Se il provider restituisce un errore da **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS non richiama il **callback** PRJ_END_DIRECTORY_ENUMERATION_CB per tale _enumerationId_.

1. ProjFS chiama il callback **PRJ_GET_DIRECTORY_ENUMERATION_CB** del provider una o più volte per ottenere il contenuto della directory dal provider.

    In risposta a questo callback, il provider restituisce un elenco ordinato di elementi dal relativo archivio dati di backup.

    Il callback può fornire un'espressione di ricerca nel _parametro searchExpression_ che il provider usa per l'ambito dei risultati dell'enumerazione.  Se _searchExpression_ è NULL, il provider restituisce tutte le voci nella directory enumerata.  Se non è NULL, il provider può usare **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** per determinare se sono presenti caratteri jolly nell'espressione.  In caso contrario, il provider usa **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** per determinare se una voce nella directory corrisponde all'espressione di ricerca.

    Il provider deve acquisire il valore di _searchExpression_ alla prima chiamata di questo callback.  Usa il valore acquisito in qualsiasi chiamata successiva del callback nella stessa sessione di enumerazione, a meno che PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN non sia impostato nel campo **Flags** del parametro _callbackData del_ callback.  In tal caso, deve ricavare il valore di _searchExpression_.

    Se non sono presenti voci corrispondenti nell'archivio di backup, il provider restituisce semplicemente S_OK dal callback.  In caso contrario, il provider formatta ogni voce corrispondente dall'archivio di backup in una **[struttura PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** e quindi usa **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** per riempire il buffer fornito dal parametro _dirEntryBufferHandle_ del callback.  Il provider continua ad aggiungere voci finché non le aggiunge tutte o finché **PrjFillDirEntryBuffer** non restituisce HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER).  Il provider restituisce quindi S_OK dal callback.  Si noti che il provider deve aggiungere le voci al buffer _dirEntryBufferHandle_ nell'ordinamento corretto.  Il provider deve usare **[PrjFileNameCompare per](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** determinare l'ordinamento corretto.

    > Il provider deve fornire un valore per il **membro IsDirectory** di **PRJ_FILE_BASIC_INFO**.  Se **IsDirectory** è FALSE, il provider deve fornire anche un valore per il **membro FileSize.**
    >
    > Se il provider non fornisce valori per i **membri CreationTime**, **LastAccessTime**, **LastWriteTime** e **ChangeTime** , ProjFS userà l'ora di sistema corrente.
    >
    > ProjFS userà qualsiasi FILE_ATTRIBUTE contrassegna i set di provider nel **membro FileAttributes** ad eccezione di FILE_ATTRIBUTE_DIRECTORY; Verrà impostato il valore corretto per FILE_ATTRIBUTE_DIRECTORY nel membro **FileAttributes** in base al valore fornito del membro **IsDirectory.**

    Se **PrjFillDirEntryBuffer** restituisce HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER) prima che il provider esaurisca le voci da aggiungere, il provider deve tenere traccia della voce che stava tentando di aggiungere quando ha ricevuto l'errore.  La volta successiva che ProjFS chiama il callback **PRJ_GET_DIRECTORY_ENUMERATION_CB** per la stessa sessione di enumerazione, il provider deve riprendere l'aggiunta di voci al buffer _dirEntryBufferHandle_ con la voce che stava tentando di aggiungere.

    > Se l'archivio di backup supporta collegamenti simbolici, il provider deve usare **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** per riempire il buffer fornito dal parametro _dirEntryBufferHandle del_ callback.  **PrjFillDirEntryBuffer2** supporta un input del buffer aggiuntivo che consente al provider di specificare che la voce di enumerazione è un collegamento simbolico e qual è la destinazione.  In caso contrario, si comporta come descritto in precedenza **per PrjFillDirEntryBuffer.**  L'esempio seguente usa **PrjFillDirEntryBuffer2** per illustrare il supporto per i collegamenti simbolici.
    >
    > Si noti **che PrjFillDirEntryBuffer2** è supportato a Windows 10 versione 2004.  Un provider deve cercare l'esistenza di **PrjFillDirEntryBuffer2,** ad esempio usando **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

    ```C++
    typedef struct MY_ENUM_ENTRY MY_ENUM_ENTRY;

    typedef struct MY_ENUM_ENTRY {
        MY_ENUM_ENTRY* Next;
        PWSTR Name;
        BOOLEAN IsDirectory;
        INT64 FileSize;
        BOOLEAN IsSymlink;
        PWSTR SymlinkTarget;
    } MY_ENUM_ENTRY;

    typedef struct MY_ENUM_SESSION {
        GUID EnumerationId;
        PWSTR SearchExpression;
        USHORT SearchExpressionMaxLen;
        BOOLEAN SearchExpressionCaptured;
        MY_ENUM_ENTRY* EnumHead;
        MY_ENUM_ENTRY* LastEnumEntry;
        BOOLEAN EnumCompleted;
    } MY_ENUM_SESSION;

    HRESULT
    MyGetEnumCallback(
        _In_ const PRJ_CALLBACK_DATA* callbackData,
        _In_ const GUID* enumerationId,
        _In_opt_z_ PCWSTR searchExpression,
        _In_ PRJ_DIR_ENTRY_BUFFER_HANDLE dirEntryBufferHandle
        )
    {
        // MyGetEnumSession is a routine the provider might implement to find
        // information about the enumeration session that it first stored
        // when processing its PRJ_START_DIRECTORY_ENUMERATION_CB callback.
        //
        // In this example the PRJ_START_DIRECTORY_ENUMERATION_CB callback has
        // already retrieved a list of the items in the backing store located at
        // callbackData->FilePathName, sorted them using PrjFileNameCompare()
        // to determine collation order, and stored the list in session->EnumHead.
        MY_ENUM_SESSION* session = NULL;
        session = MyGetEnumSession(enumerationId);

        if (session == NULL)
        {
            return HRESULT_FROM_WIN32(ERROR_INVALID_PARAMETER);
        }

        if (!session->SearchExpressionCaptured ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            if (searchExpression != NULL)
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              searchExpression,
                              wcslen(searchExpression)))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            else
            {
                if (wcsncpy_s(session->SearchExpression,
                              session->SearchExpressionMaxLen,
                              "*",
                              1))
                {
                    // Failed to copy the search expression; perhaps the provider
                    // could try reallocating session->SearchExpression.
                }
            }
            session->SearchExpressionCaptured = TRUE;
        }

        MY_ENUM_ENTRY* enumHead = NULL;

        // We have to start the enumeration from the beginning if we aren't
        // continuing an existing session or if the caller is requesting a restart.
        if (((session->LastEnumEntry == NULL) &&
             !session->EnumCompleted) ||
            (callbackData->Flags & PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN))
        {
            // Ensure that if the caller is requesting a restart we reset our
            // bookmark of how far we got in the enumeration.
            session->LastEnumEntry = NULL;

            // In case we're restarting ensure we don't think we're done.
            session->EnumCompleted = FALSE;

            // We need to start considering items from the beginning of the list
            // retrieved from the backing store.
            enumHead = session->EnumHead;
        }
        else
        {
            // We are resuming an existing enumeration session.  Note that
            // session->LastEnumEntry may be NULL.  That is okay; it means
            // we got all the entries the last time this callback was invoked.
            // Returning S_OK without adding any new entries to the
            // dirEntryBufferHandle buffer signals ProjFS that the enumeration
            // has returned everything it can.
            enumHead = session->LastEnumEntry;
        }

        if (enumHead == NULL)
        {
            // There are no items to return.  Remember that we've returned everything
            // we can.
            session->EnumCompleted = TRUE;
        }
        else
        {
            MY_ENUM_ENTRY* thisEntry = enumHead;
            while (thisEntry != NULL)
            {
                // We'll insert the entry into the return buffer if it matches
                // the search expression captured for this enumeration session.
                if (PrjFileNameMatch(thisEntry->Name, session->SearchExpression))
                {
                    PRJ_FILE_BASIC_INFO fileBasicInfo = {};
                    fileBasicInfo.IsDirectory = thisEntry->IsDirectory;
                    fileBasicInfo.FileSize = thisEntry->FileSize;

                    // If our backing store says this is really a symbolic link,
                    // set up to tell ProjFS that it is a symlink and what its
                    // target is.
                    PRJ_EXTENDED_INFO extraInfo = {};
                    if (thisEntry->IsSymlink)
                    {
                        extraInfo.InfoType = PRJ_EXT_INFO_SYMLINK;
                        extraInfo.Symlink.TargetName = thisEntry->SymlinkTarget;
                    }

                    // Format the entry for return to ProjFS.
                    HRESULT fillResult = PrjFillDirEntryBuffer2(dirEntryBufferHandle,
                                                                thisEntry->Name,
                                                                &fileBasicInfo,
                                                                thisEntry->IsSymlink ? &extraInfo : NULL);

                    if (fillResult == HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER))
                    {
                        // We couldn't add this entry to the buffer; remember where we left
                        // off for the next time we're called for this enumeration session.
                        session->LastEnumEntry = thisEntry;
                        return S_OK;
                    }
                }

                thisEntry = thisEntry->Next;
            }

            // We reached the end of the list of entries; remember that we've returned
            // everything we can.
            session->EnumCompleted = TRUE;
        }

        return S_OK;
    }
    ```

1. ProjFS chiama il callback PRJ_END_DIRECTORY_ENUMERATION_CB **provider** per terminare la sessione di enumerazione.

    Il provider deve eseguire qualsiasi operazione di pulizia per terminare la sessione di **enumerazione,** ad esempio deallocare la memoria allocata durante l'elaborazione PRJ_START_DIRECTORY_ENUMERATION_CB .
