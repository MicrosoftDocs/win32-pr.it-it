---
title: Conversione dello spazio colore
description: Conversione dello spazio colore
ms.assetid: f5f1ec99-b3b9-4420-bf64-3872d9bbe650
keywords:
- Windows Media Format SDK, conversione dello spazio colore
- ASF (Advanced Systems Format), conversione dello spazio colore
- ASF (formato avanzato dei sistemi), conversione dello spazio colore
- conversione dello spazio colore
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cbc284995cbc72aee148e12977dad9f4476b29c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221420"
---
# <a name="color-space-conversion"></a>Conversione dello spazio colore

Spesso esiste una differenza tra la profondità di colore del formato video compresso nel profilo e il formato di input. Quando si verifica questo problema, il video di origine deve essere convertito per essere conforme allo spazio dei colori della destinazione. Il writer gestisce questo processo, comunicando con un convertitore di spazi colore interno.

Il lettore comunica anche con il convertitore di spazi dei colori per risolvere le differenze tra il formato compresso e il formato di output.

Come per tutte le trasformazioni eseguite sui dati, la conversione tra le profondità dei colori può ridurre la qualità dell'output. Quando possibile, è consigliabile usare i formati di input e di output con la stessa profondità di colore del formato compresso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Funzionalità di scrittura di file**](file-writing-features.md)
</dt> <dt>

[**Utilizzo degli input**](working-with-inputs.md)
</dt> <dt>

[**Uso degli output**](working-with-outputs.md)
</dt> </dl>

 

 




