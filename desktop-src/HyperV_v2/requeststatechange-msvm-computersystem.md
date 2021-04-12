---
description: Richiede che lo stato della macchina virtuale venga modificato in un valore specificato.
ms.assetid: 87BE4C7D-604B-4F8D-B4DC-89BD563E3999
title: Metodo RequestStateChange della classe Msvm_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ComputerSystem.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 291d72797b1ee765507a3d23921cd518cf605354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234359"
---
# <a name="requeststatechange-method-of-the-msvm_computersystem-class"></a><span data-ttu-id="a059a-103">Metodo RequestStateChange della classe MSVM \_ ComputerSystem</span><span class="sxs-lookup"><span data-stu-id="a059a-103">RequestStateChange method of the Msvm\_ComputerSystem class</span></span>

<span data-ttu-id="a059a-104">Richiede che lo stato della macchina virtuale venga modificato in un valore specificato.</span><span class="sxs-lookup"><span data-stu-id="a059a-104">Requests that the state of the virtual machine be changed to the specified value.</span></span> <span data-ttu-id="a059a-105">Richiamando il metodo **RequestStateChange** più volte, le richieste precedenti potrebbero essere sovrascritte o perse.</span><span class="sxs-lookup"><span data-stu-id="a059a-105">Invoking the **RequestStateChange** method multiple times could result in earlier requests being overwritten or lost.</span></span> <span data-ttu-id="a059a-106">Questo metodo è supportato solo per le istanze della classe [**MSVM \_ ComputerSystem**](msvm-computersystem.md) che rappresentano una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a059a-106">This method is only supported for instances of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represent a virtual machine.</span></span>

<span data-ttu-id="a059a-107">Mentre è in corso la modifica dello stato, la proprietà **RequestedState** viene modificata nel valore del parametro *RequestedState* .</span><span class="sxs-lookup"><span data-stu-id="a059a-107">While the state change is in progress, the **RequestedState** property is changed to the value of the *RequestedState* parameter.</span></span>

## <a name="syntax"></a><span data-ttu-id="a059a-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a059a-108">Syntax</span></span>


```mof
uint32 RequestStateChange(
  [in]  uint16              RequestedState,
  [out] CIM_ConcreteJob REF Job,
  [in]  datetime            TimeoutPeriod
);
```



## <a name="parameters"></a><span data-ttu-id="a059a-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="a059a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a059a-110">*RequestedState* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a059a-110">*RequestedState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a059a-111">Tipo: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="a059a-111">Type: **uint16**</span></span>

<span data-ttu-id="a059a-112">Nuovo stato.</span><span class="sxs-lookup"><span data-stu-id="a059a-112">The new state.</span></span> <span data-ttu-id="a059a-113">I valori maggiori di 32767 sono valori **DMTF** proposti e sono soggetti a modifiche.</span><span class="sxs-lookup"><span data-stu-id="a059a-113">Values that are greater than 32767 are **DMTF** proposed values and are subject to change.</span></span>

<span data-ttu-id="a059a-114">I valori possibili sono i seguenti:</span><span class="sxs-lookup"><span data-stu-id="a059a-114">Here are possible values:</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="a059a-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Altro** (1)</span><span class="sxs-lookup"><span data-stu-id="a059a-115"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-116">Corrisponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = other.</span><span class="sxs-lookup"><span data-stu-id="a059a-116">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Other.</span></span>

</dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="a059a-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Abilitato** (2)</span><span class="sxs-lookup"><span data-stu-id="a059a-117"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (2)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-118">Corrisponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled.</span><span class="sxs-lookup"><span data-stu-id="a059a-118">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled.</span></span>

</dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="a059a-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabilitato** (3)</span><span class="sxs-lookup"><span data-stu-id="a059a-119"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-120">Corrisponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = disabled.</span><span class="sxs-lookup"><span data-stu-id="a059a-120">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Disabled.</span></span>

</dd> <dt>

<span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>

