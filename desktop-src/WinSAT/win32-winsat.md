---
title: Classe Win32_WinSAT
description: Definisce le informazioni di valutazione di riepilogo per la valutazione formale più recente.
ms.assetid: adf4de42-9dfd-46a7-ae75-3bbcfd15dd68
keywords:
- Classe Win32_WinSAT WinSAT
- Classe Win32_WinSAT WinSAT, descrizione
topic_type:
- apiref
api_name:
- Win32_WinSAT
- Win32_WinSAT.TimeTaken
- Win32_WinSAT.WinSPRLevel
- Win32_WinSAT.WinSATAssessmentState
- Win32_WinSAT.MemoryScore
- Win32_WinSAT.CPUScore
- Win32_WinSAT.DiskScore
- Win32_WinSAT.D3DScore
- Win32_WinSAT.GraphicsScore
api_location:
- WinSATAPI.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 829e5e1b3658771728aab9ef30634d90a8bc6450
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302732"
---
# <a name="win32_winsat-class"></a><span data-ttu-id="b005d-105">Win32 \_ WinSAT (classe)</span><span class="sxs-lookup"><span data-stu-id="b005d-105">Win32\_WinSAT class</span></span>

<span data-ttu-id="b005d-106">\[**Win32 \_ WinSAT** può essere modificato o non disponibile per le versioni dopo Windows 8.1.\]</span><span class="sxs-lookup"><span data-stu-id="b005d-106">\[**Win32\_WinSAT** may be altered or unavailable for releases after Windows 8.1.\]</span></span>

<span data-ttu-id="b005d-107">Definisce le informazioni di valutazione di riepilogo per la valutazione formale più recente.</span><span class="sxs-lookup"><span data-stu-id="b005d-107">Defines summary assessment information for the most recent formal assessment.</span></span>

<span data-ttu-id="b005d-108">La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà ereditate.</span><span class="sxs-lookup"><span data-stu-id="b005d-108">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b005d-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b005d-109">Syntax</span></span>

``` syntax
class Win32_WinSAT
{
  string TimeTaken = "MostRecentAssessment";
  real32 WinSPRLevel;
  uint32 WinSATAssessmentState;
  real32 MemoryScore;
  real32 CPUScore;
  real32 DiskScore;
  real32 D3DScore;
  real32 GraphicsScore;
};
```

## <a name="members"></a><span data-ttu-id="b005d-110">Members</span><span class="sxs-lookup"><span data-stu-id="b005d-110">Members</span></span>

<span data-ttu-id="b005d-111">La classe **Win32 \_ WinSAT** presenta questi tipi di membri:</span><span class="sxs-lookup"><span data-stu-id="b005d-111">The **Win32\_WinSAT** class has these types of members:</span></span>

