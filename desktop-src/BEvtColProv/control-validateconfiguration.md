---
description: Convalidare la correttezza di un testo di configurazione senza impostarlo come attivo. Restituisce 1 in seguito all'esito positivo, 0 in seguito a un errore.
ms.assetid: baeabed0-7717-498a-9886-e49e4a101711
ms.tgt_platform: multiple
title: Metodo ValidateConfiguration della classe Control
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Control.ValidateConfiguration
api_type:
- COM
api_location:
- BEvtCol.exe
ms.openlocfilehash: d4e1d0061b779a54973aeea1a487d8838781cf6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103965909"
---
# <a name="validateconfiguration-method-of-the-control-class"></a><span data-ttu-id="e9f2c-104">Metodo ValidateConfiguration della classe Control</span><span class="sxs-lookup"><span data-stu-id="e9f2c-104">ValidateConfiguration method of the Control class</span></span>

<span data-ttu-id="e9f2c-105">Convalidare la correttezza di un testo di configurazione senza impostarlo come attivo.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-105">Validate a configuration text for correctness without setting it active.</span></span> <span data-ttu-id="e9f2c-106">Restituisce 1 in seguito all'esito positivo, 0 in seguito a un errore.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-106">Returns 1 on success, 0 on error.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9f2c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e9f2c-107">Syntax</span></span>


```mof
Uint32 ValidateConfiguration(
  [in]  string Config,
  [out] string ErrorString,
  [out] string WarningString,
  [out] string InfoString,
  [out] uint32 ErrorType
);
```



## <a name="parameters"></a><span data-ttu-id="e9f2c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="e9f2c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9f2c-109">*Configurazione* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="e9f2c-109">*Config* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f2c-110">Configurazione da verificare.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-110">The configuration to check.</span></span>

</dd> <dt>

<span data-ttu-id="e9f2c-111">*ErrorString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e9f2c-111">*ErrorString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f2c-112">Quando questo metodo restituisce, se si è verificato un errore, questo parametro contiene una descrizione dell'errore di convalida per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-112">When this method returns, if there was a error, this parameter contains a description of the validation error for the operation.</span></span>

</dd> <dt>

<span data-ttu-id="e9f2c-113">*WarningString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e9f2c-113">*WarningString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f2c-114">Quando questo metodo restituisce un risultato, questo parametro contiene una descrizione degli avvisi di convalida per l'operazione.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-114">When this method returns, this parameter contains a description of any validation warnings for the operation.</span></span>

<span data-ttu-id="e9f2c-115">Stringa di testo con avvisi.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-115">The text string with warnings.</span></span>

</dd> <dt>

<span data-ttu-id="e9f2c-116">*InfoString* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e9f2c-116">*InfoString* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f2c-117">Quando questo metodo restituisce un risultato, questo parametro contiene un set di informazioni sulla configurazione.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-117">When this method returns, this parameter contains a set of information about the configuration.</span></span>

</dd> <dt>

<span data-ttu-id="e9f2c-118">*ErrorType* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="e9f2c-118">*ErrorType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9f2c-119">Quando questo metodo restituisce, se si è verificato un errore di convalida, questo parametro indica il tipo di errore.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-119">When this method returns, if there was a validation error, this parameter indicates the error type.</span></span>

<span data-ttu-id="e9f2c-120">I valori possibili sono:</span><span class="sxs-lookup"><span data-stu-id="e9f2c-120">The possible values are:</span></span>

<dt>

<span data-ttu-id="e9f2c-121">0</span><span class="sxs-lookup"><span data-stu-id="e9f2c-121">0</span></span>
</dt> <dd>

<span data-ttu-id="e9f2c-122">Argomento mancante.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-122">The argument is missing.</span></span>

</dd> <dt>

<span data-ttu-id="e9f2c-123">1</span><span class="sxs-lookup"><span data-stu-id="e9f2c-123">1</span></span>
</dt> <dd>

<span data-ttu-id="e9f2c-124">Il formato dell'argomento non è valido.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-124">The argument format is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="e9f2c-125">2</span><span class="sxs-lookup"><span data-stu-id="e9f2c-125">2</span></span>
</dt> <dd>

<span data-ttu-id="e9f2c-126">Un argomento di configurazione non è valido.</span><span class="sxs-lookup"><span data-stu-id="e9f2c-126">A configuration argument is invalid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9f2c-127">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e9f2c-127">Return value</span></span>

<dl> <dt>


</dt> <dd>

<span data-ttu-id="e9f2c-128">0</span><span class="sxs-lookup"><span data-stu-id="e9f2c-128">0</span></span>

<span data-ttu-id="e9f2c-129">Errore</span><span class="sxs-lookup"><span data-stu-id="e9f2c-129">Failure</span></span>

</dd> <dt>


</dt> <dd>

<span data-ttu-id="e9f2c-130">1</span><span class="sxs-lookup"><span data-stu-id="e9f2c-130">1</span></span>

<span data-ttu-id="e9f2c-131">Operazione completata</span><span class="sxs-lookup"><span data-stu-id="e9f2c-131">Success</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e9f2c-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e9f2c-132">Requirements</span></span>



| <span data-ttu-id="e9f2c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9f2c-133">Requirement</span></span> | <span data-ttu-id="e9f2c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="e9f2c-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9f2c-135">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f2c-135">Minimum supported client</span></span><br/> | <span data-ttu-id="e9f2c-136">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="e9f2c-136">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e9f2c-137">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e9f2c-137">Minimum supported server</span></span><br/> | <span data-ttu-id="e9f2c-138">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="e9f2c-138">Windows Server 2016</span></span><br/>                                                                       |
| <span data-ttu-id="e9f2c-139">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="e9f2c-139">Namespace</span></span><br/>                | <span data-ttu-id="e9f2c-140">Radice \\ Microsoft \\ Windows \\ BootEventCollector</span><span class="sxs-lookup"><span data-stu-id="e9f2c-140">Root\\Microsoft\\Windows\\BootEventCollector</span></span><br/>                                              |
| <span data-ttu-id="e9f2c-141">MOF</span><span class="sxs-lookup"><span data-stu-id="e9f2c-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e9f2c-142"><dt>BootEventCollectorWMI. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e9f2c-142"><dt>BootEventCollectorWMI.mof</dt></span></span> </dl> |
| <span data-ttu-id="e9f2c-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e9f2c-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9f2c-144"><dt>BEvtCol.exe</dt></span><span class="sxs-lookup"><span data-stu-id="e9f2c-144"><dt>BEvtCol.exe</dt></span></span> </dl>               |



## <a name="see-also"></a><span data-ttu-id="e9f2c-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e9f2c-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9f2c-146">**Control**</span><span class="sxs-lookup"><span data-stu-id="e9f2c-146">**Control**</span></span>](control.md)
</dt> </dl>

 

 




