---
description: Delle sei modalità di mapping predefinite, una è dipendente dal dispositivo (MM TEXT) e le cinque rimanenti \_ (MM \_ HIENGLISH, MM \_ LOENGLISH, MM \_ HIMETRIC, MM LOMETRIC e \_ MM \_ TWIPS) sono indipendenti dal dispositivo.
ms.assetid: 722df020-edf2-4763-b58c-3e29fa7007db
title: Modalità di mapping predefinite
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c0eecce6196672db11d61326c82364c1fde1d1b494e48ff77e214e79df91e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119037679"
---
# <a name="predefined-mapping-modes"></a>Modalità di mapping predefinite

Delle sei modalità di mapping predefinite, una è dipendente dal dispositivo (MM TEXT) e le cinque rimanenti \_ (MM \_ HIENGLISH, MM \_ LOENGLISH, MM \_ HIMETRIC, MM LOMETRIC e \_ MM \_ TWIPS) sono indipendenti dal dispositivo.

La modalità di mapping predefinita è MM \_ TEXT. Un'unità logica è uguale a un pixel. La x positiva è a destra e y positivo è in basso. Questa modalità viene mappata direttamente al sistema di coordinate del dispositivo. Il mapping logico-fisico comporta solo un offset in x e y definito dalle origini finestra e viewport controllate dall'applicazione. Gli extent del viewport e della finestra sono tutti impostati su 1, creando un mapping uno-a-uno.

Le applicazioni che visualizzano forme geometriche (cerchi, quadrati, poligoni e così via) usano una delle modalità di mapping indipendenti dal dispositivo. Ad esempio, se si scrive un'applicazione per fornire funzionalità di creazione di grafici per un foglio di calcolo e si vuole garantire che il diametro di ogni grafico a torta sia di 2 pollici, usare la modalità di mapping MM LOENGLISH e chiamare le funzioni appropriate per disegnare e riempire il \_ grafico. Specificando MM LOENGLISH, il diametro del grafico è coerente \_ su qualsiasi display o stampante. Se si usa MM TEXT invece di MM LOENGLISH, un grafico che appare circolare su un display VGA apparirebbe ellittico su un display EGA e apparirebbe molto piccolo su una stampante laser da \_ \_ 300 dpi (punti per pollice).

 

 



