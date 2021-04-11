---
description: La funzione ExpertIndicateStatus indica la percentuale di completamento dell'analisi degli esperti del file di acquisizione.
ms.assetid: 6dbaa6d3-6068-4a28-9d9f-bcc7a25da407
title: Funzione ExpertIndicateStatus (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ExpertIndicateStatus
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: ac707a774b667b96a4d612e9eaf7da2c779c0327
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128355"
---
# <a name="expertindicatestatus-function"></a><span data-ttu-id="63c5d-103">ExpertIndicateStatus (funzione)</span><span class="sxs-lookup"><span data-stu-id="63c5d-103">ExpertIndicateStatus function</span></span>

<span data-ttu-id="63c5d-104">La funzione **ExpertIndicateStatus** indica la percentuale di completamento dell'analisi del file di acquisizione da parte dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="63c5d-104">The **ExpertIndicateStatus** function indicates the percentage of completion of the expert's analysis of the capture file.</span></span>

## <a name="syntax"></a><span data-ttu-id="63c5d-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="63c5d-105">Syntax</span></span>


```C++
DWORD WINAPI ExpertIndicateStatus(
  _In_  HEXPERTKEY              hExpertKey,
  _In_  EXPERTSTATUSENUMERATION Status,
  _In_  DWORD                   SubStatus,
  _In_  char                    *sztext,
  _Out_ long                    PercentDone
);
```



## <a name="parameters"></a><span data-ttu-id="63c5d-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="63c5d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="63c5d-107">*hExpertKey* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63c5d-107">*hExpertKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63c5d-108">Identificatore univoco dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="63c5d-108">Unique expert identifier.</span></span> <span data-ttu-id="63c5d-109">Network Monitor passa *hExpertKey* all'esperto quando chiama la funzione [Run](run.md) .</span><span class="sxs-lookup"><span data-stu-id="63c5d-109">Network Monitor passes *hExpertKey* to the expert when it calls the [Run](run.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="63c5d-110">*Stato* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="63c5d-110">*Status* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63c5d-111">Stato corrente dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="63c5d-111">Current status of the analysis.</span></span> <span data-ttu-id="63c5d-112">Specificare uno dei valori [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) seguenti.</span><span class="sxs-lookup"><span data-stu-id="63c5d-112">Specify one of the following [EXPERTSTATUSENUMERATION](expertstatusenumeration.md) values.</span></span>



| <span data-ttu-id="63c5d-113">Valore</span><span class="sxs-lookup"><span data-stu-id="63c5d-113">Value</span></span>                                                                                                                                                                                 | <span data-ttu-id="63c5d-114">Significato</span><span class="sxs-lookup"><span data-stu-id="63c5d-114">Meaning</span></span>                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="EXPERTSTATUS_INACTIVE"></span><span id="expertstatus_inactive"></span><dl> <span data-ttu-id="63c5d-115"><dt>**EXPERTSTATUS \_ INattivo**</dt></span><span class="sxs-lookup"><span data-stu-id="63c5d-115"><dt>**EXPERTSTATUS\_INACTIVE**</dt></span></span> </dl> | <span data-ttu-id="63c5d-116">L'esperto non è mai stato avviato.</span><span class="sxs-lookup"><span data-stu-id="63c5d-116">The expert never started.</span></span> <br/>                                          |
| <span id="EXPERTSTATUS_STARTING"></span><span id="expertstatus_starting"></span><dl> <span data-ttu-id="63c5d-117"><dt>**avvio di EXPERTSTATUS \_**</dt></span><span class="sxs-lookup"><span data-stu-id="63c5d-117"><dt>**EXPERTSTATUS\_STARTING**</dt></span></span> </dl> | <span data-ttu-id="63c5d-118">L'esperto si sta avviando.</span><span class="sxs-lookup"><span data-stu-id="63c5d-118">The expert is starting.</span></span> <br/>                                            |
| <span id="EXPERTSTATUS_RUNNING"></span><span id="expertstatus_running"></span><dl> <span data-ttu-id="63c5d-119"><dt>**EXPERTSTATUS \_ in esecuzione**</dt></span><span class="sxs-lookup"><span data-stu-id="63c5d-119"><dt>**EXPERTSTATUS\_RUNNING**</dt></span></span> </dl>    | <span data-ttu-id="63c5d-120">L'esperto viene eseguito normalmente.</span><span class="sxs-lookup"><span data-stu-id="63c5d-120">The expert is running normally.</span></span> <br/>                                    |
| <span id="EXPERTSTATUS_PROBLEM"></span><span id="expertstatus_problem"></span><dl> <span data-ttu-id="63c5d-121"><dt>**\_problema EXPERTSTATUS**</dt></span><span class="sxs-lookup"><span data-stu-id="63c5d-121"><dt>**EXPERTSTATUS\_PROBLEM**</dt></span></span> </dl>    | <span data-ttu-id="63c5d-122">Un problema specificato nel parametro SubStatus ha interrotto l'esperto.</span><span class="sxs-lookup"><span data-stu-id="63c5d-122">A problem specified in the SubStatus parameter stopped the expert.</span></span> <br/> |
| <span id="EXPERTSTATUS_ABORTED"></span><span id="expertstatus_aborted"></span><dl> <span data-ttu-id="63c5d-123"><dt>**EXPERTSTATUS \_ interrotto**</dt></span><span class="sxs-lookup"><span data-stu-id="63c5d-123"><dt>**EXPERTSTATUS\_ABORTED**</dt></span></span> </dl>    | <span data-ttu-id="63c5d-124">Network Monitor arrestato l'esperto.</span><span class="sxs-lookup"><span data-stu-id="63c5d-124">Network Monitor stopped the expert.</span></span> <br/>                                |
| <span id="EXPERTSTATUS_DONE"></span><span id="expertstatus_done"></span><dl> <span data-ttu-id="63c5d-125"><dt>**EXPERTSTATUS \_ completato**</dt></span><span class="sxs-lookup"><span data-stu-id="63c5d-125"><dt>**EXPERTSTATUS\_DONE**</dt></span></span> </dl>             | <span data-ttu-id="63c5d-126">L'analisi è stata completata correttamente.</span><span class="sxs-lookup"><span data-stu-id="63c5d-126">The expert finished the analysis successfully.</span></span> <br/>                     |



 

</dd> <dt>

<span data-ttu-id="63c5d-127">*Stato secondario* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63c5d-127">*SubStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63c5d-128">Estensione o chiarimento delle informazioni fornite dal parametro *status* .</span><span class="sxs-lookup"><span data-stu-id="63c5d-128">Extension or clarification of information provided by the *Status* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="63c5d-129">*szText* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="63c5d-129">*sztext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="63c5d-130">Indicatore di stato del testo facoltativo.</span><span class="sxs-lookup"><span data-stu-id="63c5d-130">Optional text status indicator.</span></span>

<span data-ttu-id="63c5d-131">Il valore di questo parametro può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="63c5d-131">This parameter value may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="63c5d-132">*PercentDone* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="63c5d-132">*PercentDone* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="63c5d-133">Percentuale dei dati di acquisizione elaborati dall'esperto.</span><span class="sxs-lookup"><span data-stu-id="63c5d-133">Percentage of the capture data that the expert has processed.</span></span>

<span data-ttu-id="63c5d-134">Quando l'esperto completa correttamente l'analisi di un file di acquisizione, il sistema imposta la percentuale su 100.</span><span class="sxs-lookup"><span data-stu-id="63c5d-134">When the expert successfully completes analysis of a capture file, the system sets the percentage to 100.</span></span> <span data-ttu-id="63c5d-135">Qualsiasi numero maggiore di 99 verrà ignorato.</span><span class="sxs-lookup"><span data-stu-id="63c5d-135">Any number greater than 99 will be ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="63c5d-136">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="63c5d-136">Return value</span></span>

<span data-ttu-id="63c5d-137">Se la funzione ha esito positivo, il valore restituito è NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="63c5d-137">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="63c5d-138">Se la funzione ha esito negativo, il valore restituito è NMERR \_ Expert \_ Terminate; l'esperto deve immediatamente pulire e restituire senza completare l'acquisizione.</span><span class="sxs-lookup"><span data-stu-id="63c5d-138">If the function is unsuccessful, the return value is NMERR\_EXPERT\_TERMINATE; the expert must immediately clean up and return without completing the capture.</span></span>

## <a name="remarks"></a><span data-ttu-id="63c5d-139">Commenti</span><span class="sxs-lookup"><span data-stu-id="63c5d-139">Remarks</span></span>

<span data-ttu-id="63c5d-140">La funzione **ExpertIndicateStatus** può essere chiamata solo da esperti che implementano la funzione di esportazione [Run](run.md) o [Configure](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="63c5d-140">The **ExpertIndicateStatus** function can only be called by experts that implement the [Run](run.md) or [Configure](configure.md) export function.</span></span>

## <a name="requirements"></a><span data-ttu-id="63c5d-141">Requisiti</span><span class="sxs-lookup"><span data-stu-id="63c5d-141">Requirements</span></span>



| <span data-ttu-id="63c5d-142">Requisito</span><span class="sxs-lookup"><span data-stu-id="63c5d-142">Requirement</span></span> | <span data-ttu-id="63c5d-143">Valore</span><span class="sxs-lookup"><span data-stu-id="63c5d-143">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="63c5d-144">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63c5d-144">Minimum supported client</span></span><br/> | <span data-ttu-id="63c5d-145">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63c5d-145">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="63c5d-146">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="63c5d-146">Minimum supported server</span></span><br/> | <span data-ttu-id="63c5d-147">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="63c5d-147">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="63c5d-148">Intestazione</span><span class="sxs-lookup"><span data-stu-id="63c5d-148">Header</span></span><br/>                   | <dl> <span data-ttu-id="63c5d-149"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="63c5d-149"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="63c5d-150">Libreria</span><span class="sxs-lookup"><span data-stu-id="63c5d-150">Library</span></span><br/>                  | <dl> <span data-ttu-id="63c5d-151"><dt>Nmap. lib</dt></span><span class="sxs-lookup"><span data-stu-id="63c5d-151"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="63c5d-152">DLL</span><span class="sxs-lookup"><span data-stu-id="63c5d-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63c5d-153"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="63c5d-153"><dt>Nmapi.dll</dt></span></span> </dl> |
