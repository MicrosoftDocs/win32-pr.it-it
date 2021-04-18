---
title: Struttura di payload Ray
description: Struttura definita dall'utente fornita come argomento INOUT in una chiamata TraceRay e come parametro inout nei tipi shader che possono accedere al payload del raggio.
ms.assetid: ''
ms.localizationpriority: low
ms.topic: language-reference
ms.date: 05/31/2018
ms.openlocfilehash: 9887bbadc2fd94b2e766c568a30fd6669f51e048
ms.sourcegitcommit: 5b98bf8c68922f8f03c14f793fbe17504900559c
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/12/2021
ms.locfileid: "106320442"
---
# <a name="ray-payload-structure"></a>Struttura di payload Ray 

Struttura definita dall'utente, fornita come argomento INOUT in una chiamata [**TraceRay**](traceray-function.md) , e come parametro inout nei tipi shader che possono accedere al payload del raggio, che include [qualsiasi hit](any-hit-shader.md), [hit più vicino](closest-hit-shader.md)e [mancato](miss-shader.md) shader. Gli shader che accedono al payload del raggio devono usare la stessa struttura di quella fornita alla chiamata **TraceRay** di origine.  Anche se uno di questi shader non fa riferimento al payload del raggio, deve comunque specificare il payload corrispondente come chiamata **TraceRay** di origine.