<span data-ttu-id="a059a-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Arresto** (4)</span><span class="sxs-lookup"><span data-stu-id="a059a-121"><span id="Shut_Down"></span><span id="shut_down"></span><span id="SHUT_DOWN"></span>**Shut Down** (4)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-122">Valido solo nella versione 1 (V1) di Hyper-V.</span><span class="sxs-lookup"><span data-stu-id="a059a-122">Valid in version 1 (V1) of Hyper-V only.</span></span> <span data-ttu-id="a059a-123">La macchina virtuale verrà arrestata tramite il servizio di arresto.</span><span class="sxs-lookup"><span data-stu-id="a059a-123">The virtual machine is shutting down via the shutdown service.</span></span> <span data-ttu-id="a059a-124">Corrisponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown.</span><span class="sxs-lookup"><span data-stu-id="a059a-124">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = ShuttingDown.</span></span>

</dd> <dt>

<span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>

<span data-ttu-id="a059a-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span><span class="sxs-lookup"><span data-stu-id="a059a-125"><span id="Offline"></span><span id="offline"></span><span id="OFFLINE"></span>**Offline** (6)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-126">Corrisponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled ma offline.</span><span class="sxs-lookup"><span data-stu-id="a059a-126">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Enabled but offline.</span></span>

</dd> <dt>

<span id="Test"></span><span id="test"></span><span id="TEST"></span>

<span data-ttu-id="a059a-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span><span class="sxs-lookup"><span data-stu-id="a059a-127"><span id="Test"></span><span id="test"></span><span id="TEST"></span>**Test** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>

<span data-ttu-id="a059a-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Rinvia** (8)</span><span class="sxs-lookup"><span data-stu-id="a059a-128"><span id="Defer"></span><span id="defer"></span><span id="DEFER"></span>**Defer** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>

<span data-ttu-id="a059a-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Mettere in stato** (9)</span><span class="sxs-lookup"><span data-stu-id="a059a-129"><span id="Quiesce"></span><span id="quiesce"></span><span id="QUIESCE"></span>**Quiesce** (9)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-130">Corrisponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = mettere in stato, abilitato ma sospeso.</span><span class="sxs-lookup"><span data-stu-id="a059a-130">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Quiesce, Enabled but paused.</span></span>

</dd> <dt>

<span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>

<span data-ttu-id="a059a-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Riavvio** (10)</span><span class="sxs-lookup"><span data-stu-id="a059a-131"><span id="Reboot"></span><span id="reboot"></span><span id="REBOOT"></span>**Reboot** (10)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-132">Transizione di stato da **disattivata** o **salvata** in **esecuzione**.</span><span class="sxs-lookup"><span data-stu-id="a059a-132">State transition from **Off** or **Saved** to **Running**.</span></span>

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span data-ttu-id="a059a-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reimposta** (11)</span><span class="sxs-lookup"><span data-stu-id="a059a-133"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Reset** (11)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-134">Ripristinare la macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a059a-134">Reset the virtual machine.</span></span> <span data-ttu-id="a059a-135">Corrisponde a [**CIM \_ EnabledLogicalElement. EnabledState**](/previous-versions//cc136818(v=vs.85)) = reset.</span><span class="sxs-lookup"><span data-stu-id="a059a-135">Corresponds to [**CIM\_EnabledLogicalElement.EnabledState**](/previous-versions//cc136818(v=vs.85)) = Reset.</span></span>

</dd> <dt>

<span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>

<span data-ttu-id="a059a-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Salvataggio** (32773)</span><span class="sxs-lookup"><span data-stu-id="a059a-136"><span id="Saving"></span><span id="saving"></span><span id="SAVING"></span>**Saving** (32773)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-137">Nella versione 1 (V1) di Hyper-V corrisponde a **EnabledStateSaving**.</span><span class="sxs-lookup"><span data-stu-id="a059a-137">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateSaving**.</span></span>

</dd> <dt>

<span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>

