---
description: L'eliminazione di un'istanza è il comando Delete più comune che è probabile eseguire in WMI.
ms.assetid: 95ba3e9c-1397-41fe-a080-c03a98aafd42
ms.tgt_platform: multiple
title: Eliminazione di un'istanza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2229889ec4bc21ad234eb1636f264977bb3e25e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310382"
---
# <a name="deleting-an-instance"></a><span data-ttu-id="45d5f-103">Eliminazione di un'istanza</span><span class="sxs-lookup"><span data-stu-id="45d5f-103">Deleting an Instance</span></span>

<span data-ttu-id="45d5f-104">L'eliminazione di un'istanza è il comando Delete più comune che è probabile eseguire in WMI.</span><span class="sxs-lookup"><span data-stu-id="45d5f-104">Deleting an instance is the most common delete command you are likely to perform in WMI.</span></span> <span data-ttu-id="45d5f-105">Come l'eliminazione di una classe, il comando effettivo è piuttosto semplice.</span><span class="sxs-lookup"><span data-stu-id="45d5f-105">Like deleting a class, the actual command is fairly simple.</span></span> <span data-ttu-id="45d5f-106">Tuttavia, WMI viene eseguito in modo molto diverso a seconda del tipo di istanza che si desidera eliminare.</span><span class="sxs-lookup"><span data-stu-id="45d5f-106">However, WMI performs quite differently depending on the type of instance you are deleting.</span></span> <span data-ttu-id="45d5f-107">Se l'istanza è statica, WMI Elimina semplicemente l'istanza dal repository WMI.</span><span class="sxs-lookup"><span data-stu-id="45d5f-107">If the instance is static, WMI simply deletes the instance from the WMI repository.</span></span> <span data-ttu-id="45d5f-108">Per informazioni sulla rimozione di classi e istanze dal repository WMI, vedere il comando per il preprocessore [**pragma deleteclass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="45d5f-108">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="45d5f-109">Se l'istanza è dinamica, WMI deve chiamare [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) nei provider responsabili delle classi seguenti:</span><span class="sxs-lookup"><span data-stu-id="45d5f-109">If the instance is dynamic, WMI must call [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) on the providers that are responsible for the following classes:</span></span>

-   <span data-ttu-id="45d5f-110">Classe proprietaria dell'istanza di.</span><span class="sxs-lookup"><span data-stu-id="45d5f-110">The class that owns the instance.</span></span>
-   <span data-ttu-id="45d5f-111">Ogni classe padre della classe proprietaria dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="45d5f-111">Every parent class of the class that owns the instance.</span></span>
-   <span data-ttu-id="45d5f-112">Ogni sottoclasse della classe proprietaria dell'istanza.</span><span class="sxs-lookup"><span data-stu-id="45d5f-112">Every subclass of the class that owns the instance.</span></span>

