---
description: La struttura EXPERTENUMINFO fornisce informazioni sull'esperto.
ms.assetid: f745997b-d753-4c4d-88b6-6978f5eaa91c
title: Struttura EXPERTENUMINFO (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EXPERTENUMINFO
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 35b8d36f55838492eb71640228d7216e6e594738
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305951"
---
# <a name="expertenuminfo-structure"></a><span data-ttu-id="7b272-103">Struttura EXPERTENUMINFO</span><span class="sxs-lookup"><span data-stu-id="7b272-103">EXPERTENUMINFO structure</span></span>

<span data-ttu-id="7b272-104">La struttura **EXPERTENUMINFO** fornisce informazioni sull'esperto.</span><span class="sxs-lookup"><span data-stu-id="7b272-104">The **EXPERTENUMINFO** structure provides information about the expert.</span></span> <span data-ttu-id="7b272-105">Network Monitor alloca memoria per la struttura e la passa all'esperto quando chiama la funzione [**Register Expert**](register-expert.md) .</span><span class="sxs-lookup"><span data-stu-id="7b272-105">Network Monitor allocates memory for the structure, and passes it to the expert when it calls the [**Register Expert**](register-expert.md) function.</span></span> <span data-ttu-id="7b272-106">Quando l'esperto riceve la struttura, deve compilare tutte le informazioni che Network Monitor richieste.</span><span class="sxs-lookup"><span data-stu-id="7b272-106">When the expert receives the structure, it must then fill-in all the information that Network Monitor requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="7b272-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7b272-107">Syntax</span></span>


```C++
typedef struct {
  char                szName[EXPERTSTRINGLENGTH];
  char                szVendor[EXPERTSTRINGLENGTH];
  char                szDescription[EXPERTSTRINGLENGTH];
  DWORD               Version;
  DWORD               Flags;
  HEXPERT             hExpert;
  char                szDllName[MAX_PATH];
  HINSTANCE           hModule;
  PEXPERTREGISTERPROC pRegisterProc;
  PEXPERTCONFIGPROC   pConfigProc;
  PEXPERTRUNPROC      pRunProc;
} EXPERTENUMINFO, *PEXPERTENUMINFO;
```



## <a name="members"></a><span data-ttu-id="7b272-108">Members</span><span class="sxs-lookup"><span data-stu-id="7b272-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="7b272-109">**szName**</span><span class="sxs-lookup"><span data-stu-id="7b272-109">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="7b272-110">Nome dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="7b272-110">Name of the expert.</span></span>

</dd> <dt>

<span data-ttu-id="7b272-111">**szVendor**</span><span class="sxs-lookup"><span data-stu-id="7b272-111">**szVendor**</span></span>
</dt> <dd>

<span data-ttu-id="7b272-112">Nome del fornitore che crea l'esperto.</span><span class="sxs-lookup"><span data-stu-id="7b272-112">Name of the vendor that creates the expert.</span></span>

</dd> <dt>

<span data-ttu-id="7b272-113">**szDescription**</span><span class="sxs-lookup"><span data-stu-id="7b272-113">**szDescription**</span></span>
</dt> <dd>

<span data-ttu-id="7b272-114">Descrizione dell'esperto.</span><span class="sxs-lookup"><span data-stu-id="7b272-114">Description of the expert.</span></span> <span data-ttu-id="7b272-115">Il valore del membro **szDescription** può essere **null**.</span><span class="sxs-lookup"><span data-stu-id="7b272-115">The value of the **szDescription** member may be **NULL**.</span></span> <span data-ttu-id="7b272-116">Se il nome è troppo lungo, viene troncato nella configurazione del visualizzatore predefinito.</span><span class="sxs-lookup"><span data-stu-id="7b272-116">If the name is too long, it is truncated in the default viewer configuration.</span></span>

</dd> <dt>

<span data-ttu-id="7b272-117">**Versione**</span><span class="sxs-lookup"><span data-stu-id="7b272-117">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="7b272-118">Il valore deve essere zero.</span><span class="sxs-lookup"><span data-stu-id="7b272-118">The value must be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7b272-119">**Flag**</span><span class="sxs-lookup"><span data-stu-id="7b272-119">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="7b272-120">I flag seguenti descrivono l'esperto.</span><span class="sxs-lookup"><span data-stu-id="7b272-120">The following flags describe the expert.</span></span>



| <span data-ttu-id="7b272-121">Valore</span><span class="sxs-lookup"><span data-stu-id="7b272-121">Value</span></span>                                                                                                                                                                                                                                                    | <span data-ttu-id="7b272-122">Significato</span><span class="sxs-lookup"><span data-stu-id="7b272-122">Meaning</span></span>                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <span id="EXPERT_ENUM_FLAG_CONFIGURABLE"></span><span id="expert_enum_flag_configurable"></span><dl> <span data-ttu-id="7b272-123"><dt>**\_flag enum \_ esperto \_ configurabile**</dt></span><span class="sxs-lookup"><span data-stu-id="7b272-123"><dt>**EXPERT\_ENUM\_FLAG\_CONFIGURABLE**</dt></span></span> </dl>                                          | <span data-ttu-id="7b272-124">L'esperto supporta le chiamate al metodo [**Configure**](configure.md) .</span><span class="sxs-lookup"><span data-stu-id="7b272-124">The expert supports calls to the [**Configure**](configure.md) method.</span></span> <br/>        |
| <span id="EXPERT_ENUM_FLAG_VIEWER_PRIVATE"></span><span id="expert_enum_flag_viewer_private"></span><dl> <span data-ttu-id="7b272-125"><dt>**\_ \_ Visualizzatore flag enum \_ esperto \_ privato**</dt></span><span class="sxs-lookup"><span data-stu-id="7b272-125"><dt>**EXPERT\_ENUM\_FLAG\_VIEWER\_PRIVATE**</dt></span></span> </dl>                                   | <span data-ttu-id="7b272-126">L'esperto richiede un Visualizzatore eventi privato (non condiviso).</span><span class="sxs-lookup"><span data-stu-id="7b272-126">The expert requires a private (non-shared) Event Viewer.</span></span> <br/>                       |
| <span id="EXPERT_ENUM_FLAG_NO_VIEWER"></span><span id="expert_enum_flag_no_viewer"></span><dl> <span data-ttu-id="7b272-127"><dt>**\_flag enum \_ esperto \_ senza \_ Visualizzatore**</dt></span><span class="sxs-lookup"><span data-stu-id="7b272-127"><dt>**EXPERT\_ENUM\_FLAG\_NO\_VIEWER**</dt></span></span> </dl>                                                  | <span data-ttu-id="7b272-128">L'esperto non invia notifiche degli eventi.</span><span class="sxs-lookup"><span data-stu-id="7b272-128">The expert does not send event notifications.</span></span> <br/>                                  |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_SUMMARY"></span><span id="expert_enum_flag_add_me_to_rmc_in_summary"></span><dl> <span data-ttu-id="7b272-129"><dt>**\_flag enum \_ esperto \_ aggiunto \_ \_ a \_ RMC \_ in \_ Riepilogo**</dt></span><span class="sxs-lookup"><span data-stu-id="7b272-129"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_SUMMARY**</dt></span></span> </dl> | <span data-ttu-id="7b272-130">Quando lo stato attivo si trova nel riquadro Riepilogo, l'esperto viene visualizzato nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="7b272-130">When the focus is in the summary pane, the expert appears on the context menu.</span></span> <br/> |
| <span id="EXPERT_ENUM_FLAG_ADD_ME_TO_RMC_IN_DETAIL"></span><span id="expert_enum_flag_add_me_to_rmc_in_detail"></span><dl> <span data-ttu-id="7b272-131"><dt>**\_flag enum \_ esperto \_ aggiunto \_ \_ a \_ RMC \_ in \_ dettaglio**</dt></span><span class="sxs-lookup"><span data-stu-id="7b272-131"><dt>**EXPERT\_ENUM\_FLAG\_ADD\_ME\_TO\_RMC\_IN\_DETAIL**</dt></span></span> </dl>    | <span data-ttu-id="7b272-132">Quando lo stato attivo si trova nel riquadro dei dettagli, l'esperto viene visualizzato nel menu di scelta rapida.</span><span class="sxs-lookup"><span data-stu-id="7b272-132">When the focus is in the detail pane, the expert appears on the context menu.</span></span> <br/>  |



 

</dd> <dt>

<span data-ttu-id="7b272-133">**hExpert**</span><span class="sxs-lookup"><span data-stu-id="7b272-133">**hExpert**</span></span>
</dt> <dd>

<span data-ttu-id="7b272-134">Handle per l'esperto.</span><span class="sxs-lookup"><span data-stu-id="7b272-134">Handle to the expert.</span></span> <span data-ttu-id="7b272-135">Quando la struttura **EXPERTENUMINFO** viene utilizzata per registrare un esperto, il parametro viene ignorato.</span><span class="sxs-lookup"><span data-stu-id="7b272-135">When the **EXPERTENUMINFO** structure is used to register an expert, the parameter is ignored.</span></span>

</dd> <dt>

<span data-ttu-id="7b272-136">**szDllName**</span><span class="sxs-lookup"><span data-stu-id="7b272-136">**szDllName**</span></span>
</dt> <dd>

<span data-ttu-id="7b272-137">Membro privato; Non usare.</span><span class="sxs-lookup"><span data-stu-id="7b272-137">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="7b272-138">**hModule**</span><span class="sxs-lookup"><span data-stu-id="7b272-138">**hModule**</span></span>
</dt> <dd>

<span data-ttu-id="7b272-139">Membro privato; Non usare.</span><span class="sxs-lookup"><span data-stu-id="7b272-139">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="7b272-140">**pRegisterProc**</span><span class="sxs-lookup"><span data-stu-id="7b272-140">**pRegisterProc**</span></span>
</dt> <dd>

<span data-ttu-id="7b272-141">Membro privato; Non usare.</span><span class="sxs-lookup"><span data-stu-id="7b272-141">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="7b272-142">**pConfigProc**</span><span class="sxs-lookup"><span data-stu-id="7b272-142">**pConfigProc**</span></span>
</dt> <dd>

<span data-ttu-id="7b272-143">Membro privato; Non usare.</span><span class="sxs-lookup"><span data-stu-id="7b272-143">Private member; do not use.</span></span>

</dd> <dt>

<span data-ttu-id="7b272-144">**pRunProc**</span><span class="sxs-lookup"><span data-stu-id="7b272-144">**pRunProc**</span></span>
</dt> <dd>

<span data-ttu-id="7b272-145">Membro privato; Non usare.</span><span class="sxs-lookup"><span data-stu-id="7b272-145">Private member; do not use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7b272-146">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7b272-146">Requirements</span></span>



| <span data-ttu-id="7b272-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="7b272-147">Requirement</span></span> | <span data-ttu-id="7b272-148">Valore</span><span class="sxs-lookup"><span data-stu-id="7b272-148">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="7b272-149">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b272-149">Minimum supported client</span></span><br/> | <span data-ttu-id="7b272-150">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7b272-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="7b272-151">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7b272-151">Minimum supported server</span></span><br/> | <span data-ttu-id="7b272-152">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7b272-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="7b272-153">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7b272-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="7b272-154"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7b272-154"><dt>Netmon.h</dt></span></span> </dl> |



 

 