<span data-ttu-id="a059a-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Sospensione** (32776)</span><span class="sxs-lookup"><span data-stu-id="a059a-138"><span id="Pausing"></span><span id="pausing"></span><span id="PAUSING"></span>**Pausing** (32776)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-139">Nella versione 1 (V1) di Hyper-V corrisponde a **EnabledStatePausing**.</span><span class="sxs-lookup"><span data-stu-id="a059a-139">In version 1 (V1) of Hyper-V, corresponds to **EnabledStatePausing**.</span></span>

</dd> <dt>

<span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>

<span data-ttu-id="a059a-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Ripresa** in (32777)</span><span class="sxs-lookup"><span data-stu-id="a059a-140"><span id="Resuming"></span><span id="resuming"></span><span id="RESUMING"></span>**Resuming** (32777)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-141">Nella versione 1 (V1) di Hyper-V corrisponde a **EnabledStateResuming**.</span><span class="sxs-lookup"><span data-stu-id="a059a-141">In version 1 (V1) of Hyper-V, corresponds to **EnabledStateResuming**.</span></span> <span data-ttu-id="a059a-142">Transizione di stato da **sospesa** a **in esecuzione**.</span><span class="sxs-lookup"><span data-stu-id="a059a-142">State transition from **Paused** to **Running**.</span></span>

</dd> <dt>

<span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>

<span data-ttu-id="a059a-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779)</span><span class="sxs-lookup"><span data-stu-id="a059a-143"><span id="FastSaved"></span><span id="fastsaved"></span><span id="FASTSAVED"></span>**FastSaved** (32779)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-144">Corrisponde a **EnabledStateFastSuspend**.</span><span class="sxs-lookup"><span data-stu-id="a059a-144">Corresponds to **EnabledStateFastSuspend**.</span></span>

</dd> <dt>

<span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>

<span data-ttu-id="a059a-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780)</span><span class="sxs-lookup"><span data-stu-id="a059a-145"><span id="FastSaving"></span><span id="fastsaving"></span><span id="FASTSAVING"></span>**FastSaving** (32780)</span></span>


</dt> <dd>

<span data-ttu-id="a059a-146">Corrisponde a **EnabledStateFastSuspending**.</span><span class="sxs-lookup"><span data-stu-id="a059a-146">Corresponds to **EnabledStateFastSuspending**.</span></span> <span data-ttu-id="a059a-147">Transizione di stato dall' **esecuzione** a **FastSaved**.</span><span class="sxs-lookup"><span data-stu-id="a059a-147">State transition from **Running** to **FastSaved**.</span></span>

</dd> </dl>

<span data-ttu-id="a059a-148">Questi valori rappresentano stati critici:</span><span class="sxs-lookup"><span data-stu-id="a059a-148">These values represent critical states:</span></span>

<dt>

<span id="RunningCritical"></span><span id="runningcritical"></span><span id="RUNNINGCRITICAL"></span>

<span data-ttu-id="a059a-149">**RunningCritical** (32781)</span><span class="sxs-lookup"><span data-stu-id="a059a-149">**RunningCritical** (32781)</span></span>


</dt> <dd></dd> <dt>

<span id="OffCritical"></span><span id="offcritical"></span><span id="OFFCRITICAL"></span>

<span data-ttu-id="a059a-150">**OffCritical** (32782)</span><span class="sxs-lookup"><span data-stu-id="a059a-150">**OffCritical** (32782)</span></span>


</dt> <dd></dd> <dt>

<span id="StoppingCritical"></span><span id="stoppingcritical"></span><span id="STOPPINGCRITICAL"></span>

<span data-ttu-id="a059a-151">**StoppingCritical** (32783)</span><span class="sxs-lookup"><span data-stu-id="a059a-151">**StoppingCritical** (32783)</span></span>


</dt> <dd></dd> <dt>

<span id="SavedCritical"></span><span id="savedcritical"></span><span id="SAVEDCRITICAL"></span>

<span data-ttu-id="a059a-152">**SavedCritical** (32784)</span><span class="sxs-lookup"><span data-stu-id="a059a-152">**SavedCritical** (32784)</span></span>


</dt> <dd></dd> <dt>

