---
title: Scelta delle funzioni
description: Scelta delle funzioni
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Windows Media Player Skin per dispositivi mobili, funzioni per l'audio
- skins,funzioni per l'audio
- creazione di skin, funzioni per l'audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 222a7a6b26b225b0c40e461833f731c477c84338c458f88074fd747c33a1e70e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119833"
---
# <a name="choosing-the-functions"></a>Scelta delle funzioni

Lo scopo di questa interfaccia è fornire funzionalità di base per la riproduzione di audio. Verranno usate le funzioni seguenti:



| Funzione                     | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| PlayPause o PlayPauseStop\* | L'avvio dell'elemento multimediale è di importanza fondamentale. Se si crea un'interfaccia per Windows Media Player 10 Mobile o versione successiva, è consigliabile usare PlayPauseStop. Se si usa una versione precedente di Windows Media Player Mobile, è necessario usare PlayPause. Entrambe le funzioni offrono la funzionalità aggiunta di sospensione, ma solo PlayPauseStop consente di arrestare una trasmissione live quando la funzionalità di sospensione non è disponibile. |
| Interrompere                         | È necessario aggiungere Arresta per interrompere la riproduzione dell'elemento. Se si crea un'interfaccia per Windows Media Player 10 Mobile o versione successiva, la funzione PlayPauseStop fornisce già questa funzionalità.                                                                                                                                                                                                                                          |
| Prossima                         | Se si dispone di una playlist, sarà possibile scegliere l'elemento successivo. Questa funzionalità è necessaria per la navigazione di base dei supporti digitali.                                                                                                                                                                                                                                                                                                       |
| Prev (Precedente)                         | Anche se è possibile usare Avanti per scorrere la playlist fino all'inizio, l'aggiunta di Prev semplifica l'avanzamento dell'utente durante l'esplorazione della playlist.                                                                                                                                                                                                                                   |
| VolumeUp o VolumeDown\*     | È necessario fornire all'utente la possibilità di alzare o disattivare il volume.                                                                                                                                                                                                                                                                                                                                                    |



 

\*Disponibile per Windows Media Player 10 Mobile o versione successiva.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Guida all'interfaccia**](skin-guide.md)
</dt> </dl>

 

 




