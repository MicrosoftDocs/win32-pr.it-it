---
title: Utilizzo dei metodi di callback
description: Utilizzo dei metodi di callback
ms.assetid: 098cb90b-8c21-4692-a4f9-bacce042520a
keywords:
- Windows Media Format SDK, metodi di callback
- Windows Media Format SDK, metodi chiamati in modo asincrono
- metodi di callback
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d39201c101c9031a7157f79f6c12ec88f07decfc
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/19/2020
ms.locfileid: "103723415"
---
# <a name="using-the-callback-methods"></a><span data-ttu-id="43277-106">Utilizzo dei metodi di callback</span><span class="sxs-lookup"><span data-stu-id="43277-106">Using the Callback Methods</span></span>

<span data-ttu-id="43277-107">Diverse interfacce in Windows Media Format SDK contengono metodi che vengono chiamati in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="43277-107">Several interfaces in the Windows Media Format SDK contain methods that are called asynchronously.</span></span> <span data-ttu-id="43277-108">La maggior parte di questi metodi usa funzioni di callback per passare informazioni all'applicazione di controllo.</span><span class="sxs-lookup"><span data-stu-id="43277-108">Most of these methods use callback functions to pass information to the controlling application.</span></span>

<span data-ttu-id="43277-109">Nelle sezioni seguenti vengono descritti alcuni problemi generali relativi all'utilizzo di metodi di callback con Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="43277-109">The following sections describe some of the general issues regarding the use of callback methods with the Windows Media Format SDK.</span></span>



| <span data-ttu-id="43277-110">Sezione</span><span class="sxs-lookup"><span data-stu-id="43277-110">Section</span></span>                                                                          | <span data-ttu-id="43277-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="43277-111">Description</span></span>                                                                                                                                                                                          |
|----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43277-112">Uso del callback di OnStatus</span><span class="sxs-lookup"><span data-stu-id="43277-112">Using the OnStatus Callback</span></span>](using-the-onstatus-callback.md)                   | <span data-ttu-id="43277-113">Viene descritto come implementare il metodo di callback [**IWMStatusCallback:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) , utilizzato da diversi oggetti per consigliare l'avanzamento dell'operazione dell'SDK.</span><span class="sxs-lookup"><span data-stu-id="43277-113">Describes how to implement the [**IWMStatusCallback::OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) callback method, which is used by several objects to advise applications of SDK operation progress.</span></span> |
| [<span data-ttu-id="43277-114">Uso di eventi con chiamate asincrone</span><span class="sxs-lookup"><span data-stu-id="43277-114">Using Events with Asynchronous Calls</span></span>](using-events-with-asynchronous-calls.md) | <span data-ttu-id="43277-115">Viene descritta una tecnica comune per gestire le chiamate asincrone al metodo in un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="43277-115">Describes a common technique to handle asynchronous method calls in an application.</span></span>                                                                                                                  |
| [<span data-ttu-id="43277-116">Uso del parametro di contesto</span><span class="sxs-lookup"><span data-stu-id="43277-116">Using the Context Parameter</span></span>](using-the-context-parameter.md)                   | <span data-ttu-id="43277-117">Introduce il parametro *pvContext* , condiviso da diversi callback e i relativi metodi di chiamata, e spiega come usarlo.</span><span class="sxs-lookup"><span data-stu-id="43277-117">Introduces the *pvContext* parameter, shared by several callbacks and their calling methods, and explains how to use it.</span></span>                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="43277-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="43277-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43277-119">**Guida per programmatori**</span><span class="sxs-lookup"><span data-stu-id="43277-119">**Programming Guide**</span></span>](programming-guide.md)
</dt> </dl>

 

 