<span id="PausedCritical"></span><span id="pausedcritical"></span><span id="PAUSEDCRITICAL"></span>

<span data-ttu-id="a059a-153">**PausedCritical** (32785)</span><span class="sxs-lookup"><span data-stu-id="a059a-153">**PausedCritical** (32785)</span></span>


</dt> <dd></dd> <dt>

<span id="StartingCritical"></span><span id="startingcritical"></span><span id="STARTINGCRITICAL"></span>

<span data-ttu-id="a059a-154">**StartingCritical** (32786)</span><span class="sxs-lookup"><span data-stu-id="a059a-154">**StartingCritical** (32786)</span></span>


</dt> <dd></dd> <dt>

<span id="ResetCritical"></span><span id="resetcritical"></span><span id="RESETCRITICAL"></span>

<span data-ttu-id="a059a-155">**ResetCritical** (32787)</span><span class="sxs-lookup"><span data-stu-id="a059a-155">**ResetCritical** (32787)</span></span>


</dt> <dd></dd> <dt>

<span id="SavingCritical"></span><span id="savingcritical"></span><span id="SAVINGCRITICAL"></span>

<span data-ttu-id="a059a-156">**SavingCritical** (32788)</span><span class="sxs-lookup"><span data-stu-id="a059a-156">**SavingCritical** (32788)</span></span>


</dt> <dd></dd> <dt>

<span id="PausingCritical"></span><span id="pausingcritical"></span><span id="PAUSINGCRITICAL"></span>

<span data-ttu-id="a059a-157">**PausingCritical** (32789)</span><span class="sxs-lookup"><span data-stu-id="a059a-157">**PausingCritical** (32789)</span></span>


</dt> <dd></dd> <dt>

<span id="ResumingCritical"></span><span id="resumingcritical"></span><span id="RESUMINGCRITICAL"></span>

<span data-ttu-id="a059a-158">**ResumingCritical** (32790)</span><span class="sxs-lookup"><span data-stu-id="a059a-158">**ResumingCritical** (32790)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavedCritical"></span><span id="fastsavedcritical"></span><span id="FASTSAVEDCRITICAL"></span>

<span data-ttu-id="a059a-159">**FastSavedCritical** (32791)</span><span class="sxs-lookup"><span data-stu-id="a059a-159">**FastSavedCritical** (32791)</span></span>


</dt> <dd></dd> <dt>

<span id="FastSavingCritical"></span><span id="fastsavingcritical"></span><span id="FASTSAVINGCRITICAL"></span>

<span data-ttu-id="a059a-160">**FastSavingCritical** (32792)</span><span class="sxs-lookup"><span data-stu-id="a059a-160">**FastSavingCritical** (32792)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="a059a-161">*Processo* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="a059a-161">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a059a-162">Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="a059a-162">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="a059a-163">Riferimento facoltativo a un oggetto [**MSVM \_ ConcreteJob**](msvm-concretejob.md) restituito se l'operazione viene eseguita in modo asincrono.</span><span class="sxs-lookup"><span data-stu-id="a059a-163">An optional reference to a [**Msvm\_ConcreteJob**](msvm-concretejob.md) object that is returned if the operation is executed asynchronously.</span></span> <span data-ttu-id="a059a-164">Se presente, il riferimento restituito può essere usato per monitorare lo stato di avanzamento e ottenere il risultato del metodo.</span><span class="sxs-lookup"><span data-stu-id="a059a-164">If present, the returned reference can be used to monitor progress and obtain the result of the method.</span></span>

</dd> <dt>

<span data-ttu-id="a059a-165">*TimeoutPeriod* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a059a-165">*TimeoutPeriod* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a059a-166">Tipo: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a059a-166">Type: **datetime**</span></span>

<span data-ttu-id="a059a-167">Questo parametro non viene usato.</span><span class="sxs-lookup"><span data-stu-id="a059a-167">This parameter is not used.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a059a-168">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a059a-168">Return value</span></span>

