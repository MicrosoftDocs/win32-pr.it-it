---
description: Una chord è un'area delimitata dall'intersezione di un'ellisse e di un segmento di linea denominato sere. La figura seguente mostra una cora disegnata usando la funzione Chord.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Informazioni su Chords
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3bad0d17d34386ada7c7c3b46bb1bcc4db5f9a2ce572ce78c33f8f4b6af909
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119400531"
---
# <a name="about-chords"></a>Informazioni su Chords

Una *chord è* un'area delimitata dall'intersezione di un'ellisse e di un segmento di linea denominato *sere*. La figura seguente mostra una cora disegnata usando la [**funzione Chord.**](/windows/desktop/api/Wingdi/nf-wingdi-chord)

![illustrazione di un elipse, che mostra due radiali, un senato e una chord](images/csfsh-02.png)

Quando si chiama [**Chord,**](/windows/win32/api/wingdi/nf-wingdi-chord)un'applicazione fornisce le coordinate degli angoli superiore sinistro e inferiore destro del rettangolo di delimitazione dell'ellisse, nonché le coordinate di due punti che definiscono due radiali. Un radiale è una linea disegnata dal centro del rettangolo di delimitazione di un'ellisse a un punto sull'ellisse.

Quando il sistema disegna la parte curva della chord, lo fa usando la direzione dell'arco corrente per il contesto di dispositivo specificato. La direzione dell'arco predefinita è in senso antiorario. È possibile fare in modo che l'applicazione azzeri la direzione dell'arco chiamando la [**funzione SetArcDirection.**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection)

 

 
