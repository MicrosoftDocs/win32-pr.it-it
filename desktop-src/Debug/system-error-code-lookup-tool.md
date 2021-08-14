---
description: Descrive come usare lo strumento Di ricerca errori Microsoft per trovare spiegazioni testuali dei codici di errore esadecimali in Windows.
title: Strumento Di ricerca errori Microsoft
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: 534b2af92b8dc0e906bd033e8ce1f0fbd08ead0cda21406d1818a318356db613
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118405891"
---
# <a name="the-microsoft-error-lookup-tool"></a>Strumento Di ricerca errori Microsoft

Microsoft Error Lookup Tool visualizza il testo del messaggio associato a un codice di stato esadecimale (o a un altro codice). Questo testo è definito in vari file di intestazione del codice sorgente Microsoft, ad esempio Winerror.h, Setupapi.h e così via.

Lo strumento è firmato digitalmente da Microsoft. Di seguito sono riportate le informazioni SHA256 per il download del file:  

|Algoritmo |Hash |
| --- | --- |
|SHA256 |88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A |

> [!NOTE]
> Gli ambienti aziendali possono limitare i file che possono essere eseguiti e da dove. Prima di scaricare ed eseguire questo strumento, controllare i dettagli seguenti:
> - È necessario disporre dell'autorizzazione o di un'eccezione di sicurezza per scaricare o eseguire lo strumento?
> - È possibile archiviare ed eseguire questo strumento nel computer (ad esempio, nella cartella Documenti)? Oppure è necessario archiviare ed eseguire lo strumento in un computer specializzato, ad esempio un computer file server?

## <a name="usage"></a>Utilizzo

1. Scaricare lo strumento selezionando [questo collegamento.](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe)
1. Se non è stato specificato un percorso nel passaggio 1, passare alla cartella di download e copiare o spostare il file scaricato (Err_6.4.5.exe) nella cartella in cui si archivierà lo strumento. Non è necessario espandere o installare il file.
   > [!NOTE]
   > Se si copia o si sposta il file in una cartella elencata nella variabile di ambiente **Path** del sistema operativo, funzionerà in qualsiasi prompt dei comandi.

1. Aprire una finestra del prompt dei comandi. Se necessario, modificare la directory nel percorso dello strumento Di ricerca errori.
1. Eseguire il comando seguente:
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > In questo comando rappresenta il codice esadecimale \<*error code*> che si vuole cercare.

## <a name="examples"></a>Esempio

```cmd
C:\Tools>Err_6.4.5.exe c000021a
# for hex 0xc000021a / decimal -1073741286
 STATUS_SYSTEM_PROCESS_TERMINATED                ntstatus.h
# {Fatal System Error}
# The %hs system process terminated unexpectedly with a
# status of 0x%08x (0x%08x 0x%08x).
# The system has been shut down.
# as an HRESULT: Severity: FAILURE (1), FACILITY_NULL (0x0), Code 0x21a
# for hex 0x21a / decimal 538
 ERROR_ABIOS_ERROR                               winerror.h
# An error occurred in the ABIOS subsystem.
# 2 matches found for "c000021a"
```

```cmd
C:\Tools>Err_6.4.5.exe 7b
# for hex 0x7b / decimal 123
 INACCESSIBLE_BOOT_DEVICE                       bugcodes.h
 NMERR_SECURITY_BREACH_CAPTURE_DELETED              netmon.h
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# as an HRESULT: Severity: SUCCESS (0), FACILITY_NULL (0x0), Code 0x7b
# for hex 0x7b / decimal 123
 ERROR_INVALID_NAME                       winerror.h
# The filename, directory name, or volume label syntax is
# incorrect.
# 4 matches found for "7b"
```

## <a name="more-information"></a>Altre informazioni

Tenere presente che si tratta di uno strumento "tempormente". Lo strumento Di ricerca errori Microsoft decodifica la maggior parte dei codici di errore Microsoft alla data in cui è stato compilato lo strumento. Poiché le nuove versioni Windows aggiungere nuovi codici di evento e di errore, potrebbe essere necessario scaricare una nuova versione dello strumento Di ricerca errori. Controllare l'Area download Microsoft per una nuova versione oppure vedere [Codici di errore](system-error-codes.md).
