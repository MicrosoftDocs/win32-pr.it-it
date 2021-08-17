---
description: Nella tabella seguente vengono descritti i thread su cui possono essere generati gli eventi dell'oggetto RecognizerContext. EventThreadsRecognitionFires nel thread di riconoscimento in background o nel thread che chiama il metodo Recognize dell'oggetto RecognizerContext. RecognitionWithAlternatesFires nel thread di riconoscimento in background.
ms.assetid: bcdf33aa-21bc-4218-a0a8-2edfa019f340
title: Eventi dell'oggetto RecognizerContext
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c8c8fa7aad4e7c6ba0dde2b38db4b82437b0732dda565aed8cc42750a339b1a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091441"
---
# <a name="recognizercontext-object-events"></a>Eventi dell'oggetto RecognizerContext

Nella tabella seguente vengono descritti i thread su cui possono essere generati gli eventi dell'oggetto [**RecognizerContext.**](inkrecognizercontext-class.md)



| Evento                                                                               | Thread                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Riconoscimento**](inkrecognizercontext-recognition.md)                             | Viene generato sul thread di riconoscimento in background o sul thread che chiama il metodo [**Recognize**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-recognize) dell'oggetto [**RecognizerContext.**](inkrecognizercontext-class.md)<br/> |
| [**RecognitionWithAlternates**](inkrecognizercontext-recognitionwithalternates.md) | Viene generato sul thread di riconoscimento in background.<br/>                                                                                                                                                               |



 

 

 




