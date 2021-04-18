---
description: Definisce i parametri di input e output per i metodi.
ms.assetid: d973feb5-27c4-4d8e-bf1b-0a455afa4375
ms.tgt_platform: multiple
title: Classe __PARAMETERS
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __PARAMETERS
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: df858445797a45e21a0d54e9aedc2387851ae54f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313217"
---
# <a name="__parameters-class"></a><span data-ttu-id="5c297-103">\_\_Classe PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c297-103">\_\_PARAMETERS class</span></span>

<span data-ttu-id="5c297-104">La classe di sistema **\_ \_ Parameters** è una classe astratta che definisce i parametri di input e output per i metodi.</span><span class="sxs-lookup"><span data-stu-id="5c297-104">The **\_\_PARAMETERS** system class is an abstract class that defines the input and output parameters for methods.</span></span> <span data-ttu-id="5c297-105">Viene inoltre utilizzato per passare i valori dei parametri di input e di output tra un client WMI e un provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="5c297-105">It is also used to pass input and output parameter values between a WMI client and a method provider.</span></span>

<span data-ttu-id="5c297-106">La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="5c297-106">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="5c297-107">Le proprietà sono elencate in ordine alfabetico e non in ordine MOF.</span><span class="sxs-lookup"><span data-stu-id="5c297-107">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c297-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c297-108">Syntax</span></span>

``` syntax
[abstract]
class __PARAMETERS
{
};
```

## <a name="members"></a><span data-ttu-id="5c297-109">Members</span><span class="sxs-lookup"><span data-stu-id="5c297-109">Members</span></span>

<span data-ttu-id="5c297-110">La classe **\_ \_ Parameters** non definisce membri.</span><span class="sxs-lookup"><span data-stu-id="5c297-110">The **\_\_PARAMETERS** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c297-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c297-111">Remarks</span></span>

<span data-ttu-id="5c297-112">Per definire un metodo in una classe User, un client WMI crea una copia della classe **\_ \_ Parameters** e aggiunge una proprietà per ogni parametro di input in un metodo.</span><span class="sxs-lookup"><span data-stu-id="5c297-112">To define a method in a user class, a WMI client creates a copy of the **\_\_PARAMETERS** class, and adds a property for each input parameter in a method.</span></span> <span data-ttu-id="5c297-113">Se il metodo contiene un valore restituito o parametri di output, è necessario creare un'altra copia dei **\_ \_ parametri** .</span><span class="sxs-lookup"><span data-stu-id="5c297-113">If the method contains a return value or output parameters, another copy of **\_\_PARAMETERS** must be created.</span></span> <span data-ttu-id="5c297-114">Se il metodo restituisce un valore restituito, il client deve aggiungere una proprietà denominata **returnValue**.</span><span class="sxs-lookup"><span data-stu-id="5c297-114">If the method returns a return value, the client must add a property named **ReturnValue**.</span></span> <span data-ttu-id="5c297-115">Il provider di metodi archivia quindi i parametri del metodo con una chiamata a [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="5c297-115">The method provider then stores the method parameters with a call to [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>

<span data-ttu-id="5c297-116">Per richiamare un metodo, un client chiama quanto segue in sequenza:</span><span class="sxs-lookup"><span data-stu-id="5c297-116">To invoke a method, a client calls the following in sequence:</span></span>

1.  <span data-ttu-id="5c297-117">[**IWbemClassObject:: GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) per recuperare una copia della classe **\_ \_ Parameters** archiviata da [**IWbemClassObject::P utmethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span><span class="sxs-lookup"><span data-stu-id="5c297-117">[**IWbemClassObject::GetMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-getmethod) to retrieve a copy of the **\_\_PARAMETERS** class that is stored by [**IWbemClassObject::PutMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-putmethod).</span></span>
2.  <span data-ttu-id="5c297-118">[**IWbemClassObject:: SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), quindi imposta una proprietà per ogni parametro di input per il metodo.</span><span class="sxs-lookup"><span data-stu-id="5c297-118">[**IWbemClassObject::SpawnInstance**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemclassobject-spawninstance), and then sets one property for each input parameter to the method.</span></span>
3.  <span data-ttu-id="5c297-119">[**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) o [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) per eseguire il metodo.</span><span class="sxs-lookup"><span data-stu-id="5c297-119">[**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) or [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync) to execute the method.</span></span>

<span data-ttu-id="5c297-120">Al termine dell'esecuzione del metodo, è possibile che venga restituita un'altra istanza della classe di **\_ \_ parametri** se il metodo ha parametri di output o un valore restituito.</span><span class="sxs-lookup"><span data-stu-id="5c297-120">After the method is finished executing, another **\_\_PARAMETERS** class instance may be returned if the method has output parameters or a return value.</span></span>

-   <span data-ttu-id="5c297-121">Se il metodo è stato richiamato usando [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), l'istanza di **\_ \_ Parameters** viene restituita come argomento di output.</span><span class="sxs-lookup"><span data-stu-id="5c297-121">If the method was invoked by using [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod), the **\_\_PARAMETERS** instance is returned as an output argument.</span></span>
-   <span data-ttu-id="5c297-122">Se il metodo è stato richiamato usando [**IWbemServices:: ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), l'istanza di **\_ \_ Parameters** viene restituita come parametro a [**IWbemObjectSink:: indica**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span><span class="sxs-lookup"><span data-stu-id="5c297-122">If the method was invoked by using [**IWbemServices::ExecMethodAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync), the **\_\_PARAMETERS** instance is returned as a parameter to [**IWbemObjectSink::Indicate**](/windows/desktop/api/Wbemcli/nf-wbemcli-iwbemobjectsink-indicate).</span></span>

## <a name="requirements"></a><span data-ttu-id="5c297-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c297-123">Requirements</span></span>



| <span data-ttu-id="5c297-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c297-124">Requirement</span></span> | <span data-ttu-id="5c297-125">Valore</span><span class="sxs-lookup"><span data-stu-id="5c297-125">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="5c297-126">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c297-126">Minimum supported client</span></span><br/> | <span data-ttu-id="5c297-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c297-127">Windows Vista</span></span><br/>       |
| <span data-ttu-id="5c297-128">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5c297-128">Minimum supported server</span></span><br/> | <span data-ttu-id="5c297-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c297-129">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="5c297-130">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5c297-130">Namespace</span></span><br/>                | <span data-ttu-id="5c297-131">Tutti gli spazi dei nomi WMI</span><span class="sxs-lookup"><span data-stu-id="5c297-131">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="5c297-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c297-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c297-133">Classi di sistema WMI</span><span class="sxs-lookup"><span data-stu-id="5c297-133">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> <dt>

[<span data-ttu-id="5c297-134">**IWbemServices:: ExecMethodAsync**</span><span class="sxs-lookup"><span data-stu-id="5c297-134">**IWbemServices::ExecMethodAsync**</span></span>](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethodasync)
</dt> <dt>

[<span data-ttu-id="5c297-135">Chiamata a un metodo</span><span class="sxs-lookup"><span data-stu-id="5c297-135">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 