-   [<span data-ttu-id="b005d-112">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b005d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b005d-113">Proprietà</span><span class="sxs-lookup"><span data-stu-id="b005d-113">Properties</span></span>

<span data-ttu-id="b005d-114">La classe **Win32 \_ WinSAT** dispone di queste proprietà.</span><span class="sxs-lookup"><span data-stu-id="b005d-114">The **Win32\_WinSAT** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b005d-115">**CPUScore**</span><span class="sxs-lookup"><span data-stu-id="b005d-115">**CPUScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b005d-116">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="b005d-116">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b005d-117">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b005d-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b005d-118">Punteggio per i processori del computer.</span><span class="sxs-lookup"><span data-stu-id="b005d-118">A score for the processors on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b005d-119">**D3DScore**</span><span class="sxs-lookup"><span data-stu-id="b005d-119">**D3DScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b005d-120">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="b005d-120">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b005d-121">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b005d-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b005d-122">Dopo Windows 8.1, WinSAT non valuterà più le funzionalità di grafica tridimensionale (gioco) del computer e la capacità del driver grafico di eseguire il rendering degli oggetti e di eseguire shader mediante questa valutazione.</span><span class="sxs-lookup"><span data-stu-id="b005d-122">After Windows 8.1, WinSAT no longer assess the three-dimensional graphics (gaming) capabilities of the computer and the graphics driver's ability to render objects and execute shaders using this assessment.</span></span> <span data-ttu-id="b005d-123">Per compatibilità, WinSAT segnala i valori sentinella per le metriche e i punteggi, tuttavia questi non vengono calcolati in tempo reale.</span><span class="sxs-lookup"><span data-stu-id="b005d-123">For compatibility, WinSAT report sentinel values for the metrics and scores, however these are not calculated in real time.</span></span>

</dd> <dt>

<span data-ttu-id="b005d-124">**DiskScore**</span><span class="sxs-lookup"><span data-stu-id="b005d-124">**DiskScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b005d-125">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="b005d-125">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b005d-126">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b005d-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b005d-127">Punteggio per la velocità effettiva di lettura sequenziale sul disco rigido primario nel computer.</span><span class="sxs-lookup"><span data-stu-id="b005d-127">A score for the sequential read throughput on the primary hard disk on the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b005d-128">**GraphicsScore**</span><span class="sxs-lookup"><span data-stu-id="b005d-128">**GraphicsScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b005d-129">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="b005d-129">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b005d-130">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b005d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b005d-131">Punteggio per le funzionalità grafiche del computer.</span><span class="sxs-lookup"><span data-stu-id="b005d-131">A score for the graphics capabilities of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b005d-132">**MemoryScore**</span><span class="sxs-lookup"><span data-stu-id="b005d-132">**MemoryScore**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b005d-133">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="b005d-133">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b005d-134">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b005d-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b005d-135">Punteggio per la velocità effettiva e la capacità della memoria del computer.</span><span class="sxs-lookup"><span data-stu-id="b005d-135">A score for the memory throughput and capacity of the computer.</span></span>

</dd> <dt>

<span data-ttu-id="b005d-136">**TimeTaken**</span><span class="sxs-lookup"><span data-stu-id="b005d-136">**TimeTaken**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b005d-137">Tipo di dati: **String**</span><span class="sxs-lookup"><span data-stu-id="b005d-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b005d-138">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b005d-138">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b005d-139">Qualificatori: **chiave**</span><span class="sxs-lookup"><span data-stu-id="b005d-139">Qualifiers: **key**</span></span>
</dt> </dl>

<span data-ttu-id="b005d-140">Questa proprietà deve essere impostata su "MostRecentAssessment" nella clausola WHERE della query WQL.</span><span class="sxs-lookup"><span data-stu-id="b005d-140">This property must be set to "MostRecentAssessment" in the WHERE clause of your WQL query.</span></span>

</dd> <dt>

<span data-ttu-id="b005d-141">**WinSATAssessmentState**</span><span class="sxs-lookup"><span data-stu-id="b005d-141">**WinSATAssessmentState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b005d-142">Tipo di dati: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="b005d-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="b005d-143">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b005d-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b005d-144">Stato della valutazione.</span><span class="sxs-lookup"><span data-stu-id="b005d-144">State of the assessment.</span></span> <span data-ttu-id="b005d-145">Per una descrizione dei valori possibili, vedere l'enumerazione [**\_ \_ dello stato di valutazione di WinSAT**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) .</span><span class="sxs-lookup"><span data-stu-id="b005d-145">For a description of the possible values, see the [**WINSAT\_ASSESSMENT\_STATE**](/windows/win32/api/winsatcominterfacei/ne-winsatcominterfacei-winsat_assessment_state) enumeration.</span></span>

<dl> <dt>

<span data-ttu-id="b005d-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)</span><span class="sxs-lookup"><span data-stu-id="b005d-146"><span id="StateUnknown"></span><span id="stateunknown"></span><span id="STATEUNKNOWN"></span>**StateUnknown** (0)</span></span>
</dt> <dt>

<span data-ttu-id="b005d-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Valido** (1)</span><span class="sxs-lookup"><span data-stu-id="b005d-147"><span id="Valid"></span><span id="valid"></span><span id="VALID"></span>**Valid** (1)</span></span>
</dt> <dt>

<span data-ttu-id="b005d-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)</span><span class="sxs-lookup"><span data-stu-id="b005d-148"><span id="IncoherentWithHardware"></span><span id="incoherentwithhardware"></span><span id="INCOHERENTWITHHARDWARE"></span>**IncoherentWithHardware** (2)</span></span>
</dt> <dt>

<span data-ttu-id="b005d-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)</span><span class="sxs-lookup"><span data-stu-id="b005d-149"><span id="NoAssessmentAvailable"></span><span id="noassessmentavailable"></span><span id="NOASSESSMENTAVAILABLE"></span>**NoAssessmentAvailable** (3)</span></span>
</dt> <dt>

<span data-ttu-id="b005d-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Non valido** (4)</span><span class="sxs-lookup"><span data-stu-id="b005d-150"><span id="Invalid"></span><span id="invalid"></span><span id="INVALID"></span>**Invalid** (4)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="b005d-151">**WinSPRLevel**</span><span class="sxs-lookup"><span data-stu-id="b005d-151">**WinSPRLevel**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b005d-152">Tipo di dati: **real32**</span><span class="sxs-lookup"><span data-stu-id="b005d-152">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="b005d-153">Tipo di accesso: sola lettura</span><span class="sxs-lookup"><span data-stu-id="b005d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b005d-154">Punteggio di base per il computer.</span><span class="sxs-lookup"><span data-stu-id="b005d-154">Base score for the computer.</span></span> <span data-ttu-id="b005d-155">Per informazioni dettagliate sul valore score, vedere la proprietà [**IProvideWinSATResultsInfo:: SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) .</span><span class="sxs-lookup"><span data-stu-id="b005d-155">For details on the score value, see the [**IProvideWinSATResultsInfo::SystemRating**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatresultsinfo-get_systemrating) property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b005d-156">Commenti</span><span class="sxs-lookup"><span data-stu-id="b005d-156">Remarks</span></span>

<span data-ttu-id="b005d-157">Per informazioni sui punteggi dei sottocomponenti, ad esempio **MemoryScore**, vedere la proprietà [**IProvideWinSATAssessmentInfo:: Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) .</span><span class="sxs-lookup"><span data-stu-id="b005d-157">For information on the subcomponent scores, such as **MemoryScore**, see the [**IProvideWinSATAssessmentInfo::Score**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatassessmentinfo-get_score) property.</span></span>

## <a name="examples"></a><span data-ttu-id="b005d-158">Esempio</span><span class="sxs-lookup"><span data-stu-id="b005d-158">Examples</span></span>

<span data-ttu-id="b005d-159">Per un esempio in cui viene illustrato come utilizzare WMI per recuperare dati da questa classe, vedere il metodo [**IProvideWinSATVisuals:: Get \_ bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) .</span><span class="sxs-lookup"><span data-stu-id="b005d-159">For an example that shows how to use WMI to retrieve data from this class, see the [**IProvideWinSATVisuals::get\_Bitmap**](/windows/desktop/api/Winsatcominterfacei/nf-winsatcominterfacei-iprovidewinsatvisuals-get_bitmap) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b005d-160">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b005d-160">Requirements</span></span>



| <span data-ttu-id="b005d-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="b005d-161">Requirement</span></span> | <span data-ttu-id="b005d-162">Valore</span><span class="sxs-lookup"><span data-stu-id="b005d-162">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b005d-163">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b005d-163">Minimum supported client</span></span><br/> | <span data-ttu-id="b005d-164">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b005d-164">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="b005d-165">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b005d-165">Minimum supported server</span></span><br/> | <span data-ttu-id="b005d-166">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b005d-166">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b005d-167">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b005d-167">Namespace</span></span><br/>                | <span data-ttu-id="b005d-168">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="b005d-168">Root\\CIMv2</span></span><br/>                                                                   |
| <span data-ttu-id="b005d-169">MOF</span><span class="sxs-lookup"><span data-stu-id="b005d-169">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b005d-170"><dt>WinSAT. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b005d-170"><dt>WinSAT.mof</dt></span></span> </dl>    |
| <span data-ttu-id="b005d-171">DLL</span><span class="sxs-lookup"><span data-stu-id="b005d-171">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b005d-172"><dt>WinSATAPI.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b005d-172"><dt>WinSATAPI.dll</dt></span></span> </dl> |



 

 





