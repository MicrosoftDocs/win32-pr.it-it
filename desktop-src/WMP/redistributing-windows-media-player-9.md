---
title: Ridistribuzione Windows Media Player serie 9
description: Ridistribuzione Windows Media Player serie 9
ms.assetid: 812e3fc7-e23d-489c-a486-62c7602cf46e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 418a780836c0a64a1b31b0d3c01a69841b695803f5db61b049915ec0d981f9c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119861681"
---
# <a name="redistributing-windows-media-player-9-series"></a>Ridistribuzione Windows Media Player serie 9

È possibile installare Windows Media Player serie 9 in Windows XP usando uno dei programmi di installazione seguenti.

-   MPSetupXP.exe
-   MPSetup.exe

> [!Note]  
> MPSetup.exe è un superset del programma MPSetupXP.exe programma di installazione. Contiene i file necessari per i sistemi operativi rilasciati prima di Windows XP. MPSetup.exe funzionalmente equivalente a MPSetupXP.exe quando viene eseguito in Windows XP, ma le dimensioni del file del programma di installazione sono maggiori perché non è stato ottimizzato per l'installazione nei sistemi operativi Windows XP.

 

È possibile installare Windows Media Player serie 9 in Windows 98 Second Edition, Windows Millennium Edition o Windows 2000 usando il programma di installazione seguente.

-   MPSetup.exe

Di seguito è riportato un esempio di riga di comando per l'installazione senza interfaccia utente e senza prompt di riavvio o riavvio.


```
MPSetup.exe /q:A /c:"setup_wm.exe /Q /R:N /P:#e"
```



> [!Note]  
> Il parametro /P: e specifica che il pacchetto Windows Media Player di installazione deve essere memorizzato nella cache durante Windows Media Player \# installazione. Questo comando viene usato per gestire gli aggiornamenti futuri del sistema operativo. Questo comando deve essere omesso solo dagli amministratori IT aziendali. L'unico caso in cui /P: e non deve essere incluso nella riga di comando è quando si è proprietari del sistema di destinazione e si sa che il sistema di destinazione non verrà mai aggiornato a un sistema operativo \# successivo. Ad esempio, se si installa Windows Media Player serie 9 in Windows 2000 e il computer potrebbe essere aggiornato a Windows XP, è necessario usare /P: e nella riga di \# comando. In caso contrario, dopo l Windows installazione di XP, i file Windows Media Player verranno sovrascritti con i file per Windows Media Player per Windows XP.

 

La tabella seguente illustra parametri aggiuntivi che è possibile usare con il programma di installazione Windows Media Player serie 9.



| Parametro              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Impedire la migrazione della libreria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Creare un punto di ripristino di sistema annidato. Usare questa opzione se l'applicazione crea un punto di ripristino di sistema per annidare Windows Media Player punto di ripristino all'interno del punto di ripristino dell'applicazione.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Non consentire la creazione di un punto di ripristino di sistema. Questo flag disabilita la creazione di un punto di ripristino di sistema. Nella maggior parte dei casi questo flag non deve essere usato per la ridistribuzione software generale. Deve essere usato solo quando è possibile scegliere esplicitamente per conto dell'utente finale di non supportare il rollback dei file Windows Media Player a una versione precedente di Player. Questo flag deve essere usato solo per la distribuzione aziendale o l'installazione OEM (Original Equipment Manufacturer). |



 

## <a name="notes"></a>Note

-   Per i parametri della riga di comando viene fatto distinzione tra maiuscole e minuscole.
-   Quando si elimina la richiesta di riavvio, è necessario controllare la chiave del Registro di sistema InstallResult e gestire la notifica di riavvio nell'applicazione di installazione chiamante.
-   Windows Media Player serie 9 installa anche il runtime di Windows Media Format, quindi non è necessario includere sia il pacchetto di distribuzione Windows Media Player che il pacchetto di distribuzione del runtime di Windows Media Format nello stesso pacchetto di ridistribuzione software. Pertanto, se si includono MPSetup.exe o MPSetupXP.exe nell'installazione, non è necessario includere WMFdist.exe.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ridistribuzione Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




