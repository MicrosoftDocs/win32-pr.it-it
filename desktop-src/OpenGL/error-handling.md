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
# <a name="error-handling-opengl"></a><span data-ttu-id="6e279-105">Gestione degli errori (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="6e279-105">Error Handling (OpenGL)</span></span>

<span data-ttu-id="6e279-106">Quando OpenGL rileva un errore, registra un codice di errore corrente.</span><span class="sxs-lookup"><span data-stu-id="6e279-106">When OpenGL detects an error, it records a current error code.</span></span> <span data-ttu-id="6e279-107">La funzione che ha causato l'errore viene ignorata, quindi non ha alcun effetto sullo stato OpenGL o sul contenuto del framebuffer.</span><span class="sxs-lookup"><span data-stu-id="6e279-107">The function that caused the error is ignored, so it has no effect on the OpenGL state or on the framebuffer contents.</span></span> <span data-ttu-id="6e279-108">(Se l'errore registrato è GL \_ \_ \_ Memoria insufficiente, tuttavia, i risultati della funzione non sono definiti. Una volta registrato, il codice di errore corrente non viene cancellato fino a quando non si chiama la funzione di query [**glGetError**](glgeterror.md) , che restituisce il codice di errore corrente.</span><span class="sxs-lookup"><span data-stu-id="6e279-108">(If the error recorded was GL\_OUT\_OF\_MEMORY, however, the results of the function are undefined.) Once recorded, the current error code isn't cleared until you call the [**glGetError**](glgeterror.md) query function, which returns the current error code.</span></span>

<span data-ttu-id="6e279-109">Le implementazioni di OpenGL possono restituire più codici di errore correnti, ognuno dei quali rimane impostato fino a quando non viene eseguita una query.</span><span class="sxs-lookup"><span data-stu-id="6e279-109">Implementations of OpenGL may return multiple current error codes, each of which remains set until queried.</span></span> <span data-ttu-id="6e279-110">La funzione **glGetError** restituisce GL \_ senza \_ errori dopo aver eseguito una query su tutti i codici di errore correnti o se non si è verificato alcun errore.</span><span class="sxs-lookup"><span data-stu-id="6e279-110">The **glGetError** function returns GL\_NO\_ERROR once you've queried all the current error codes or if there is no error.</span></span> <span data-ttu-id="6e279-111">Se pertanto si ottiene un codice di errore, chiamare **glGetError** fino a quando \_ non \_ viene restituito alcun errore per assicurarsi di aver individuato tutti gli errori.</span><span class="sxs-lookup"><span data-stu-id="6e279-111">Therefore, if you obtain an error code, call **glGetError** until GL\_NO\_ERROR is returned to be sure you've discovered all the errors.</span></span> <span data-ttu-id="6e279-112">Per l'elenco dei codici di errore, vedere [codici di errore OpenGL](opengl-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6e279-112">For the list of error codes, see [OpenGL error codes](opengl-error-codes.md).</span></span>

<span data-ttu-id="6e279-113">Per ottenere una stringa descrittiva corrispondente al codice di errore passato, è possibile usare la funzione [**gluErrorString**](gluerrorstring.md) Glu.</span><span class="sxs-lookup"><span data-stu-id="6e279-113">You can use the [**gluErrorString**](gluerrorstring.md) GLU function to obtain a descriptive string corresponding to the error code passed in.</span></span> <span data-ttu-id="6e279-114">Per ulteriori informazioni su **gluErrorString**, vedere [gestione degli errori](handling-errors.md).</span><span class="sxs-lookup"><span data-stu-id="6e279-114">For more information on **gluErrorString**, see [Handling Errors](handling-errors.md).</span></span>

> [!Note]  
> <span data-ttu-id="6e279-115">Le funzioni GLU spesso restituiscono valori di errore se viene rilevato un errore.</span><span class="sxs-lookup"><span data-stu-id="6e279-115">GLU functions often return error values if an error is detected.</span></span> <span data-ttu-id="6e279-116">Inoltre, la libreria dell'utilità OpenGL definisce i codici di errore GLU \_ non validi \_ enum, Glu \_ non valido \_ e Glu \_ \_ di \_ memoria insufficiente, che hanno lo stesso significato dei codici di errore OpenGL correlati.</span><span class="sxs-lookup"><span data-stu-id="6e279-116">Also, the OpenGL Utility library defines the error codes GLU\_INVALID\_ENUM, GLU\_INVALID\_VALUE, and GLU\_OUT\_OF\_MEMORY, which have the same meaning as the related OpenGL error codes.</span></span>

 

 

 




