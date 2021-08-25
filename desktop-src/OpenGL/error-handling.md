---
title: Gestione degli errori (OpenGL)
description: Quando OpenGL rileva un errore, registra un codice di errore corrente.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- gestione degli errori OpenGL
- Gestione degli errori OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 064330859b4e6b6d2d0bb9985e9f24d968a7daa5062215c64e82f89563ae06ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361381"
---
# <a name="error-handling-opengl"></a>Gestione degli errori (OpenGL)

Quando OpenGL rileva un errore, registra un codice di errore corrente. La funzione che ha causato l'errore viene ignorata, quindi non ha alcun effetto sullo stato OpenGL o sul contenuto framebuffer. (Se l'errore registrato è GL \_ OUT \_ OF \_ MEMORY, tuttavia, i risultati della funzione non sono definiti. Una volta registrato, il codice di errore corrente non viene cancellato fino a quando non si chiama la funzione di query [**glGetError,**](glgeterror.md) che restituisce il codice di errore corrente.

Le implementazioni di OpenGL possono restituire più codici di errore correnti, ognuno dei quali rimane impostato fino a quando non viene eseguita una query. La **funzione glGetError** restituisce GL NO ERROR dopo aver sottoposto a query tutti i codici di errore correnti o \_ se non è presente alcun \_ errore. Pertanto, se si ottiene un codice di errore, chiamare **glGetError** fino a quando non viene restituito GL NO ERROR per assicurarsi di \_ aver individuato tutti gli \_ errori. Per l'elenco dei codici di errore, vedere [Codici di errore OpenGL.](opengl-error-codes.md)

È possibile usare la [**funzione GLU gluErrorString**](gluerrorstring.md) per ottenere una stringa descrittiva corrispondente al codice di errore passato. Per altre informazioni su **gluErrorString,** vedere [Gestione degli errori.](handling-errors.md)

> [!Note]  
> Le funzioni GLU restituiscono spesso valori di errore se viene rilevato un errore. Inoltre, la libreria di utilità OpenGL definisce i codici di errore GLU INVALID ENUM, GLU INVALID VALUE e GLU OUT OF MEMORY, che hanno lo stesso significato dei codici di errore \_ \_ \_ \_ \_ \_ \_ OpenGL correlati.

 

 

 




