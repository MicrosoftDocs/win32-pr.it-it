---
description: Un terminale multitraccia può essere pensato come un terminale che è una raccolta di altri terminali. Ogni terminale figlio (&\# 0034; traccia&\# 0034;) può essere un terminale multitraccia o un terminale a traccia singola.
ms.assetid: bf23bc26-5763-45a3-a63d-e43ce2480956
title: Informazioni sui terminali multitraccia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa84537c3cf7764ba7e4520d32a325b89ad4dffd9921daa14bc5e0c968c7763f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118872904"
---
# <a name="about-multitrack-terminals"></a>Informazioni sui terminali multitraccia

Un terminale multitraccia può essere pensato come un terminale che è una raccolta di altri terminali. Ogni terminale figlio (una "traccia") può essere un terminale multitraccia o un terminale a traccia singola.

Tutti i terminali multitraccia espongono l'interfaccia [**ITMultiTrackTerminal,**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) che include metodi generici per enumerare, creare e rimuovere terminali di traccia da un terminale multitraccia. Tutti i terminali, a traccia singola e multitraccia, espongono [**l'interfaccia ITTerminal.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)

Un client che ha un puntatore a un'interfaccia [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) può individuare se il terminale è multitraccia o a traccia singola tramite una query sul terminale per l'interfaccia [**ITMultiTrackTerminal,**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal) esposta solo sui terminali multitraccia.

Il terminale padre può usare [**l'interfaccia ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) dei relativi terminali di traccia oppure può richiedere terminali di traccia per esporre interfacce private.

Per altre informazioni, vedere [Track Terminals](track-terminals.md).

 

 
