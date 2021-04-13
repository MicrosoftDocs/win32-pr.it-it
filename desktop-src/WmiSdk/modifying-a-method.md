---
description: Oltre alle classi e alle istanze, WMI consente di modificare un metodo. Il motivo principale per cui si desidera modificare un metodo è se è stata modificata l'implementazione di un metodo in un provider. Per ulteriori informazioni, vedere scrittura di un provider di metodi.
ms.assetid: 239a994f-ecaf-4558-9626-8f5e60dd350c
ms.tgt_platform: multiple
title: Modifica di un metodo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93009891deec8651599f73f14a73f83bba8ffd4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104401563"
---
# <a name="modifying-a-method"></a><span data-ttu-id="2278f-105">Modifica di un metodo</span><span class="sxs-lookup"><span data-stu-id="2278f-105">Modifying a Method</span></span>

<span data-ttu-id="2278f-106">Oltre alle classi e alle istanze, WMI consente di modificare un metodo.</span><span class="sxs-lookup"><span data-stu-id="2278f-106">In addition to classes and instances, WMI allows you to modify a method.</span></span> <span data-ttu-id="2278f-107">Il motivo principale per cui si desidera modificare un metodo è se è stata modificata l'implementazione di un metodo in un provider.</span><span class="sxs-lookup"><span data-stu-id="2278f-107">The main reason you would want to modify a method is if you changed the implementation of a method in a provider.</span></span> <span data-ttu-id="2278f-108">Per ulteriori informazioni, vedere [scrittura di un provider di metodi](writing-a-method-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2278f-108">For more information, see [Writing a Method Provider](writing-a-method-provider.md).</span></span>

<span data-ttu-id="2278f-109">La modifica di un metodo non è un'operazione che può essere eseguita nello script.</span><span class="sxs-lookup"><span data-stu-id="2278f-109">Modifying a method is not an operation that can be done in script.</span></span>

<span data-ttu-id="2278f-110">Nella procedura riportata di seguito viene descritto come modificare un metodo a livello di codice.</span><span class="sxs-lookup"><span data-stu-id="2278f-110">The following procedure describes how to modify a method programmatically.</span></span>

<span data-ttu-id="2278f-111">**Per modificare un metodo a livello di codice**</span><span class="sxs-lookup"><span data-stu-id="2278f-111">**To modify a method programmatically**</span></span>

1.  <span data-ttu-id="2278f-112">Recuperare la definizione di classe con una chiamata a [**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span><span class="sxs-lookup"><span data-stu-id="2278f-112">Retrieve the class definition with a call to [**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod).</span></span>

    <span data-ttu-id="2278f-113">I due parametri out, *ppInSignature* e *ppOutSignature*, contengono rispettivamente la classe in-Parameter e la classe out-parameter.</span><span class="sxs-lookup"><span data-stu-id="2278f-113">The two out parameters, *ppInSignature* and *ppOutSignature*, contain the in-parameter class and the out-parameter class, respectively.</span></span> <span data-ttu-id="2278f-114">Il valore restituito viene aggregato nella classe del parametro out come proprietà e deve essere denominato **returnValue**.</span><span class="sxs-lookup"><span data-stu-id="2278f-114">The return value is bundled into the out-parameter class as a property, and should be named **ReturnValue**.</span></span>

2.  <span data-ttu-id="2278f-115">Recuperare e modificare i parametri con le chiamate a [**IWbemClassObject:: Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::P UT**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put)o [**IWbemClassObject::D Elimina**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span><span class="sxs-lookup"><span data-stu-id="2278f-115">Retrieve and modify the parameters with calls to [**IWbemClassObject::Get**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-get), [**IWbemClassObject::Put**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-put), or [**IWbemClassObject::Delete**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-delete).</span></span>
3.  <span data-ttu-id="2278f-116">Inserire nuovamente la nuova versione del metodo nella classe padre con una chiamata a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="2278f-116">Place your new version of the method back into the parent class with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="2278f-117">Per ulteriori informazioni, vedere [modifica delle informazioni sulle classi e sulle istanze](manipulating-class-and-instance-information.md).</span><span class="sxs-lookup"><span data-stu-id="2278f-117">For more information, see [Manipulating Class and Instance Information](manipulating-class-and-instance-information.md).</span></span>

 

 



