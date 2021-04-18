---
description: Viene descritto come utilizzare lo strumento ricerca errori Microsoft per trovare le spiegazioni del testo dei codici errore esadecimali in Windows.
title: Strumento ricerca errori Microsoft
ms.topic: article
ms.date: 12/4/2019
ms.openlocfilehash: e39b5623458fc176f5ecc81eae71212ba279945c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304659"
---
# <a name="the-microsoft-error-lookup-tool"></a>Strumento ricerca errori Microsoft

Lo strumento ricerca errori Microsoft Visualizza il testo del messaggio associato a un codice di stato esadecimale (o altro codice). Questo testo è definito in diversi file di intestazione del codice sorgente Microsoft, ad esempio Winerror. h, Setupapi. h e così via.

Lo strumento è firmato digitalmente da Microsoft. Di seguito sono riportate le informazioni di SHA256 per il download del file:  

|Algoritmo |Hash |
| --- | --- |
|SHA256 |88739EC82BA16A0B4A3C83C1DD2FCA6336AD8E2A1E5F1238C085B1E86AB8834A |

> [!NOTE]
> Gli ambienti aziendali possono limitare i file che possono essere eseguiti e da dove. Prima di scaricare ed eseguire lo strumento, verificare i seguenti dettagli:
> - È necessario disporre dell'autorizzazione o di un'eccezione di sicurezza per scaricare o eseguire lo strumento?
> - È possibile archiviare ed eseguire lo strumento nel computer (ad esempio, nella cartella documenti)? In alternativa, è necessario archiviare ed eseguire lo strumento in un computer specializzato, ad esempio un file server centrale?

## <a name="usage"></a>Utilizzo

1. Scaricare lo strumento selezionando [questo collegamento](https://download.microsoft.com/download/4/3/2/432140e8-fb6c-4145-8192-25242838c542/Err_6.4.5/Err_6.4.5.exe).
1. Se non è stato specificato un percorso nel passaggio 1, passare alla cartella di download e copiare o spostare il file scaricato (Err_6.4.5.exe) nella cartella in cui verrà archiviato lo strumento. Non è necessario espandere o installare il file.
   > [!NOTE]
   > Se si copia o si sposta il file in una cartella elencata nella variabile di ambiente **path** del sistema operativo, il file funzionerà in qualsiasi prompt dei comandi.

1. Aprire una finestra del prompt dei comandi. Se necessario, impostare la directory sul percorso dello strumento di ricerca degli errori.
1. Eseguire il comando seguente:
   ```cmd
   Err_6.4.5.exe <error code>
   ```
   > [!NOTE]  
   > In questo comando \<*error code*> rappresenta il codice esadecimale che si desidera cercare.

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

## <a name="more-information"></a>Ulteriori informazioni

Tenere presente che si tratta di uno strumento "temporizzato". Lo strumento ricerca errori Microsoft decodifica la maggior parte dei codici di errore Microsoft alla data in cui lo strumento è stato compilato. Poiché le nuove versioni di Windows aggiungono nuovi codici di errore e di evento, potrebbe essere necessario scaricare una nuova versione dello strumento di ricerca degli errori. Controllare l'area download Microsoft per una nuova versione o vedere i [codici di errore](system-error-codes.md).
