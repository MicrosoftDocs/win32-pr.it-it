---
title: Trasformazione in coordinate della finestra
description: Prima che le coordinate di ritaglio siano convertite in coordinate della finestra, vengono divise per il valore di w per produrre coordinate del dispositivo normalizzate.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- Pipeline di elaborazione OpenGL, conversione in coordinate finestra
- conversione in coordinate della finestra OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fa74b42457349b14e151099a3c4238e855ad0001e1b8f9416808a1279b82345
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119887991"
---
# <a name="transforming-to-window-coordinates"></a>Trasformazione in coordinate della finestra

Prima che le coordinate di ritaglio siano convertite in coordinate della finestra, vengono divise per il valore *di w* per produrre coordinate del dispositivo normalizzate. La trasformazione viewport applicata a queste coordinate normalizzate produce coordinate della finestra. Puoi controllare il viewport, che determina l'area della finestra su schermo che visualizza un'immagine, con [**glDepthRange**](gldepthrange.md) e [**glViewport**](glviewport.md).

 

 




