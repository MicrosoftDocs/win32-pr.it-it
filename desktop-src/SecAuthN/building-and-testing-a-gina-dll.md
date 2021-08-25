---
description: Tutte le funzioni, i prototipi, le strutture e le costanti sono definiti nel file di intestazione Winwlx.h.
ms.assetid: 13b5bc92-583d-4031-94f9-f84dbfbf7ee7
title: Compilazione e test di una DLL GINA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31df8597ca9ad78b8c94efb5610e3c899f7834cb14c9112b15a410c72705a0cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883531"
---
# <a name="building-and-testing-a-gina-dll"></a>Compilazione e test di una DLL GINA

Tutte le funzioni, i prototipi, le strutture e le costanti sono definiti nel file di intestazione Winwlx.h.

> [!Note]  
> Le DLL GINA vengono ignorate in Windows Vista.

 

Per testare una DLL [*GINA,*](/windows/desktop/SecGloss/g-gly) usare il Winlogon.exe da una versione controllata del sistema operativo, disponibile con Microsoft Windows Driver Development Kit (DDK). La versione controllata di [*Winlogon supporta*](/windows/desktop/SecGloss/w-gly) il debug di file DIA come indicato di seguito:

-   È possibile usare la sintassi seguente per creare una sezione in Win.ini specificare le opzioni di debug di Winlogon.

    ``` syntax
    [WinlogonDebug]
    LogFile=C:\Winlogon.log
    DebugFlags=Flag1 [, Flag2 ...]
    ```

    Se specificato, **LogFile** deve contenere il nome completo del file che verrà usato per registrare le informazioni di debug. Se il file non esiste, verrà creato automaticamente.

    Le **opzioni DebugFlags** specificano i tipi di informazioni di debug da scrivere nel file di log o nel debugger. **DebugFlags** può contenere uno o più dei flag seguenti.

    

    | Flag di debug | Descrizione                                                                                                                                                                |
    |----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | CoolSwitch     | La combinazione di tasti CTRL+ALT+MAIUSC+TAB causerà un'interruzione del debug in Winlogon.                                                                                               |
    | Errore          | Errori di stampa.                                                                                                                                                              |
    | Init           | Stampare i messaggi di inizializzazione e di stato.                                                                                                                                |
    | Notifica         | Stampare i messaggi del pacchetto di notifica.                                                                                                                                       |
    | SAS            | Stampare informazioni sulle [*notifiche della sequenza di attenzione*](/windows/desktop/SecGloss/s-gly) sicura. |
    | State          | Stampare i messaggi quando Winlogon cambia stato.                                                                                                                                |
    | Timeout        | Stampare i messaggi quando viene impostato un limite di tempo o viene raggiunto un limite di tempo.                                                                                                        |
    | Trace          | Stampare informazioni dettagliate sulla traccia.                                                                                                                                           |
    | Avvisa           | Stampare gli avvisi.                                                                                                                                                            |

    

     

-   Per avviare la versione controllata di Winlogon in un debugger, aggiungere la voce seguente al Registro di sistema:

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
> È necessario usare il debugger Windows simbolico (NTSD) per eseguire il debug di Winlogon.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Caricamento ed esecuzione di una DLL GINA](loading-and-running-a-gina-dll.md)
</dt> <dt>

[Funzioni di esportazione DI GINA](authentication-functions.md)
</dt> <dt>

[Strutture DI GINA](authentication-structures.md)
</dt> <dt>

[Funzioni GINA di Servizi terminal](terminal-services-gina-functions.md)
</dt> </dl>

 

 
