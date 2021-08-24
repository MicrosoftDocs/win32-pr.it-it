---
description: TAPI 3.1 introduce la nozione di terminale multitraccia, un terminale che, in sostanza, è una raccolta di terminali &\# 0034; traccia&\# 0034; terminali.
ms.assetid: 8dd6f792-a29e-40fd-9f5b-ee5525028c2e
title: Terminali multitraccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f9e5f9c6d614308370b3d9211f578d5fcb2650bd3c5ba7f8a81dbc981ad2687
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119575521"
---
# <a name="multitrack-terminals"></a>Terminali multitraccia

TAPI 3.1 introduce la nozione di terminale multitraccia, un terminale che, in sostanza, è una raccolta di terminali "tracciati". I terminali multitraccia semplificano il carico del programmatore in situazioni in cui più flussi multimediali sono coinvolti in una sessione di comunicazione.

Il [terminale di registrazione file](file-playback-terminal-and-file-recording-terminal.md) è un esempio di terminale multitraccia. È costituito da "tracce", dove ogni "traccia" è un terminale corrispondente a un flusso nel file registrato.

Un [terminale di](track-terminals.md) traccia può essere un altro terminale multitraccia o un terminale a traccia singola. Un terminale a traccia singola è un terminale che non dispone di terminali binari. Un terminale a traccia singola è un terminale nel senso TAPI 3 della parola.

Per altre informazioni sui terminali multitraccia, vedere gli argomenti seguenti:

-   [Informazioni sui terminali multitraccia](about-multitrack-terminals.md)
-   [Meccanismo di selezione del terminale predefinito](default-terminal-selection-mechanism.md)
-   [Selezione manuale del terminale](manual-terminal-selection.md)
-   [Uso dei terminali multitraccia e del meccanismo di selezione predefinito](using-multitrack-terminals-and-the-default-selection-mechanism.md)

 

 



