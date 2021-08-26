---
description: Il terminale di riproduzione file e il terminale di registrazione file espongono le interfacce ITTerminal e ITMultiTrackTerminal. Questi oggetti espongono anche l'interfaccia ITMediaControl, che fornisce metodi per l'arresto, l'avvio e la navigazione multimediale.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminale di riproduzione file e terminale di registrazione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ad07ea46e2abf13465ac3344e69f586673c3b29463eac8bdd324966fb838368
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100591"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>Terminale di riproduzione file e terminale di registrazione file

Il terminale di riproduzione file e il terminale di registrazione file espongono le interfacce [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) [**e ITMultiTrackTerminal.**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) Questi oggetti espongono anche [**l'interfaccia ITMediaControl,**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) che fornisce metodi per l'arresto, l'avvio e la navigazione multimediale.

Il terminale di riproduzione file espone [**l'interfaccia ITMediaPlayback,**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) che dispone di metodi specifici per la riproduzione.

Il terminale di registrazione file espone [**l'interfaccia ITMediaRecord,**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) che fornisce metodi specifici della registrazione.

Come [terminali multitracking,](multitrack-terminals.md)terminale di registrazione file e terminale di riproduzione file gestiscono ognuno una raccolta di [terminali di traccia.](track-terminals.md)

 

 
