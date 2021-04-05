---
description: Nella tabella seguente vengono descritti i thread sui quali è possibile attivare gli eventi degli oggetti RecognizerContext. EventThreadsRecognitionFires sul thread di riconoscimento in background o sul thread che chiama il metodo Recognize dell'oggetto RecognizerContext. RecognitionWithAlternatesFires nel thread di riconoscimento in background.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Eventi oggetto RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc520801ae3391288966e6286d24449be4741b87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968036"
---
# <a name="recognizercontext-object-events"></a>Eventi oggetto RecognizerContext

Nella tabella seguente vengono descritti i thread sui quali è possibile attivare gli eventi degli oggetti [**RecognizerContext**](inkrecognizercontext-class.md) .



| Evento                                                                               | Thread                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Riconoscimento**](inkrecognizercontext-recognition.md)                             | Viene attivato sul thread di riconoscimento in background o sul thread che chiama il metodo [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) dell'oggetto [**RecognizerContext**](inkrecognizercontext-class.md) .<br/> |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Generato nel thread di riconoscimento in background.<br/>                                                                                                                                                               |



 

 

 




