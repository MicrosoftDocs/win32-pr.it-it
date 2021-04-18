---
title: Gestione degli errori (OpenGL)
description: Quando OpenGL rileva un errore, registra un codice di errore corrente.
ms.assetid: 8e40e382-14fd-44df-8e1c-ebceb34af19c
keywords:
- gestione degli errori OpenGL
- Gestione degli errori OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2005eb38f85e6e57f814a3ec61abf8b76fa4761
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300827"
---
# <a name="error-handling-opengl"></a>Gestione degli errori (OpenGL)

Quando OpenGL rileva un errore, registra un codice di errore corrente. La funzione che ha causato l'errore viene ignorata, quindi non ha alcun effetto sullo stato OpenGL o sul contenuto del framebuffer. (Se l'errore registrato è GL \_ \_ \_ Memoria insufficiente, tuttavia, i risultati della funzione non sono definiti. Una volta registrato, il codice di errore corrente non viene cancellato fino a quando non si chiama la funzione di query [**glGetError**](glgeterror.md) , che restituisce il codice di errore corrente.

Le implementazioni di OpenGL possono restituire più codici di errore correnti, ognuno dei quali rimane impostato fino a quando non viene eseguita una query. La funzione **glGetError** restituisce GL \_ senza \_ errori dopo aver eseguito una query su tutti i codici di errore correnti o se non si è verificato alcun errore. Se pertanto si ottiene un codice di errore, chiamare **glGetError** fino a quando \_ non \_ viene restituito alcun errore per assicurarsi di aver individuato tutti gli errori. Per l'elenco dei codici di errore, vedere [codici di errore OpenGL](opengl-error-codes.md).

Per ottenere una stringa descrittiva corrispondente al codice di errore passato, è possibile usare la funzione [**gluErrorString**](gluerrorstring.md) Glu. Per ulteriori informazioni su **gluErrorString**, vedere [gestione degli errori](handling-errors.md).

> [!Note]  
> Le funzioni GLU spesso restituiscono valori di errore se viene rilevato un errore. Inoltre, la libreria dell'utilità OpenGL definisce i codici di errore GLU \_ non validi \_ enum, Glu \_ non valido \_ e Glu \_ \_ di \_ memoria insufficiente, che hanno lo stesso significato dei codici di errore OpenGL correlati.

 

 

 




