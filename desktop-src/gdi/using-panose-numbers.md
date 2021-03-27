---
description: I file dei tipi di carattere TrueType includono i numeri PANOse, che possono essere usati dalle applicazioni per scegliere un tipo di carattere che corrisponda strettamente alle specifiche.
ms.assetid: 39fd56da-c744-432d-9623-92fc7d9bf5f5
title: Uso di numeri PANOse
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4dfa6a185e2afb05aec5fdf0e200300c7cf686a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233212"
---
# <a name="using-panose-numbers"></a>Uso di numeri PANOse

I file dei tipi di carattere TrueType includono i numeri PANOse, che possono essere usati dalle applicazioni per scegliere un tipo di carattere che corrisponda strettamente alle specifiche. Il sistema PANOn classifica i visi di 10 attributi diversi. Per ulteriori informazioni su questi attributi, vedere [**Panose**](/windows/win32/api/wingdi/ns-wingdi-panose). Una struttura **Panoa** fa parte della struttura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) (i cui valori sono compilati chiamando la funzione [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) ).

Gli attributi PANOn vengono classificati singolarmente su una scala. I valori risultanti vengono concatenati per produrre un numero. Dato questo numero per un tipo di carattere e una metrica matematica per misurare le distanze nello spazio PANOn, un'applicazione può determinare gli elementi adiacenti più vicini.

 

 