<span data-ttu-id="a059a-169">Tipo: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="a059a-169">Type: **uint32**</span></span>

<span data-ttu-id="a059a-170">Questo metodo restituisce uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="a059a-170">This method returns one of the following values.</span></span>



| <span data-ttu-id="a059a-171">Codice/valore restituito</span><span class="sxs-lookup"><span data-stu-id="a059a-171">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="a059a-172">Descrizione</span><span class="sxs-lookup"><span data-stu-id="a059a-172">Description</span></span>                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a059a-173"><dt>**Completato senza errori**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-173"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                           | <span data-ttu-id="a059a-174">Esito positivo.</span><span class="sxs-lookup"><span data-stu-id="a059a-174">Success.</span></span><br/>                                                                |
| <dl> <span data-ttu-id="a059a-175"><dt>**Parametri del metodo controllati-transizione avviata**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-175"><dt>**Method Parameters Checked - Transition Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="a059a-176">La transizione è asincrona.</span><span class="sxs-lookup"><span data-stu-id="a059a-176">The transition is asynchronous.</span></span><br/>                                         |
| <dl> <span data-ttu-id="a059a-177"><dt>**Accesso negato**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-177"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                                 | <span data-ttu-id="a059a-178">Accesso negato.</span><span class="sxs-lookup"><span data-stu-id="a059a-178">Access denied.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="a059a-179"><dt></dt><dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-179"><dt></dt> <dt>32768</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="a059a-180"><dt></dt><dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-180"><dt></dt> <dt>32770</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="a059a-181"><dt></dt><dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-181"><dt></dt> <dt>32771</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="a059a-182"><dt></dt><dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-182"><dt></dt> <dt>32772</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="a059a-183"><dt></dt><dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-183"><dt></dt> <dt>32773</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="a059a-184"><dt></dt><dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-184"><dt></dt> <dt>32774</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="a059a-185"><dt>**Stato non valido per l'operazione**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-185"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>              | <span data-ttu-id="a059a-186">Il valore specificato nel parametro *RequestedState* non è supportato.</span><span class="sxs-lookup"><span data-stu-id="a059a-186">The value specified in the *RequestedState* parameter is not supported.</span></span><br/> |
| <dl> <span data-ttu-id="a059a-187"><dt></dt><dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-187"><dt></dt> <dt>32776</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="a059a-188"><dt></dt><dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-188"><dt></dt> <dt>32777</dt></span></span> </dl>                                                  |                                                                                    |
| <dl> <span data-ttu-id="a059a-189"><dt></dt><dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-189"><dt></dt> <dt>32778</dt></span></span> </dl>                                                  |                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="a059a-190">Commenti</span><span class="sxs-lookup"><span data-stu-id="a059a-190">Remarks</span></span>

<span data-ttu-id="a059a-191">L'accesso alla [**classe \_ ComputerSystem di MSVM**](msvm-computersystem.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente.</span><span class="sxs-lookup"><span data-stu-id="a059a-191">Access to the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="a059a-192">Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="a059a-192">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="examples"></a><span data-ttu-id="a059a-193">Esempio</span><span class="sxs-lookup"><span data-stu-id="a059a-193">Examples</span></span>

<span data-ttu-id="a059a-194">Nell'esempio C# seguente viene avviata o disabilitata una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a059a-194">The following C# example starts or disables a virtual machine.</span></span> <span data-ttu-id="a059a-195">Le utilità a cui si fa riferimento sono disponibili in [utilità comuni per gli esempi di virtualizzazione (v2)](common-utilities-for-the-virtualization-samples-v2.md).</span><span class="sxs-lookup"><span data-stu-id="a059a-195">The referenced utilities can be found in [Common utilities for the virtualization samples (V2)](common-utilities-for-the-virtualization-samples-v2.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a059a-196">Per funzionare correttamente, il codice seguente deve essere eseguito sul server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="a059a-196">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```CSharp
using System;
using System.Management;

