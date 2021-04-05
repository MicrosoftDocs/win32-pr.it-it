---
title: Lettura dei valori di colore dal framebuffer
description: Quando si usano le funzioni che leggono i valori di colore dal framebuffer, tenere presente le differenze tra la lettura dei valori RGBA e i valori di indice colore nei dispositivi con colori reali e nei dispositivi basati su tavolozza.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL per Windows, lettura dei valori dei colori da framebuffer
- lettura dei valori di colore da framebuffer OpenGL
- framebuffer, lettura dei valori di colore OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4df14690b68f7e93949d26ee50ac562ebd667be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709358"
---
# <a name="reading-color-values-from-the-framebuffer"></a>Lettura dei valori di colore dal framebuffer

Quando si usano le funzioni che leggono i valori di colore dal framebuffer, tenere presente le differenze tra la lettura dei valori RGBA e i valori di indice colore nei dispositivi con colori reali e nei dispositivi basati su tavolozza.

Su un dispositivo a colori true:

-   I valori RGBA sono limitati al canale nel dispositivo.
-   I valori di indice dei colori vengono archiviati come valori RGBA nel framebuffer. Quando si usano questi valori, è necessario eseguire una conversione inversa da RGBA all'indice della tavolozza logica. Se due indici logici hanno gli stessi valori RGBA, può essere restituito l'indice errato.

In un dispositivo basato su tavolozza:

-   I valori RGBA vengono letti da un indice nella tavolozza di sistema. L'indice logico viene ottenuto da una tabella inversa e vengono estratti i componenti RGBA.
-   I valori di indice colore vengono letti da un indice nella tavolozza di sistema e viene utilizzata una tabella inversa per ottenere l'indice della tavolozza logica.

 

 




