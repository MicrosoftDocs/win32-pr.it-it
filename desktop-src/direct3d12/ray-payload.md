---
title: Struttura del payload ray
description: Struttura definita dall'utente fornita come argomento inout in una chiamata TraceRay e come parametro inout nei tipi shader che possono accedere al payload del raggio.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b2c1c6944bc66d33ebd134d6e2d0899c1992624cfb4db3b0fc0aaa80a1ef99a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119565631"
---
# <a name="ray-payload-structure"></a>Struttura del payload ray 

Struttura definita dall'utente fornita come argomento inout in una chiamata [**TraceRay**](traceray-function.md) e come parametro inout nei tipi shader che possono accedere al payload del raggio, che includono qualsiasi [hit,](any-hit-shader.md) [hit più](closest-hit-shader.md)vicino e [miss](miss-shader.md) shader. Tutti gli shader che accedono al payload ray devono usare la stessa struttura di quella fornita alla chiamata **TraceRay di** origine.  Anche se uno di questi shader non fa riferimento al payload ray, deve comunque specificare il payload corrispondente come chiamata **TraceRay di** origine.

