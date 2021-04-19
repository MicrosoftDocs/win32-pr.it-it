---
description: Richiede che lo stato del componente dell'interfaccia del servizio Guest venga modificato nel valore specificato.
ms.assetid: D9F7CD03-0D86-4005-A600-5CC7082A5047
title: 'Metodo Msvm_GuestServiceInterfaceComponent:: RequestStateChange'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestServiceInterfaceComponent.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: de5689968d44277b01d6cb2256d41ddbbe573cd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311779"
---
# <a name="msvm_guestserviceinterfacecomponentrequeststatechange-method"></a><span data-ttu-id="97cb4-103">\_Metodo MSVM GuestServiceInterfaceComponent:: RequestStateChange</span><span class="sxs-lookup"><span data-stu-id="97cb4-103">Msvm\_GuestServiceInterfaceComponent::RequestStateChange method</span></span>

<span data-ttu-id="97cb4-104">Richiede che lo stato del componente dell'interfaccia del servizio Guest venga modificato nel valore specificato.</span><span class="sxs-lookup"><span data-stu-id="97cb4-104">Requests that the state of the guest service interface component be changed to the specified value.</span></span>

## <a name="syntax"></a><span data-ttu-id="97cb4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="97cb4-105">Syntax</span></span>


```C++
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="97cb4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="97cb4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97cb4-107">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97cb4-107">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97cb4-108">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="97cb4-108">Type: **uint16**</span></span>

<span data-ttu-id="97cb4-109">Nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="97cb4-109">The new state.</span></span> <span data-ttu-id="97cb4-110">Le informazioni vengono inserite nella proprietà **RequestedState** dell'istanza se il codice restituito del metodo **RequestStateChange** è 0 o 4096.</span><span class="sxs-lookup"><span data-stu-id="97cb4-110">The info is placed in the **RequestedState** property of the instance if the return code of the **RequestStateChange** method is 0 or 4096.</span></span> <span data-ttu-id="97cb4-111">Per ulteriori informazioni, vedere la descrizione delle proprietà **EnabledState** e **RequestedState** per l'elemento.</span><span class="sxs-lookup"><span data-stu-id="97cb4-111">For more info, see the description of the **EnabledState** and **RequestedState** properties for the element.</span></span> <span data-ttu-id="97cb4-112">Deve essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="97cb4-112">This must be one of the following values.</span></span>

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="97cb4-113">**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="97cb4-113">**Enabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="97cb4-114">**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="97cb4-114">**Disabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="97cb4-115">**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="97cb4-115">**Shut Down** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="97cb4-116">**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="97cb4-116">**Offline** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="97cb4-117">**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="97cb4-117">**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="97cb4-118">**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="97cb4-118">**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="97cb4-119">**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="97cb4-119">**Quiesce** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="97cb4-120">**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="97cb4-120">**Reboot** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="97cb4-121">**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="97cb4-121">**Reset** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="97cb4-122">**DMTF riservato** (..)</span><span class="sxs-lookup"><span data-stu-id="97cb4-122">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="97cb4-123">**Fornitore riservato** (32768.. 65535)</span><span class="sxs-lookup"><span data-stu-id="97cb4-123">**Vendor Reserved** (32768..65535)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="97cb4-124">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="97cb4-124">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="97cb4-125">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="97cb4-125">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="97cb4-126">Riferimento facoltativo a un oggetto [**MSVM \_ ConcreteJob**](msvm-concretejob.md) restituito se l'operazione viene eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="97cb4-126">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="97cb4-127">Se presente, il riferimento restituito può essere usato per monitorare lo stato di avanzamento e ottenere il risultato del metodo.</span><span class="sxs-lookup"><span data-stu-id="97cb4-127">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="97cb4-128">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="97cb4-128">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97cb4-129">Tipo: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="97cb4-129">Type: **datetime**</span></span>

<span data-ttu-id="97cb4-130">Periodo di timeout che specifica la quantità massima di tempo per cui il client prevede che la transizione al nuovo stato venga eseguita.</span><span class="sxs-lookup"><span data-stu-id="97cb4-130">A timeout period that specifies the maximum amount of time that the client expects the transition to the new state to take.</span></span> <span data-ttu-id="97cb4-131">Per specificare il periodo di timeout, è necessario utilizzare il formato intervallo.</span><span class="sxs-lookup"><span data-stu-id="97cb4-131">The interval format must be used to specify the timeout period.</span></span> <span data-ttu-id="97cb4-132">Il valore 0 o **null** indica che il client non dispone di requisiti temporali per la transizione.</span><span class="sxs-lookup"><span data-stu-id="97cb4-132">A value of 0 or **Null** indicates that the client has no time requirements for the transition.</span></span> <span data-ttu-id="97cb4-133">Se questa proprietà non contiene 0 o **null** e l'implementazione non supporta questo parametro, deve essere restituito un codice restituito 4098 (**utilizzo del parametro timeout non supportato**).</span><span class="sxs-lookup"><span data-stu-id="97cb4-133">If this property does not contain 0 or **Null** and the implementation does not support this parameter, a return code of 4098 (**Use Of Timeout Parameter Not Supported**) must be returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97cb4-134">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="97cb4-134">Return value</span></span>

<span data-ttu-id="97cb4-135">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="97cb4-135">Type: **uint32**</span></span>

<span data-ttu-id="97cb4-136">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="97cb4-136">This method returns one of the following values.</span></span>



| <span data-ttu-id="97cb4-137">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="97cb4-137">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="97cb4-138">Descrizione</span><span class="sxs-lookup"><span data-stu-id="97cb4-138">Description</span></span>         |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|
| <dl> <span data-ttu-id="97cb4-139"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-139"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="97cb4-140">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="97cb4-140">Success.</span></span><br/> |
| <dl> <span data-ttu-id="97cb4-141"><dt>**Non supportato**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-141"><dt>**Not supported**</dt> <dt>1</dt></span></span> </dl>                                     |                     |
| <dl> <span data-ttu-id="97cb4-142"><dt>**Errore sconosciuto/non specificato**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-142"><dt>**Unknown/Unspecified Error**</dt> <dt>2</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="97cb4-143"><dt>**Non può essere completato entro il periodo di timeout**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-143"><dt>**Can NOT complete within Timeout Period**</dt> <dt>3</dt></span></span> </dl>            |                     |
| <dl> <span data-ttu-id="97cb4-144"><dt>**Errore**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-144"><dt>**Failed**</dt> <dt>4</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="97cb4-145"><dt>**Parametro 5 non valido**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-145"><dt>**Invalid Parameter**</dt> <dt>5</dt></span></span> </dl>                                 |                     |
| <dl> <span data-ttu-id="97cb4-146"><dt>**In uso**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-146"><dt>**In Use**</dt> <dt>6</dt></span></span> </dl>                                            |                     |
| <dl> <span data-ttu-id="97cb4-147"><dt>**DMTF riservato**</dt> <dt>..</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-147"><dt>**DMTF Reserved**</dt> <dt>..</dt></span></span> </dl>                                    |                     |
| <dl> <span data-ttu-id="97cb4-148"><dt>**Parametri del metodo controllati-transizione avviata**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-148"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> |                     |
| <dl> <span data-ttu-id="97cb4-149"><dt>**Transizione di stato non valida**</dt> <dt>4097</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-149"><dt>**Invalid State Transition**</dt> <dt>4097</dt></span></span> </dl>                       |                     |
| <dl> <span data-ttu-id="97cb4-150"><dt>**Uso del parametro timeout non supportato**</dt> <dt>4098</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-150"><dt>**Use of Timeout Parameter Not Supported**</dt> <dt>4098</dt></span></span> </dl>         |                     |
| <dl> <span data-ttu-id="97cb4-151"><dt>**Occupato**</dt> <dt>4099</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-151"><dt>**Busy**</dt> <dt>4099</dt></span></span> </dl>                                           |                     |
| <dl> <span data-ttu-id="97cb4-152"><dt>**Metodo riservato**</dt> <dt>4100.. 32767</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-152"><dt>**Method Reserved**</dt> <dt>4100..32767</dt></span></span> </dl>                         |                     |
| <dl> <span data-ttu-id="97cb4-153">32768 <dt>**specifici del fornitore**</dt> <dt>.. 65535</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-153"><dt>**Vendor Specific**</dt> <dt>32768..65535</dt></span></span> </dl>                        |                     |



 

## <a name="requirements"></a><span data-ttu-id="97cb4-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="97cb4-154">Requirements</span></span>



| <span data-ttu-id="97cb4-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="97cb4-155">Requirement</span></span> | <span data-ttu-id="97cb4-156">Valore</span><span class="sxs-lookup"><span data-stu-id="97cb4-156">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97cb4-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97cb4-157">Minimum supported client</span></span><br/> | <span data-ttu-id="97cb4-158">Windows 8.1 \[ solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="97cb4-158">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="97cb4-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="97cb4-159">Minimum supported server</span></span><br/> | <span data-ttu-id="97cb4-160">Solo app desktop Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="97cb4-160">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="97cb4-161">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="97cb4-161">Namespace</span></span><br/>                | <span data-ttu-id="97cb4-162">\\\\\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="97cb4-162">\\\\Root\\Virtualization\\V2</span></span><br/>                                                                 |
| <span data-ttu-id="97cb4-163">MOF</span><span class="sxs-lookup"><span data-stu-id="97cb4-163">MOF</span></span><br/>                      | <dl> <span data-ttu-id="97cb4-164"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-164"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="97cb4-165">DLL</span><span class="sxs-lookup"><span data-stu-id="97cb4-165">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97cb4-166"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="97cb4-166"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="97cb4-167">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="97cb4-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97cb4-168">**\_GuestServiceInterfaceComponent MSVM**</span><span class="sxs-lookup"><span data-stu-id="97cb4-168">**Msvm\_GuestServiceInterfaceComponent**</span></span>](msvm-guestserviceinterfacecomponent.md)
</dt> </dl>

 

