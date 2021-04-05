---
title: Trasformazione in coordinate finestra
description: Prima che le coordinate della clip vengano convertite in coordinate della finestra, sono divise per il valore di w per restituire coordinate del dispositivo normalizzate.
ms.assetid: 4c2d0bf6-89e8-485a-9080-c0599f989943
keywords:
- Pipeline di elaborazione OpenGL, conversione in coordinate finestra
- conversione in coordinate della finestra OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8ec3d8922890cfa3a79c5dacd94e93a06c53a73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103713924"
---
# <a name="transforming-to-window-coordinates"></a>Trasformazione in coordinate finestra

Prima che le coordinate della clip vengano convertite in coordinate della finestra, sono divise per il valore di *w* per restituire coordinate del dispositivo normalizzate. La trasformazione viewport applicata a queste coordinate normalizzate genera le coordinate della finestra. Si controlla il viewport, che determina l'area della finestra sullo schermo che visualizza un'immagine, con [**glDepthRange**](gldepthrange.md) e [**glViewport**](glviewport.md).

 

 