namespace HyperVSamples
{
    public class RequestStateChangeClass
    {
        public static void RequestStateChange(string vmName, string action)
        {
            ManagementScope scope = new ManagementScope(@"\\.\root\virtualization\v2", null);
            ManagementObject vm = Utility.GetTargetComputer(vmName, scope);

            if (null == vm)
            {
                throw new ArgumentException(
                    string.Format(
                    "The virtual machine '{0}' could not be found.", 
                    vmName));
            }

            ManagementBaseObject inParams = vm.GetMethodParameters("RequestStateChange");

            const int Enabled = 2;
            const int Disabled = 3;

            if (action.ToLower() == "start")
            {
                inParams["RequestedState"] = Enabled;
            }
            else if (action.ToLower() == "stop")
            {
                inParams["RequestedState"] = Disabled;
            }
            else
            {
                throw new Exception("Wrong action is specified");
            }

            ManagementBaseObject outParams = vm.InvokeMethod(
                "RequestStateChange", 
                inParams, 
                null);

            if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
            {
                if (Utility.JobCompleted(outParams, scope))
                {
                    Console.WriteLine(
                        "{0} state was changed successfully.", 
                        vmName);
                }
                else
                {
                    Console.WriteLine("Failed to change virtual system state");
                }
            }
            else if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
            {
                Console.WriteLine(
                    "{0} state was changed successfully.", 
                    vmName);
            }
            else
            {
                Console.WriteLine(
                    "Change virtual system state failed with error {0}", 
                    outParams["ReturnValue"]);
            }

        }

        public static void Main(string[] args)
        {
            if (args != null && args.Length != 2)
            {
                Console.WriteLine("Usage: <application> vmName action");
                Console.WriteLine("action: start|stop");
                return;
            }

            RequestStateChange(args[0], args[1]);
        }

    }
}
```



<span data-ttu-id="a059a-197">Nell'esempio seguente Visual Basic Scripting Edition (VBScript) viene avviata o disabilitata una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="a059a-197">The following Visual Basic Scripting Edition (VBScript) example starts or disables a virtual machine.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a059a-198">Per funzionare correttamente, il codice seguente deve essere eseguito sul server host della macchina virtuale e deve essere eseguito con privilegi di amministratore.</span><span class="sxs-lookup"><span data-stu-id="a059a-198">To function correctly, the following code must be run on the virtual machine host server, and must be run with administrator privileges.</span></span>

 


```VB
dim objWMIService
dim fileSystem

const JobStarting = 3
const JobRunning = 4
const JobCompleted = 7
const wmiStarted = 4096
const Enabled = 2
const Disabled = 3



Main()

'-----------------------------------------------------------------
' Main routine
'-----------------------------------------------------------------
Sub Main()
    set fileSystem = Wscript.CreateObject("Scripting.FileSystemObject")

    strComputer = "."
    set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\virtualization\v2")

    set objArgs = WScript.Arguments
    if WScript.Arguments.Count = 2 then
       vmName= objArgs.Unnamed.Item(0)
       action = objArgs.Unnamed.Item(1)
    else
       WScript.Echo "usage: cscript StartVM.vbs vmName start|stop"
       WScript.Quit
    end if
    
    set computerSystem = GetComputerSystem(vmName)

    if RequestStateChange(computerSystem, action) then

        WriteLog "Done"
        WScript.Quit(0)
    else
        WriteLog "RequestStateChange failed"
        WScript.Quit(1)
    end if

End Sub

'-----------------------------------------------------------------
' Retrieve Msvm_VirtualComputerSystem from base on its ElementName
' 
'-----------------------------------------------------------------
Function GetComputerSystem(vmElementName)
    On Error Resume Next
    query = Format1("select * from Msvm_ComputerSystem where ElementName = '{0}'", vmElementName)
    set GetComputerSystem = objWMIService.ExecQuery(query).ItemIndex(0)
    if (Err.Number <> 0) then
        WriteLog Format1("Err.Number: {0}", Err.Number)
        WriteLog Format1("Err.Description:{0}",Err.Description)
        WScript.Quit(1)
    end if
End Function


