---
description: A differenza dell'eliminazione di un'istanza dinamica, l'eliminazione di una classe è una procedura semplice.
ms.assetid: bc0ee1e8-7515-4f35-ace3-6344c2ef0ab8
ms.tgt_platform: multiple
title: Eliminazione di una classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f3d9ce149b5eff0f5202cb25c5f7d16fdf44291
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315734"
---
# <a name="deleting-a-class"></a><span data-ttu-id="f2a88-103">Eliminazione di una classe</span><span class="sxs-lookup"><span data-stu-id="f2a88-103">Deleting a Class</span></span>

<span data-ttu-id="f2a88-104">A differenza dell'eliminazione di un'istanza dinamica, l'eliminazione di una classe è una procedura semplice.</span><span class="sxs-lookup"><span data-stu-id="f2a88-104">Unlike deleting a dynamic instance, deleting a class is a simple procedure.</span></span> <span data-ttu-id="f2a88-105">Tuttavia, come illustrato in precedenza, le classi base o derivate vengono eliminate raramente.</span><span class="sxs-lookup"><span data-stu-id="f2a88-105">However, as discussed earlier, base or derived classes are rarely deleted.</span></span> <span data-ttu-id="f2a88-106">Un'istanza viene invece eliminata più di frequente.</span><span class="sxs-lookup"><span data-stu-id="f2a88-106">Instead, an instance is more commonly deleted.</span></span> <span data-ttu-id="f2a88-107">L' [API di scripting per WMI](scripting-api-for-wmi.md) utilizza gli stessi metodi per eliminare un oggetto classe o un'istanza di.</span><span class="sxs-lookup"><span data-stu-id="f2a88-107">The [Scripting API for WMI](scripting-api-for-wmi.md) uses the same methods to delete either a class object or an instance.</span></span> <span data-ttu-id="f2a88-108">Per ulteriori informazioni, vedere [eliminazione di un'istanza](deleting-an-instance.md).</span><span class="sxs-lookup"><span data-stu-id="f2a88-108">For more information, see [Deleting an Instance](deleting-an-instance.md).</span></span> <span data-ttu-id="f2a88-109">Per informazioni sulla rimozione di classi e istanze dal repository WMI, vedere il comando per il preprocessore [**pragma deleteclass**](pragma-deleteclass.md) .</span><span class="sxs-lookup"><span data-stu-id="f2a88-109">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="f2a88-110">Per l' [API com per WMI](com-api-for-wmi.md) sono disponibili metodi diversi per l'eliminazione di un'istanza di e l'eliminazione di un oggetto.</span><span class="sxs-lookup"><span data-stu-id="f2a88-110">The [COM API for WMI](com-api-for-wmi.md) has different methods for deleting an instance and deleting an object.</span></span>

<span data-ttu-id="f2a88-111">Nella procedura riportata di seguito viene descritto come eliminare una classe base o una classe derivata.</span><span class="sxs-lookup"><span data-stu-id="f2a88-111">The following procedure describes how to delete a base class or derived class.</span></span>

<span data-ttu-id="f2a88-112">**Per eliminare una classe base o una classe derivata**</span><span class="sxs-lookup"><span data-stu-id="f2a88-112">**To delete a base class or derived class**</span></span>

-   <span data-ttu-id="f2a88-113">Chiamare il metodo [**IWbemServices::D eleteclass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) o [**IWbemServices::D eleteclassasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) .</span><span class="sxs-lookup"><span data-stu-id="f2a88-113">Call either the [**IWbemServices::DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) or [**IWbemServices::DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) method.</span></span>

    <span data-ttu-id="f2a88-114">Come suggerisce il nome, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) Elimina un'istanza in modo asincrono mentre [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) Elimina un'istanza in modo sincrono.</span><span class="sxs-lookup"><span data-stu-id="f2a88-114">As the name suggests, [**DeleteClassAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclassasync) deletes an instance asynchronously while [**DeleteClass**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-deleteclass) deletes an instance synchronously.</span></span> <span data-ttu-id="f2a88-115">Per usare **DeleteClassAsync**, è necessario implementare anche un oggetto [**IWbemObjectSink**](iwbemobjectsink.md) .</span><span class="sxs-lookup"><span data-stu-id="f2a88-115">To use **DeleteClassAsync**, you must also implement an [**IWbemObjectSink**](iwbemobjectsink.md) object.</span></span>

> [!Note]  
> <span data-ttu-id="f2a88-116">Poiché il callback al sink potrebbe non essere restituito allo stesso livello di autenticazione richiesto dal client, è consigliabile utilizzare semisincrono anziché la comunicazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="f2a88-116">Because the callback to the sink might not be returned at the same authentication level as the client requires, it is recommended that you use semisynchronous instead of asynchronous communication.</span></span> <span data-ttu-id="f2a88-117">Per ulteriori informazioni, vedere [chiamata a un metodo](calling-a-method.md).</span><span class="sxs-lookup"><span data-stu-id="f2a88-117">For more information, see [Calling a Method](calling-a-method.md).</span></span>

 

 

 



