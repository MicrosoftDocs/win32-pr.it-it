---
title: Lettura dei valori dei colori da Framebuffer
description: Quando si usano funzioni che leggono i valori dei colori da framebuffer, tenere presente le differenze tra la lettura dei valori RGBA e i valori dell'indice dei colori nei dispositivi con colore reale e nei dispositivi basati sulla tavolozza.
ms.assetid: 70a96f09-37e9-4dfe-a6e0-0223e0a04bac
keywords:
- OpenGL in Windows,lettura dei valori dei colori da buffer frame
- lettura di valori di colore da buffer frame OpenGL
- framebuffers,lettura dei valori di colore OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65beb6dae04019637fc8683220ce12e671c4a52d4f015ae9f8d45e70db67bb36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117794768"
---
# <a name="reading-color-values-from-the-framebuffer"></a>Lettura dei valori dei colori da Framebuffer

Quando si usano funzioni che leggono i valori dei colori da framebuffer, tenere presente le differenze tra la lettura dei valori RGBA e i valori dell'indice dei colori nei dispositivi con colore reale e nei dispositivi basati sulla tavolozza.

In un dispositivo di colore reale:

-   I valori RGBA sono limitati al canale nel dispositivo.
-   I valori dell'indice dei colori vengono archiviati come valori RGBA in framebuffer. Quando si usano questi valori, è necessario eseguire una conversione inversa da RGBA all'indice della tavolozza logica. Se due indici logici hanno gli stessi valori RGBA, può essere restituito l'indice errato.

In un dispositivo basato sulla tavolozza:

-   I valori RGBA vengono letti da un indice nella tavolozza di sistema. L'indice logico viene ottenuto da una tabella inversa e i componenti RGBA vengono estratti.
-   I valori dell'indice dei colori vengono letti da un indice nella tavolozza di sistema e viene usata una tabella inversa per ottenere l'indice logico della tavolozza.

 

 




