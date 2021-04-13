---
description: Tutte le funzioni, i prototipi, le strutture e le costanti vengono definiti nel file di intestazione Winwlx. h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Compilazione e test di una DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02e6e4a00f15e6ced4827bbc3efeb3c459f5d6a8
ms.sourcegitcommit: 70f39ec77d19d3c32c376ee2831753d2cafae41a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "104352046"
---
# <a name="building-and-testing-a-gina-dll"></a>Compilazione e test di una DLL GINA

Tutte le funzioni, i prototipi, le strutture e le costanti vengono definiti nel file di intestazione Winwlx. h.

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

Per testare una dll [*Gina*](/windows/desktop/SecGloss/g-gly) , utilizzare il Winlogon.exe da una versione controllata del sistema operativo, disponibile con Microsoft Windows Driver Development Kit (DDK). La versione controllata di [*Winlogon*](/windows/desktop/SecGloss/w-gly) supporta il debug di Ginas come indicato di seguito:

-   È possibile usare la sintassi seguente per creare una sezione in Win.ini per specificare le opzioni di debug di Winlogon.

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    Se specificato, **logfile** deve contenere il nome completo del file che verrà usato per registrare le informazioni di debug. Se il file non esiste, verrà creato automaticamente.

    Le opzioni **DebugFlags** specificano i tipi di informazioni di debug da scrivere nel file di log o nel debugger. **DebugFlags** può contenere uno o più dei flag seguenti.

    

    | Flag di debug | Descrizione                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | CoolSwitch     | La combinazione di tasti CTRL + ALT + MAIUSC + TAB provocherà un'operazione di debug in Winlogon.                                                                                               |
    | Errore          | Errori di stampa.                                                                                                                                                              |
    | Init           | Messaggi di inizializzazione e di stato di stampa.                                                                                                                                |
    | Notifica         | Stampa messaggi del pacchetto di notifica.                                                                                                                                       |
    | SAS            | Stampa le informazioni sulle notifiche di [*Secure Attention Sequence*](/windows/desktop/SecGloss/s-gly) (SAS). |
    | State          | Stampare messaggi quando lo stato di Winlogon cambia.                                                                                                                                |
    | Timeout        | Stampare i messaggi quando viene impostato un limite di tempo o viene raggiunto un limite di tempo.                                                                                                        |
    | Trace          | Stampa le informazioni di traccia dettagliate.                                                                                                                                           |
    | Avvisa           | Avvisi di stampa.                                                                                                                                                            |

    

     

-   Per avviare la versione controllata di Winlogon in un debugger, aggiungere la voce seguente al registro di sistema:

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows NT
                CurrentVersion
                   Image File Execution Options
                      winlogon.exe
                         Debugger = ntsd -d<dl>
    <dt>

                     Data type
</dt>
    <dd>                     REG_SZ</dd>
    </dl>
    ```

> [!NOTE]
> Per eseguire il debug di Winlogon, è necessario usare il debugger simbolico di Windows (NTSD).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Caricamento ed esecuzione di una DLL GINA](loading-and-running-a-gina-dll.md)
</dt> <dt>

[Funzioni di esportazione GINA](authentication-functions.md)
</dt> <dt>

[Strutture GINA](authentication-structures.md)
</dt> <dt>

[Funzioni di Servizi terminal GINA](terminal-services-gina-functions.md)
</dt> </dl>

 

 
