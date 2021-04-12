---
title: Scelta delle funzioni
description: Scelta delle funzioni
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Windows Media Player Mobile Skins, funzioni per audio
- interfacce, funzioni per l'audio
- creazione di interfacce, funzioni per l'audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a139dc21a7d10847a7920955988ec2b02fced0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396690"
---
# <a name="choosing-the-functions"></a>Scelta delle funzioni

Lo scopo di questa interfaccia è fornire funzionalità di base per la riproduzione di audio. Verranno usate le funzioni seguenti:



| Funzione                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Come playpause o PlayPauseStop\* | L'avvio dell'elemento multimediale è di importanza fondamentale. Se si sta creando un'interfaccia per Windows Media Player 10 mobile o versione successiva, è necessario usare PlayPauseStop. Se si utilizza una versione precedente di Windows Media Player Mobile, è necessario utilizzare come playpause. Entrambe le funzioni forniscono la funzionalità aggiuntiva di sospensione, ma solo PlayPauseStop consente di arrestare una trasmissione in tempo reale quando la funzionalità di sospensione non è disponibile. |
| Interrompere                         | Si desidera aggiungere stop per interrompere la riproduzione dell'elemento. Se si sta creando un'interfaccia per Windows Media Player 10 mobile o versione successiva, la funzione PlayPauseStop fornisce già questa funzionalità.                                                                                                                                                                                                                                          |
| Prossima                         | Se si dispone di una playlist, sarà possibile scegliere l'elemento successivo. Questa operazione è necessaria per l'esplorazione di base dei file multimediali digitali.                                                                                                                                                                                                                                                                                                       |
| Prev (Precedente)                         | Sebbene sia possibile usare Next per scorrere la playlist fino a quando non si è arrivati all'inizio, l'aggiunta di Prev renderà più semplice per l'utente tornare indietro, oltre che avanti quando si naviga nella playlist.                                                                                                                                                                                                                                   |
| VolumeUp o VolumeDown\*     | È necessario fornire all'utente la possibilità di attivare o disattivare il volume.                                                                                                                                                                                                                                                                                                                                                    |



 

\*Disponibile per Windows Media Player 10 mobile o versione successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida all'interfaccia**](skin-guide.md)
</dt> </dl>

 

 




