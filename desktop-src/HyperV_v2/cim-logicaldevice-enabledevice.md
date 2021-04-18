---
description: Il metodo EnableDevice è stato deprecato al posto del metodo RequestStateChange più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.
ms.assetid: 1d481417-b640-437d-82ed-d45a9e420d3b
title: Metodo EnableDevice della classe CIM_LogicalDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.EnableDevice
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5a6da7695d7e611223a3a257be23add16094b533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314364"
---
# <a name="enabledevice-method-of-the-cim_logicaldevice-class"></a><span data-ttu-id="f5c16-103">Metodo EnableDevice della classe CIM \_ LogicalDevice</span><span class="sxs-lookup"><span data-stu-id="f5c16-103">EnableDevice method of the CIM\_LogicalDevice class</span></span>

<span data-ttu-id="f5c16-104">Il metodo EnableDevice è stato deprecato al posto del metodo RequestStateChange più generale che si sovrappone direttamente alla funzionalità fornita da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="f5c16-104">The EnableDevice method has been deprecated in lieu of the more general RequestStateChange method that directly overlaps with the functionality provided by this method.</span></span>

<span data-ttu-id="f5c16-105">Richiede l'abilitazione di LogicalDevice ("Enabled" parametro di input = TRUE) o disabilitato (= FALSE).</span><span class="sxs-lookup"><span data-stu-id="f5c16-105">Requests that the LogicalDevice be enabled ("Enabled" input parameter = TRUE) or disabled (= FALSE).</span></span> <span data-ttu-id="f5c16-106">In caso di esito positivo, le proprietà StatusInfo/EnabledState del dispositivo devono riflettere lo stato desiderato (abilitato/disabilitato).</span><span class="sxs-lookup"><span data-stu-id="f5c16-106">If successful, the Device's StatusInfo/EnabledState properties should reflect the desired state (enabled/disabled).</span></span> <span data-ttu-id="f5c16-107">Si noti che la funzione di questo metodo si sovrappone alla proprietà RequestedState.</span><span class="sxs-lookup"><span data-stu-id="f5c16-107">Note that this method's function overlaps with the RequestedState property.</span></span> <span data-ttu-id="f5c16-108">RequestedState è stato aggiunto al modello per mantenere un record (ovvero un valore permanente) dell'ultima richiesta di stato.</span><span class="sxs-lookup"><span data-stu-id="f5c16-108">RequestedState was added to the model to maintain a record (i.e., a persisted value) of the last state request.</span></span> <span data-ttu-id="f5c16-109">Per richiamare il metodo EnableDevice, è necessario impostare la proprietà RequestedState in modo appropriato.</span><span class="sxs-lookup"><span data-stu-id="f5c16-109">Invoking the EnableDevice method should set the RequestedState property appropriately.</span></span>

<span data-ttu-id="f5c16-110">Il codice restituito deve essere 0 se la richiesta è stata eseguita correttamente, 1 se la richiesta non è supportata e un altro valore se si è verificato un errore.</span><span class="sxs-lookup"><span data-stu-id="f5c16-110">The return code should be 0 if the request was successfully executed, 1 if the request is not supported and some other value if an error occurred.</span></span> <span data-ttu-id="f5c16-111">In una sottoclasse è possibile specificare il set di possibili codici restituiti utilizzando un qualificatore ValueMap nel metodo.</span><span class="sxs-lookup"><span data-stu-id="f5c16-111">In a subclass, the set of possible return codes could be specified, using a ValueMap qualifier on the method.</span></span> <span data-ttu-id="f5c16-112">Le stringhe a cui è stato convertito il contenuto ValueMap possono anche essere specificate nella sottoclasse come qualificatore della matrice di valori.</span><span class="sxs-lookup"><span data-stu-id="f5c16-112">The strings to which the ValueMap contents are 'translated' may also be specified in the subclass as a Values array qualifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5c16-113">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f5c16-113">Syntax</span></span>


```mof
uint32 EnableDevice(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="f5c16-114">Parametri</span><span class="sxs-lookup"><span data-stu-id="f5c16-114">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5c16-115">*Abilitato* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f5c16-115">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5c16-116">Se TRUE, Abilita il dispositivo, se FALSE Disabilita il dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5c16-116">If TRUE enable the device, if FALSE disable the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5c16-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f5c16-117">Return value</span></span>

<span data-ttu-id="f5c16-118">Restituisce 0 in caso di esito positivo; in caso contrario, restituisce un errore.</span><span class="sxs-lookup"><span data-stu-id="f5c16-118">Returns a 0 on success; otherwise, returns an error.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c16-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f5c16-119">Requirements</span></span>



| <span data-ttu-id="f5c16-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="f5c16-120">Requirement</span></span> | <span data-ttu-id="f5c16-121">Valore</span><span class="sxs-lookup"><span data-stu-id="f5c16-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5c16-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5c16-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c16-123">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f5c16-123">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f5c16-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f5c16-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c16-125">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f5c16-125">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f5c16-126">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="f5c16-126">Namespace</span></span><br/>                | <span data-ttu-id="f5c16-127">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="f5c16-127">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f5c16-128">MOF</span><span class="sxs-lookup"><span data-stu-id="f5c16-128">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f5c16-129"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f5c16-129"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f5c16-130">DLL</span><span class="sxs-lookup"><span data-stu-id="f5c16-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5c16-131"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f5c16-131"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f5c16-132">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f5c16-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5c16-133">**\_LOGICALDEVICE CIM**</span><span class="sxs-lookup"><span data-stu-id="f5c16-133">**CIM\_LogicalDevice**</span></span>](cim-logicaldevice.md)
</dt> </dl>

 

 