<span data-ttu-id="45d5f-113">Il completamento dell'eliminazione dipende dalla classe non astratta più grande per l'istanza originale.</span><span class="sxs-lookup"><span data-stu-id="45d5f-113">The success of the deletion depends on the topmost nonabstract class for the original instance.</span></span> <span data-ttu-id="45d5f-114">Se il provider di una classe non astratta più in alto riesce a completare l'eliminazione, l'operazione ha esito positivo.</span><span class="sxs-lookup"><span data-stu-id="45d5f-114">If the provider for any topmost nonabstract class succeeds in completing the deletion, the operation succeeds.</span></span> <span data-ttu-id="45d5f-115">Per ulteriori informazioni, vedere la sezione Osservazioni di [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span><span class="sxs-lookup"><span data-stu-id="45d5f-115">For more information, see the Remarks section of [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance).</span></span>

<span data-ttu-id="45d5f-116">Per l' [API com per WMI](com-api-for-wmi.md) sono disponibili metodi diversi per l'eliminazione di un'istanza di e l'eliminazione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="45d5f-116">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="45d5f-117">Nella procedura seguente viene descritto come utilizzare C++ per eliminare un'istanza di una classe di base o di una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="45d5f-117">The following procedure describes how to use C++ to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="45d5f-118">**Per eliminare un'istanza di una classe base o di una classe derivata mediante C++**</span><span class="sxs-lookup"><span data-stu-id="45d5f-118">**To delete an instance of a base class or derived class using C++**</span></span>

-   <span data-ttu-id="45d5f-119">Chiamare i metodi [**IWbemServices::D eleteinstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) o [**IWbemServices::D eleteinstanceasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) .</span><span class="sxs-lookup"><span data-stu-id="45d5f-119">Call either the [**IWbemServices::DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) or [**IWbemServices::DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) methods.</span></span>

    <span data-ttu-id="45d5f-120">Come suggerisce il nome, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) Elimina un'istanza in modo asincrono mentre [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) Elimina un'istanza in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="45d5f-120">As the name suggests, [**DeleteInstanceAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstanceasync) deletes an instance asynchronously while [**DeleteInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteinstance) deletes an instance synchronously.</span></span> <span data-ttu-id="45d5f-121">Per usare **DeleteInstanceAsync**, è necessario implementare anche un oggetto [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="45d5f-121">To use **DeleteInstanceAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="45d5f-122">Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="45d5f-122">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="45d5f-123">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="45d5f-123">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

<span data-ttu-id="45d5f-124">L' [API di scripting per WMI](scripting-api-for-wmi.md) utilizza gli stessi metodi per eliminare un oggetto classe o un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="45d5f-124">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span>

<span data-ttu-id="45d5f-125">Nella procedura seguente viene descritto come utilizzare VBScript per eliminare un'istanza di una classe di base o di una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="45d5f-125">The following procedure describes how to use VBScript to delete an instance of a base class or derived class.</span></span>

<span data-ttu-id="45d5f-126">**Per eliminare un'istanza di una classe base o di una classe derivata tramite VBScript**</span><span class="sxs-lookup"><span data-stu-id="45d5f-126">**To delete an instance of a base class or derived class using VBScript**</span></span>

-   <span data-ttu-id="45d5f-127">Chiamare i metodi [**SWbemObject. Delete \_**](swbemobject-delete-.md) o [**SWbemObject. DeleteAsync \_**](swbemobject-deleteasync-.md) .</span><span class="sxs-lookup"><span data-stu-id="45d5f-127">Call either the [**SWbemObject.Delete\_**](swbemobject-delete-.md) or [**SWbemObject.DeleteAsync\_**](swbemobject-deleteasync-.md) methods.</span></span>

    <span data-ttu-id="45d5f-128">Come suggerisce il nome, [**Delete \_**](swbemobject-delete-.md) Elimina un'istanza in modo sincrono mentre [**DeleteAsync \_**](swbemobject-deleteasync-.md) Elimina un'istanza in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="45d5f-128">As the name suggests, [**Delete\_**](swbemobject-delete-.md) deletes an instance synchronously while [**DeleteAsync\_**](swbemobject-deleteasync-.md) deletes an instance asynchronously.</span></span> <span data-ttu-id="45d5f-129">Per ulteriori informazioni sull'eliminazione di un'istanza in modo asincrono, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="45d5f-129">For more information about deleting an instance asynchronously, see [Calling a Method](calling-a-method.md).</span></span>

    <span data-ttu-id="45d5f-130">Nell'esempio seguente viene descritto come eliminare un'istanza di utilizzando VBScript.</span><span class="sxs-lookup"><span data-stu-id="45d5f-130">The following example describes how to delete an instance using VBScript.</span></span>

    ```VB
    Dim service

    Set service = GetObject("winmgmts:{impersonationLevel=impersonate}") 

    Set objwbemobject= service.get("")

    objwbemobject.Path_.Class = "MyNewClass" 
    objwbemobject.put_
    service.delete  "MyNewClass"
    ```

    

> [!Note]  
> <span data-ttu-id="45d5f-131">Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="45d5f-131">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="45d5f-132">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="45d5f-132">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



