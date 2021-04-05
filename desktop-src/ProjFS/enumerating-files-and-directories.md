---
title: Enumerazione di file e directory
description: Viene descritto il modo in cui un provider ProjFS partecipa all'enumerazione di directory.
ms.assetid: <GUID-GOES-HERE>
ms.date: 09/25/2018
ms.topic: article
ms.openlocfilehash: e0712ceb927388b090a84a89f80f0e2d3a1befbb
ms.sourcegitcommit: 80d74c0bf4fc402865a1ad223480abe1ce4d1115
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2020
ms.locfileid: "103723991"
---
# <a name="enumerating-files-and-directories"></a>Enumerazione di file e directory

Quando un provider crea innanzitutto una radice di virtualizzazione, è vuota nel sistema locale.  Ovvero, nessuno degli elementi nell'archivio dati di supporto è ancora stato memorizzato nella cache su disco.  Poiché ogni elemento viene aperto, viene memorizzato nella cache, ma fino a quando non viene aperto un elemento esiste solo nell'archivio dati di supporto.

Poiché gli elementi non aperti non hanno una presenza locale, l'enumerazione di directory normale non rivelerà l'esistenza dell'utente.  Pertanto, il provider deve partecipare all'enumerazione di directory restituendo le informazioni a ProjFS sugli elementi nell'archivio dati di supporto.  ProjFS unisce le informazioni del provider con le informazioni sul file system locale per presentare all'utente un elenco unificato del contenuto di una directory.

## <a name="directory-enumeration-callbacks"></a>Callback di enumerazione directory

Per partecipare all'enumerazione di directory, il provider deve implementare i callback **[PRJ_START_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_start_directory_enumeration_cb)**, **[PRJ_GET_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_get_directory_enumeration_cb)** e **[PRJ_END_DIRECTORY_ENUMERATION_CB](/windows/win32/api/projectedfslib/nc-projectedfslib-prj_end_directory_enumeration_cb)** .  Quando viene enumerata una directory sotto la radice di virtualizzazione del provider, ProjFS esegue le azioni seguenti:

1. ProjFS chiama il callback **PRJ_START_DIRECTORY_ENUMERATION_CB** del provider per avviare una sessione di enumerazione.

    Come parte dell'elaborazione di questo callback, il provider deve prepararsi a eseguire l'enumerazione.  Ad esempio, deve allocare la memoria necessaria per tenere traccia dello stato di avanzamento dell'enumerazione nell'archivio dati di supporto.

    ProjFS identifica la directory enumerata nel membro **FilePathName** del parametro _callBackData_ del callback.  Viene specificato come percorso relativo alla radice di virtualizzazione.  Se ad esempio la radice di virtualizzazione si trova in `C:\virtRoot` e la directory enumerata è `C:\virtRoot\dir1\dir2` , il membro **FilePathName** conterrà `dir1\dir2` .  Il provider si prepara a enumerare il percorso nell'archivio dati di supporto.  A seconda delle funzionalità dell'archivio di backup di un provider, può essere utile eseguire l'enumerazione dell'archivio di backup nel callback **PRJ_START_DIRECTORY_ENUMERATION_CB** .

    Poiché più enumerazioni possono essere eseguite in parallelo nella stessa directory, ogni callback di enumerazione ha un argomento _enumerationId_ per consentire al provider di associare le chiamate di callback in una singola sessione di enumerazione.

    Se il provider restituisce S_OK dal callback **PRJ_START_DIRECTORY_ENUMERATION_CB** , deve gestire tutte le informazioni sulla sessione di enumerazione che possiede fino a quando ProjFS richiama il callback **PRJ_END_DIRECTORY_ENUMERATION_CB** con lo stesso valore per _enumerationId_.  Se il provider restituisce un errore da **PRJ_START_DIRECTORY_ENUMERATION_CB**, ProjFS non richiama il callback **PRJ_END_DIRECTORY_ENUMERATION_CB** per tale _enumerationId_.

