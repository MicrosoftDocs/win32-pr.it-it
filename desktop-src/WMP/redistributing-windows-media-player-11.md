---
title: Ridistribuzione di Windows Media Player 11
description: Ridistribuzione di Windows Media Player 11
ms.assetid: 3348821f-6d72-40c2-954b-0046ce502401
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674da0298196f0749a549670bf9bd7c4095b6e7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044488"
---
# <a name="redistributing-windows-media-player-11"></a>Ridistribuzione di Windows Media Player 11

È possibile installare Windows Media Player 11 in Windows XP utilizzando uno dei seguenti programmi di installazione, in cui *LocaleID* è un identificatore delle impostazioni locali.

-   wmp11-windowsxp-x86-*LocaleID*. exe
-   WMP11-WindowsXP-x64-*LocaleID*. exe

Di seguito è riportato un esempio di una riga di comando per l'installazione senza interfaccia utente e nessuna richiesta di riavvio o riavvio.


```
wmp11-windowsxp-x86-enu.exe /q:A /c:"setup_wm.exe /Q /R:N"
```



La tabella seguente illustra i parametri aggiuntivi che è possibile usare con il programma di installazione di Windows Media Player 11.



| Parametro              | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| /NoMigrate             | Impedisci la migrazione della libreria.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| /NestedRestore         | Creare un punto di ripristino del sistema annidato. Usare questa istruzione se l'applicazione crea un punto di ripristino del sistema per annidare il punto di ripristino di Windows Media Player all'interno del punto di ripristino dell'applicazione.                                                                                                                                                                                                                                                                                                                             |
| /DisallowSystemRestore | Impedisce la creazione di un punto di ripristino del sistema. Questo flag Disabilita la creazione di un punto di ripristino del sistema. Nella maggior parte dei casi non è consigliabile usare questo flag per la ridistribuzione generale del software. Questa operazione deve essere utilizzata solo quando è possibile effettuare una scelta esplicita per conto dell'utente finale per non supportare il rollback dei file di Media Player Windows a una versione precedente del lettore. Questo flag deve essere usato solo per la distribuzione aziendale o l'installazione OEM (Original Equipment Manufacturer). |
| /DefaultService        | Impostare l'archivio online iniziale. Per ulteriori informazioni, vedere [impostazione dei parametri della riga di comando per i negozi online](setup-command-line-parameters-for-online-stores.md).                                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Ridistribuzione del software Windows Media Player**](redistributing-windows-media-player-software.md)
</dt> </dl>

 

 




