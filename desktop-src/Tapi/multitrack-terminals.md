---
description: TAPI 3,1 introduce la nozione di un terminale multitraccia, un terminale che, in sostanza, è una raccolta di &\# 0034, track&\# 0034; terminali.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Terminali multitraccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb795169f5e7cbd669e0bceb1d635e33c912c50a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308291"
---
# <a name="multitrack-terminals"></a>Terminali multitraccia

TAPI 3,1 introduce la nozione di un terminale multitraccia, un terminale che, in sostanza, è una raccolta di terminali "Track". I terminali multitraccia facilitano il caricamento del programmatore in situazioni in cui più flussi multimediali sono interessati da una sessione di comunicazione.

Il [terminale di registrazione file](file-playback-terminal-and-file-recording-terminal.md) è un esempio di terminale multitraccia. È costituito da "tracks", dove ogni "Track" è un terminale corrispondente a un flusso nel file registrato.

Un [terminale di Track](track-terminals.md) può essere un altro terminale multitraccia o un terminale a traccia singola. Un terminale a traccia singola è un terminale senza terminali di rilevamento. Un terminale a traccia singola è un terminale in TAPI 3 Sense of the Word.

Per ulteriori informazioni sui terminali multitraccia, vedere gli argomenti seguenti:

-   [Informazioni sui terminali multitraccia](about-multitrack-terminals.md)
-   [Meccanismo di selezione terminali predefinito](default-terminal-selection-mechanism.md)
-   [Selezione terminale manuale](manual-terminal-selection.md)
-   [Uso di terminali multitraccia e del meccanismo di selezione predefinito](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



