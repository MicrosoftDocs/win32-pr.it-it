---
description: Il terminale per la riproduzione di file e il terminale di registrazione file espongono le interfacce ITTerminal e ITMultiTrackTerminal. Questi oggetti espongono anche l'interfaccia ITMediaControl, che fornisce metodi per l'arresto, l'avvio e la navigazione multimediale.
ms.assetid: 16b04ce1-d625-4824-bb1e-994a292cd42c
title: Terminale di riproduzione file e terminale di registrazione file
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a73c788e3e1750e44298c1020a088cf8111bee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967468"
---
# <a name="file-playback-terminal-and-file-recording-terminal"></a>Terminale di riproduzione file e terminale di registrazione file

Il terminale per la riproduzione di file e il terminale di registrazione file espongono le interfacce [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) e [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) . Questi oggetti espongono anche l'interfaccia [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol) , che fornisce metodi per l'arresto, l'avvio e la navigazione multimediale.

Il terminale per la riproduzione di file espone l'interfaccia [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) , che include metodi specifici per la riproduzione.

Il terminale di registrazione file espone l'interfaccia [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord) , che fornisce metodi specifici per la registrazione.

Come [terminali multitraccia](multitrack-terminals.md), il terminale per la registrazione di file e il terminale di riproduzione file gestiscono una raccolta di [terminali Track](track-terminals.md).

 

 
