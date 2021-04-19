---
description: Il mapper di invio viene creato utilizzando COM CoCreateInstance ed espone un'interfaccia, ITDispatchMapper.
ms.assetid: 435034e1-d90c-4bad-8758-8a627d88875f
title: Mapper di invio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ed0a3a6cbc906861f5e95694bfd75aec6f5791f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311902"
---
# <a name="dispatch-mapper"></a><span data-ttu-id="b5e0e-103">Mapper di invio</span><span class="sxs-lookup"><span data-stu-id="b5e0e-103">Dispatch Mapper</span></span>

<span data-ttu-id="b5e0e-104">Il mapper di invio viene creato utilizzando COM **CoCreateInstance** ed espone un'interfaccia, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper).</span><span class="sxs-lookup"><span data-stu-id="b5e0e-104">The Dispatch Mapper is created using COM **CoCreateInstance** and exposes one interface, [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper).</span></span> <span data-ttu-id="b5e0e-105">Questa interfaccia consente a un'applicazione di recuperare il puntatore di invio di un'altra interfaccia su un oggetto, dato il puntatore di invio di un'interfaccia e il GUID di un altro.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-105">This interface allows an application to retrieve the dispatch pointer of another interface on an object, given the dispatch pointer of one interface and the GUID of another.</span></span> <span data-ttu-id="b5e0e-106">Questa interfaccia viene fornita per aiutare i programmatori che utilizzano applicazioni di scripting che non consentono di eseguire immediatamente il polling delle interfacce in un oggetto.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-106">This interface is provided to assist programmers using scripting applications which do not provide a means of readily polling the interfaces on an object.</span></span>

<span data-ttu-id="b5e0e-107">Il mapper di invio utilizza l'interfaccia **IObjectSafety** di un oggetto per assicurarsi che l'oggetto sia sicuro per l'esecuzione di script sull'interfaccia richiesta.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-107">The Dispatch Mapper uses an object's **IObjectSafety** interface to make sure the object is safe for scripting on the requested interface.</span></span> <span data-ttu-id="b5e0e-108">Se l'oggetto non implementa **IObjectSafety** o se l'oggetto non è sicuro su questa interfaccia particolare, la chiamata avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="b5e0e-108">If the object does not implement **IObjectSafety**, or if the object is not safe on this particular interface, the call will fail.</span></span>

 

 