1. ProjFS chiama il callback **PRJ_GET_DIRECTORY_ENUMERATION_CB** del provider una o più volte per ottenere il contenuto della directory dal provider.

    In risposta a questo callback, il provider restituisce un elenco ordinato di elementi dall'archivio dati di supporto.

    Il callback può fornire un'espressione di ricerca nel parametro _searchExpression_ che il provider USA per definire l'ambito dei risultati dell'enumerazione.  Se _searchExpression_ è null, il provider restituisce tutte le voci della directory enumerata.  Se è diverso da NULL, il provider può utilizzare **[PrjDoesNameContainWildCards](/windows/win32/api/projectedfslib/nf-projectedfslib-prjdoesnamecontainwildcards)** per determinare se sono presenti caratteri jolly nell'espressione.  In tal caso, il provider utilizza **[PrjFileNameMatch](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamematch)** per determinare se una voce nella directory corrisponde all'espressione di ricerca.

    Il provider deve acquisire il valore di _searchExpression_ alla prima chiamata di questo callback.  Usa il valore acquisito per qualsiasi chiamata successiva del callback nella stessa sessione di enumerazione, a meno che PRJ_CB_DATA_FLAG_ENUM_RESTART_SCAN non sia impostato nel campo dei **flag** del parametro _callBackData_ del callback.  In tal caso, è necessario riacquisire il valore di _searchExpression_.

    Se non sono presenti voci corrispondenti nell'archivio di backup, il provider restituisce semplicemente S_OK dal callback.  In caso contrario, il provider formatta ogni voce corrispondente dal relativo archivio di backup in una struttura **[PRJ_FILE_BASIC_INFO](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info)** , quindi utilizza **[PrjFillDirEntryBuffer](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer)** per riempire il buffer fornito dal parametro _dirEntryBufferHandle_ del callback.  Il provider continua ad aggiungere voci fino a quando non vengono aggiunte tutte o fino a quando **PrjFillDirEntryBuffer** non restituisce HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER).  Il provider restituisce quindi S_OK dal callback.  Si noti che il provider deve aggiungere le voci al buffer _dirEntryBufferHandle_ nell'ordinamento corretto.  Il provider deve usare **[PrjFileNameCompare](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilenamecompare)** per determinare il tipo di ordinamento corretto.

    > Il provider deve fornire un valore per il membro della **directory** di **PRJ_FILE_BASIC_INFO**.  Se la **directory** è false, il provider deve fornire anche un valore per il membro **Filesize** .
    >
    > Se il provider non fornisce valori per i membri **creationTime**, **LastAccessTime**, **LastWriteTime** e **ChangeTime** , ProjFS utilizzerà l'ora di sistema corrente.
    >
    > ProjFS utilizzerà qualsiasi FILE_ATTRIBUTE flag che il provider imposta nel membro **FileAttributes** ad eccezione di FILE_ATTRIBUTE_DIRECTORY; il valore corretto per FILE_ATTRIBUTE_DIRECTORY nel membro **FileAttributes** verrà impostato in base al valore fornito del membro di **directory** .

    Se **PrjFillDirEntryBuffer** restituisce HRESULT_FROM_WIN32 (ERROR_INSUFFICIENT_BUFFER) prima che il provider esaurisca le voci da aggiungere, il provider deve tenere traccia della voce che stava tentando di aggiungere quando ha ricevuto l'errore.  La volta successiva che ProjFS chiama il callback **PRJ_GET_DIRECTORY_ENUMERATION_CB** per la stessa sessione di enumerazione, il provider deve riprendere l'aggiunta di voci al buffer _dirEntryBufferHandle_ con la voce che stava tentando di aggiungere.

    > Se l'archivio di backup supporta i collegamenti simbolici, il provider deve usare **[PrjFillDirEntryBuffer2](/windows/win32/api/projectedfslib/nf-projectedfslib-prjfilldirentrybuffer2)** per riempire il buffer fornito dal parametro _dirEntryBufferHandle_ del callback.  **PrjFillDirEntryBuffer2** supporta un input del buffer aggiuntivo che consente al provider di specificare che la voce di enumerazione è un collegamento simbolico e la relativa destinazione.  In caso contrario, si comporta come descritto in precedenza per **PrjFillDirEntryBuffer**.  Nell'esempio seguente viene usato **PrjFillDirEntryBuffer2** per illustrare il supporto dei collegamenti simbolici.
    >
    > Si noti che **PrjFillDirEntryBuffer2** è supportato a partire da Windows 10, versione 2004.  Un provider deve verificare l'esistenza di **PrjFillDirEntryBuffer2**, ad esempio usando **[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)**.

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

1. ProjFS chiama il callback **PRJ_END_DIRECTORY_ENUMERATION_CB** del provider per terminare la sessione di enumerazione.

    Il provider deve eseguire tutte le operazioni di pulizia necessarie per terminare la sessione di enumerazione, ad esempio deallocare la memoria allocata come parte dell'elaborazione **PRJ_START_DIRECTORY_ENUMERATION_CB**.
