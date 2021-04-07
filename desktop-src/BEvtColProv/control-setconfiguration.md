---
description: Imposta la nuova configurazione attiva dell'agente di raccolta.
ms.assetid: 1979e657-a8f3-4eab-991c-a884bde10724
ms.tgt_platform: multiple
title: Metodo di configurazione della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.SetConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: 4f482de9c4cd8f410371da51e605762a1f92e104
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747783"
---
# <a name="setconfiguration-method-of-the-control-class"></a><span data-ttu-id="1d883-103">Metodo di configurazione della classe Control</span><span class="sxs-lookup"><span data-stu-id="1d883-103">SetConfiguration method of the Control class</span></span>

<span data-ttu-id="1d883-104">Imposta la nuova configurazione attiva dell'agente di raccolta.</span><span class="sxs-lookup"><span data-stu-id="1d883-104">Set the new active configuration of the collector.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d883-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1d883-105">Syntax</span></span>


```mof
Uint32 SetConfiguration(
  [in]  string Config,
  [in]  Uint32 OldTimestampLow,
  [in]  Uint32 OldTimestampHigh,
  [out] Uint32 NewTimestampLow,
  [out] Uint32 NewTimestampHigh,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="1d883-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1d883-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d883-107">*Configurazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="1d883-107">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d883-108">Configurazione da attivare.</span><span class="sxs-lookup"><span data-stu-id="1d883-108">The configuration to activate.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-109">*OldTimestampLow* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d883-109">*OldTimestampLow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d883-110">Bit di ordine inferiore di un timestamp che indica quando è stata impostata la configurazione attiva corrente.</span><span class="sxs-lookup"><span data-stu-id="1d883-110">The low-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="1d883-111">Il controllo di atomicità è abilitato se questa proprietà non è impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="1d883-111">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-112">*OldTimestampHigh* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1d883-112">*OldTimestampHigh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d883-113">Bit di ordine superiore di un timestamp che indica quando è stata impostata la configurazione attiva corrente.</span><span class="sxs-lookup"><span data-stu-id="1d883-113">The high-order bits of a timestamp that indicates when the current active configuration was set.</span></span> <span data-ttu-id="1d883-114">Il controllo di atomicità è abilitato se questa proprietà non è impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="1d883-114">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-115">*NewTimestampLow* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1d883-115">*NewTimestampLow* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d883-116">Quando questo metodo restituisce un risultato, questo parametro contiene i bit di ordine inferiore di un timestamp che indica quando è stata impostata la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="1d883-116">When this method returns, this parameter contains the low-order bits of a timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="1d883-117">Il controllo di atomicità è abilitato se questa proprietà non è impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="1d883-117">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-118">*NewTimestampHigh* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1d883-118">*NewTimestampHigh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d883-119">Quando questo metodo viene restituito, questo parametro contiene i bit più significativi del timestamp che indica quando è stata impostata la nuova configurazione.</span><span class="sxs-lookup"><span data-stu-id="1d883-119">When this method returns, this parameter contains the high-order bits of the timestamp that indicates when the new configuration was set.</span></span> <span data-ttu-id="1d883-120">Il controllo di atomicità è abilitato se questa proprietà non è impostata su 0.</span><span class="sxs-lookup"><span data-stu-id="1d883-120">Atomicity checking is enabled if this property is not set to 0.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-121">*ErrorString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1d883-121">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d883-122">Quando questo metodo restituisce, se si è verificato un errore, questo parametro contiene la descrizione dell'errore.</span><span class="sxs-lookup"><span data-stu-id="1d883-122">When this method returns, if there was an error, this parameter contains the error description.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-123">*WarningString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1d883-123">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d883-124">Quando questo metodo termina, questo parametro contiene tutti i messaggi di avviso per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="1d883-124">When this method returns, this parameter contains any warnings messages for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-125">*InfoString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1d883-125">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d883-126">Quando questo metodo restituisce un risultato, questo parametro contiene informazioni per la nuova configurazione attiva.</span><span class="sxs-lookup"><span data-stu-id="1d883-126">When this method returns, this parameter contains information for the new active configuration.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-127">*ErrorType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1d883-127">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1d883-128">Quando questo metodo restituisce, se si è verificato un errore, questo parametro indica il tipo di errore.</span><span class="sxs-lookup"><span data-stu-id="1d883-128">When this method returns, if there was an error, this parameter indicates the error type.</span></span>

<dt>

<span data-ttu-id="1d883-129">0</span><span class="sxs-lookup"><span data-stu-id="1d883-129">0</span></span>
</dt> <dd>

<span data-ttu-id="1d883-130">La nuova configurazione è mancante.</span><span class="sxs-lookup"><span data-stu-id="1d883-130">The new configuration is missing.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-131">1</span><span class="sxs-lookup"><span data-stu-id="1d883-131">1</span></span>
</dt> <dd>

<span data-ttu-id="1d883-132">Il formato della nuova configurazione non è valido.</span><span class="sxs-lookup"><span data-stu-id="1d883-132">The format of the new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-133">2</span><span class="sxs-lookup"><span data-stu-id="1d883-133">2</span></span>
</dt> <dd>

<span data-ttu-id="1d883-134">La nuova configurazione non è valida.</span><span class="sxs-lookup"><span data-stu-id="1d883-134">The new configuration is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-135">3</span><span class="sxs-lookup"><span data-stu-id="1d883-135">3</span></span>
</dt> <dd>

<span data-ttu-id="1d883-136">Si è verificato un errore causato da un socket aperto.</span><span class="sxs-lookup"><span data-stu-id="1d883-136">There was an error caused by an open socket.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-137">4</span><span class="sxs-lookup"><span data-stu-id="1d883-137">4</span></span>
</dt> <dd>

<span data-ttu-id="1d883-138">Si è verificato un errore di scrittura del file.</span><span class="sxs-lookup"><span data-stu-id="1d883-138">There was a file write error.</span></span>

</dd> <dt>

<span data-ttu-id="1d883-139">5</span><span class="sxs-lookup"><span data-stu-id="1d883-139">5</span></span>
</dt> <dd>

<span data-ttu-id="1d883-140">Si è verificato un errore di atomicità.</span><span class="sxs-lookup"><span data-stu-id="1d883-140">There was an atomicity error.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d883-141">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1d883-141">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="1d883-142">0</span><span class="sxs-lookup"><span data-stu-id="1d883-142">0</span></span>

<span data-ttu-id="1d883-143">Errore</span><span class="sxs-lookup"><span data-stu-id="1d883-143">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="1d883-144">1</span><span class="sxs-lookup"><span data-stu-id="1d883-144">1</span></span>

<span data-ttu-id="1d883-145">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="1d883-145">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1d883-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1d883-146">Requirements</span></span>



| <span data-ttu-id="1d883-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d883-147">Requirement</span></span> | <span data-ttu-id="1d883-148">Valore</span><span class="sxs-lookup"><span data-stu-id="1d883-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d883-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d883-149">Minimum supported client</span></span><br/> | <span data-ttu-id="1d883-150">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1d883-150">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="1d883-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1d883-151">Minimum supported server</span></span><br/> | <span data-ttu-id="1d883-152">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="1d883-152">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="1d883-153">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="1d883-153">Namespace</span></span><br/>                | <span data-ttu-id="1d883-154">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="1d883-154">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="1d883-155">MOF</span><span class="sxs-lookup"><span data-stu-id="1d883-155">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d883-156"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d883-156"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d883-157">DLL</span><span class="sxs-lookup"><span data-stu-id="1d883-157">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d883-158"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="1d883-158"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="1d883-159">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1d883-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d883-160">**Control**</span><span class="sxs-lookup"><span data-stu-id="1d883-160">**Control**</span></span>](control.md)
</dt> </dl>

 

 




