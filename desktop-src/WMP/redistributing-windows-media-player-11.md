---
title: Ridistribuzione Windows Media Player 11
description: Ridistribuzione Windows Media Player 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec17042165ed891370d1543fad303150c4b21d1f1db7f9da38de9f75d02876a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117746560"
---
# <a name="redistributing-windows-media-player-11"></a>Ridistribuzione Windows Media Player 11

È possibile installare Windows Media Player 11 in Windows XP usando uno dei programmi di installazione seguenti, dove *localeId* è un identificatore delle impostazioni locali.

-   wmp11-windowsxp-x86-*localeId*.exe
-   wmp11-windowsxp-x64-*localeId*.exe

Di seguito è riportato un esempio di riga di comando per l'installazione senza interfaccia utente e senza prompt di riavvio o riavvio.


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



La tabella seguente illustra parametri aggiuntivi che è possibile usare con il programma Windows Media Player programma di installazione di 11.



| Parametro              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Impedire la migrazione delle librerie.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Creare un punto di ripristino di sistema annidato. Usare questa opzione se l'applicazione crea un punto di ripristino del sistema per annidare Windows Media Player punto di ripristino all'interno del punto di ripristino dell'applicazione.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Non consente la creazione di un punto di ripristino del sistema. Questo flag disabilita la creazione di un punto di ripristino del sistema. Nella maggior parte dei casi questo flag non deve essere usato per la ridistribuzione software generale. Deve essere usato solo quando è possibile scegliere esplicitamente per conto dell'utente finale di non supportare il rollback dei file Windows Media Player a una versione precedente di Player. Questo flag deve essere usato solo per la distribuzione aziendale o l'installazione OEM (Original Equipment Manufacturer). |
| /DefaultService        | Impostare lo store online iniziale. Per altre informazioni, vedere [Setup Command-line Parameters for Online Stores](setup-command-line-parameters-for-online-stores.md).                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ridistribuzione Windows Media Player Software**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




