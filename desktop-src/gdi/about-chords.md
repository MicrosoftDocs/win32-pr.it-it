---
description: Una corda è un'area delimitata dall'intersezione tra un'ellisse e un segmento di linea chiamato secante. La figura seguente mostra un accordo disegnato usando la funzione Chord.
ms.assetid: 9aa35b39-06f2-48bf-b32c-3e3e32fab68b
title: Informazioni sugli accordi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18d6310c47a503766e61b9c7936816a5891da89a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527703"
---
# <a name="about-chords"></a>Informazioni sugli accordi

Una *corda* è un'area delimitata dall'intersezione tra un'ellisse e un segmento di linea chiamato *secante*. La figura seguente mostra un accordo disegnato usando la funzione [**Chord**](/windows/desktop/api/Wingdi/nf-wingdi-chord) .

![illustrazione di un Elipse, che mostra due radiali, una secante e una corda](images/csfsh-02.png)

Quando si chiama [**Chord**](/windows/win32/api/wingdi/nf-wingdi-chord), un'applicazione fornisce le coordinate degli angoli superiore sinistro e inferiore destro del rettangolo di delimitazione dell'ellisse, nonché le coordinate di due punti che definiscono due radiali. Una radiale è una linea disegnata dal centro del rettangolo di delimitazione di un'ellisse a un punto nell'ellisse.

Quando il sistema disegna la parte curva della corda, esegue questa operazione utilizzando la direzione di arco corrente per il contesto di dispositivo specificato. La direzione di arco predefinita è in senso antiorario. È possibile reimpostare la direzione dell'arco chiamando la funzione [**SetArcDirection**](/windows/desktop/api/Wingdi/nf-wingdi-setarcdirection) .

 

 
