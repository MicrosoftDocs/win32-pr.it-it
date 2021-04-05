---
title: Esecuzione di query e impostazione del tempo
description: Esecuzione di query e impostazione del tempo
ms.assetid: 84eba230-88b6-4cba-9e90-ba0b4bcfc691
keywords:
- MIDI (Musical Instrument Digital Interface), tempo
- MIDI (Musical Instrument Digital Interface), tempo
- Sequencer MIDI MCI, tempo
- Comando MCI_STATUS
- tempo sequenza
- tempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3927d2f04e1b073b25c262437620325dc5cd040
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714578"
---
# <a name="querying-and-setting-the-tempo"></a>Esecuzione di query e impostazione del tempo

Per recuperare il tempo di una sequenza, utilizzare il comando [**MCI \_ status**](mci-status.md) e impostare il membro **dwItem** della struttura [**\_ \_ parametri stato MCI**](mci-status-parms.md) su MCI \_ seq \_ status \_ tempo. Se il comando di **\_ stato MCI** ha esito positivo, il membro **dwReturn** della struttura **\_ \_ parametri stato MCI** contiene il tempo corrente.

Per modificare il tempo, utilizzare il comando [**MCI \_ set**](mci-set.md) con la struttura [**MCI \_ seq \_ set \_ parametri**](mci-seq-set-parms.md) , specificando \_ il \_ flag set tempo per MCI Seq set \_ tempo e impostando il membro **dwTempo** della struttura sul tempo desiderato.

Il modo in cui viene rappresentato il tempo dipende dal tipo di divisione della sequenza. Se il tipo di divisione è PPQN, il tempo viene rappresentato in battute al minuto. Se il tipo di divisione è uno dei tipi di divisione SMPTE, il tempo viene rappresentato in frame al secondo. Per informazioni sulla determinazione del tipo di divisione di una sequenza, vedere [recupero del tipo di divisione Sequence](retrieving-the-sequence-division-type.md).

 

 




