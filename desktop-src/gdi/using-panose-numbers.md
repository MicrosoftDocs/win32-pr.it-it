---
description: I file dei tipi di carattere TrueType includono i numeri PANOSE, che le applicazioni possono usare per scegliere un tipo di carattere che corrisponda esattamente alle specifiche.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Uso dei numeri PANOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a974a0d1e708cac931e06e386e2df0802cbea79e5c9d499ca460d6deb5b0bab9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037459"
---
# <a name="using-panose-numbers"></a>Uso dei numeri PANOSE

I file dei tipi di carattere TrueType includono i numeri PANOSE, che le applicazioni possono usare per scegliere un tipo di carattere che corrisponda esattamente alle specifiche. Il sistema PANOSE classifica i visi in base a 10 attributi diversi. Per altre informazioni su questi attributi, vedere [**PANOSE**](/windows/win32/api/wingdi/ns-wingdi-panose). Una **struttura PANOSE** fa parte della [**struttura OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (i cui valori vengono compilati chiamando la funzione [**GetOutlineTextMetrics).**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa)

Gli attributi PANOSE vengono classificati singolarmente su una scala. I valori risultanti vengono concatenati per produrre un numero. Dato questo numero per un tipo di carattere e una metrica matematica per misurare le distanze nello spazio PANOSE, un'applicazione può determinare i vicini più vicini.

 

 



