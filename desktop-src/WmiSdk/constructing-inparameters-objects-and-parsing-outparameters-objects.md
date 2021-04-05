---
description: In genere, l'accesso diretto è adeguato per chiamare un metodo del provider WMI.
ms.assetid: be9332b5-8094-44a2-8632-af9957ecf36b
ms.tgt_platform: multiple
title: Creazione di oggetti InParameters e analisi di oggetti OutParameters
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a291d4fd44e69e87572684856bba587685e1f07b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103967973"
---
# <a name="constructing-inparameters-objects-and-parsing-outparameters-objects"></a><span data-ttu-id="ef81b-103">Creazione di oggetti InParameters e analisi di oggetti OutParameters</span><span class="sxs-lookup"><span data-stu-id="ef81b-103">Constructing InParameters Objects and Parsing OutParameters Objects</span></span>

<span data-ttu-id="ef81b-104">In genere, l'accesso diretto è adeguato per chiamare un [*metodo del provider*](gloss-p.md)WMI.</span><span class="sxs-lookup"><span data-stu-id="ef81b-104">Normally, direct access is adequate to call a WMI [*provider method*](gloss-p.md).</span></span> <span data-ttu-id="ef81b-105">L'accesso diretto comporta l'esecuzione di un metodo tramite la sintassi *Object. Method* .</span><span class="sxs-lookup"><span data-stu-id="ef81b-105">Direct access means executing a method by using *object.method* syntax.</span></span> <span data-ttu-id="ef81b-106">In alcuni casi, tuttavia, non è possibile usare l'accesso diretto.</span><span class="sxs-lookup"><span data-stu-id="ef81b-106">However, in some cases, direct access cannot be used.</span></span> <span data-ttu-id="ef81b-107">Inoltre, la chiamata asincrona di un metodo del provider da uno script richiede un tipo di chiamata [**ExecMethodAsync**](swbemobject-execmethodasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="ef81b-107">Also, calling a provider method asynchronously from a script requires an [**ExecMethodAsync**](swbemobject-execmethodasync-.md) type of call.</span></span>

> [!Note]  
> <span data-ttu-id="ef81b-108">Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="ef81b-108">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="ef81b-109">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="ef81b-109">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="ef81b-110">L'ordine dei parametri di input e output del metodo viene definito nello schema Managed Object Format (MOF) per il metodo.</span><span class="sxs-lookup"><span data-stu-id="ef81b-110">The order of method input and output parameters is defined in the Managed Object Format (MOF) schema for the method.</span></span> <span data-ttu-id="ef81b-111">WMI non impedisce la modifica dell'ordine dei parametri quando la classe viene ricompilata da [mofcomp](mofcomp.md).</span><span class="sxs-lookup"><span data-stu-id="ef81b-111">WMI does not prevent the parameter order from being changed when the class is recompiled by [mofcomp](mofcomp.md).</span></span> <span data-ttu-id="ef81b-112">Utilizzando un oggetto [**InParameters**](swbemmethod-inparameters.md) , è possibile evitare problemi causati dallo schema modificato perché i parametri di input sono identificati in base al nome.</span><span class="sxs-lookup"><span data-stu-id="ef81b-112">By using an [**InParameters**](swbemmethod-inparameters.md) object, you can avoid problems that result from changed schema because the input parameters are identified by name.</span></span> <span data-ttu-id="ef81b-113">Il parametro corretto può essere visualizzato esaminando il qualificatore **ID** di ogni parametro di input.</span><span class="sxs-lookup"><span data-stu-id="ef81b-113">The correct parameter can be seen by examining the **ID** qualifier of each input parameter.</span></span> <span data-ttu-id="ef81b-114">Il primo parametro ha un valore **ID** pari a 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="ef81b-114">The first parameter has an **ID** value of 0 (zero).</span></span>

<span data-ttu-id="ef81b-115">[**I metodi SWbemObject.Exe\_ cMethod**](swbemobject-execmethod-.md), [**SWbemObject.Exe\_ cMethodAsync**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)e [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) forniscono una modalità alternativa per eseguire un metodo del provider nei casi in cui non è possibile eseguire direttamente un metodo.</span><span class="sxs-lookup"><span data-stu-id="ef81b-115">[**The SWbemObject.ExecMethod\_**](swbemobject-execmethod-.md), [**SWbemObject.ExecMethodAsync\_**](swbemobject-execmethodasync-.md), [**SWbemServices.ExecMethod**](swbemservices-execmethod.md), and [**SWbemServices.ExecMethodAsync**](swbemservices-execmethodasync.md) methods provide an alternate way to execute a provider method in cases where it is not possible to execute a method directly.</span></span> <span data-ttu-id="ef81b-116">Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="ef81b-116">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

<span data-ttu-id="ef81b-117">Per altre informazioni sui parametri, vedere [creazione di oggetti InParameters](constructing-inparameters-objects.md) e [analisi di oggetti OutParameters](parsing-outparameters-objects.md).</span><span class="sxs-lookup"><span data-stu-id="ef81b-117">For more information about parameters, see [Constructing InParameters Objects](constructing-inparameters-objects.md) and [Parsing OutParameters Objects](parsing-outparameters-objects.md).</span></span>

 

 



