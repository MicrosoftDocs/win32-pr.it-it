---
title: Ridistribuzione di Windows Media Player 9 Series
description: Ridistribuzione di Windows Media Player 9 Series
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f48da20123255ae08a0993d361a95deb8ed335
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045257"
---
# <a name="redistributing-windows-media-player-9-series"></a>Ridistribuzione di Windows Media Player 9 Series

È possibile installare la serie Windows Media Player 9 in Windows XP utilizzando uno dei seguenti programmi di installazione.

-   MPSetupXP.exe
-   MPSetup.exe

> [!Note]  
> MPSetup.exe è un superset del programma di installazione di MPSetupXP.exe. Contiene i file necessari per i sistemi operativi rilasciati prima di Windows XP. MPSetup.exe è equivalente dal punto di vista funzionale al MPSetupXP.exe quando viene eseguito in Windows XP, ma le dimensioni del file del programma di installazione sono maggiori perché non sono state ottimizzate per l'installazione nei sistemi operativi Windows XP.

 

È possibile installare la serie Windows Media Player 9 in Windows 98 Second Edition, Windows Millennium Edition o Windows 2000 usando il programma di installazione seguente.

-   MPSetup.exe

Di seguito è riportato un esempio di una riga di comando per l'installazione senza interfaccia utente e nessuna richiesta di riavvio o riavvio.


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> Il parametro/P: \# e specifica che il pacchetto di installazione di windows media Player deve essere memorizzato nella cache durante l'installazione di windows media player. Questo comando viene utilizzato per gestire gli aggiornamenti futuri del sistema operativo. Questo comando deve essere omesso solo dagli amministratori IT aziendali. L'unico caso in cui/P: \# e non deve essere incluso nella riga di comando è quando si è proprietari del sistema di destinazione e si sa che il sistema di destinazione non verrà mai aggiornato a un sistema operativo successivo. Se ad esempio si installa la serie Windows Media Player 9 in Windows 2000 e il computer potrebbe essere aggiornato a Windows XP, è necessario utilizzare/P: \# e nella riga di comando. In caso contrario, dopo l'installazione di Windows XP, i file di Windows Media Player verranno sovrascritti con i file per Windows Media Player per Windows XP.

 

La tabella seguente illustra i parametri aggiuntivi che è possibile usare con il programma di installazione della serie Windows Media Player 9.



| Parametro              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Impedisci la migrazione della libreria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Creare un punto di ripristino del sistema annidato. Usare questa istruzione se l'applicazione crea un punto di ripristino del sistema per annidare il punto di ripristino di Windows Media Player all'interno del punto di ripristino dell'applicazione.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Impedisce la creazione di un punto di ripristino del sistema. Questo flag Disabilita la creazione di un punto di ripristino del sistema. Nella maggior parte dei casi non è consigliabile usare questo flag per la ridistribuzione generale del software. Questa operazione deve essere utilizzata solo quando è possibile effettuare una scelta esplicita per conto dell'utente finale per non supportare il rollback dei file di Media Player Windows a una versione precedente del lettore. Questo flag deve essere usato solo per la distribuzione aziendale o l'installazione OEM (Original Equipment Manufacturer). |



 

## <a name="notes"></a>Note

-   I parametri della riga di comando distinguono tra maiuscole e minuscole.
-   Quando si disattiva la richiesta di riavvio, è necessario controllare la chiave del registro di sistema InstallResult e gestire la notifica di riavvio nell'applicazione di installazione chiamante.
-   La serie Windows Media Player 9 installa anche il runtime di Windows Media Format, pertanto non è necessario includere il pacchetto di distribuzione di Windows Media Player e il pacchetto di distribuzione di runtime di Windows Media Format nello stesso pacchetto di ridistribuzione software. Se pertanto si includono MPSetup.exe o MPSetupXP.exe nell'installazione di, non è necessario includere WMFdist.exe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ridistribuzione del software Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