'-----------------------------------------------------------------
' Turn on a virtual machine
'-----------------------------------------------------------------
Function RequestStateChange(computerSystem, action)
    WriteLog Format2("RequestStateChange({0}, {1})", computerSystem.ElementName, action)

    RequestStateChange = false
    set objInParam = computerSystem.Methods_("RequestStateChange").InParameters.SpawnInstance_()
    
    if action = "start" then
        objInParam.RequestedState = Enabled
    else
        objInParam.RequestedState = Disabled
    end if

    set objOutParams = computerSystem.ExecMethod_("RequestStateChange", objInParam)

    if (WMIMethodStarted(objOutParams)) then
        if (WMIJobCompleted(objOutParams)) then
            WriteLog Format1("VM {0} was started successfully", computerSystem.ElementName)
            RequestStateChange = true
        end if
    end if

End Function


'-----------------------------------------------------------------
' Handle wmi return values
'-----------------------------------------------------------------
Function WMIMethodStarted(outParam)

    WMIMethodStarted = false

    if Not IsNull(outParam) then
        wmiStatus = outParam.ReturnValue

        if  wmiStatus = wmiStarted then
            WMIMethodStarted = true
        end if

    end if

End Function


'-----------------------------------------------------------------
' Handle wmi Job object
'-----------------------------------------------------------------
Function WMIJobCompleted(outParam)
    dim WMIJob

    set WMIJob = objWMIService.Get(outParam.Job)

    WMIJobCompleted = true

    jobState = WMIJob.JobState

    while jobState = JobRunning or jobState = JobStarting

        WScript.Sleep(1000)
        set WMIJob = objWMIService.Get(outParam.Job)
        jobState = WMIJob.JobState

    wend


    if (jobState <> JobCompleted) then
        WriteLog Format1("ErrorDescription:{0}", WMIJob.ErrorDescription)
        WMIJobCompleted = false
    end if

End Function

'-----------------------------------------------------------------
' Create the console log files.
'-----------------------------------------------------------------
Sub WriteLog(line)
    dim fileStream
    set fileStream = fileSystem.OpenTextFile(".\StartVM.log", 8, true)
    WScript.Echo line
    fileStream.WriteLine line
    fileStream.Close

End Sub


'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format2(myString, arg0, arg1)
    Format2 = Format1(myString, arg0)
    Format2 = Replace(Format2, "{1}", arg1)
End Function

'------------------------------------------------------------------------------
' The string formatting functions to avoid string concatenation.
'------------------------------------------------------------------------------
Function Format1(myString, arg0)
    Format1 = Replace(myString, "{0}", arg0)
End Function
```



## <a name="requirements"></a><span data-ttu-id="a059a-199">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a059a-199">Requirements</span></span>



| <span data-ttu-id="a059a-200">Requisito</span><span class="sxs-lookup"><span data-stu-id="a059a-200">Requirement</span></span> | <span data-ttu-id="a059a-201">Valore</span><span class="sxs-lookup"><span data-stu-id="a059a-201">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a059a-202">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a059a-202">Minimum supported client</span></span><br/> | <span data-ttu-id="a059a-203">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a059a-203">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="a059a-204">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a059a-204">Minimum supported server</span></span><br/> | <span data-ttu-id="a059a-205">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a059a-205">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a059a-206">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="a059a-206">Namespace</span></span><br/>                | <span data-ttu-id="a059a-207">\\Virtualizzazione radice \\ v2</span><span class="sxs-lookup"><span data-stu-id="a059a-207">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="a059a-208">MOF</span><span class="sxs-lookup"><span data-stu-id="a059a-208">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a059a-209"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-209"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="a059a-210">DLL</span><span class="sxs-lookup"><span data-stu-id="a059a-210">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a059a-211"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="a059a-211"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="a059a-212">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a059a-212">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a059a-213">**\_ComputerSystem MSVM**</span><span class="sxs-lookup"><span data-stu-id="a059a-213">**Msvm\_ComputerSystem**</span></span>](msvm-computersystem.md)
</dt> </dl>

 

