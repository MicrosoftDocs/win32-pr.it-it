---
description: Contiene informazioni sui dati di AppHelp.
ms.assetid: 31b305e9-1f38-4952-b4fd-963df79b1346
title: Struttura APPHELP_DATA
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- APPHELP_DATA
api_type:
- NA
api_location: ''
ms.openlocfilehash: 20c66779dcb3d89746de5f90b2817ddcdb37b59f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304458"
---
# <a name="apphelp_data-structure"></a><span data-ttu-id="ed869-103">\_Struttura dei dati APPHELP</span><span class="sxs-lookup"><span data-stu-id="ed869-103">APPHELP\_DATA structure</span></span>

<span data-ttu-id="ed869-104">Contiene informazioni sui dati di AppHelp.</span><span class="sxs-lookup"><span data-stu-id="ed869-104">Contains Apphelp data information.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed869-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ed869-105">Syntax</span></span>


```C++
typedef struct tagAPPHELP_DATA {
  DWORD  dwFlags;
  DWORD  dwSeverity;
  DWORD  dwHTMLHelpID;
  LPTSTR szAppName;
  TAGREF trExe;
  LPTSTR szURL;
  LPTSTR szLink;
  LPTSTR szAppTitle;
  LPTSTR szContact;
  LPTSTR szDetails;
  DWORD  dwData;
  BOOL   bSPEntry;
} APPHELP_DATA, *PAPPHELP_DATA;
```



## <a name="members"></a><span data-ttu-id="ed869-106">Members</span><span class="sxs-lookup"><span data-stu-id="ed869-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ed869-107">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="ed869-107">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-108">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="ed869-108">This parameter can be one of more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ed869-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Disabilita \_ shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="ed869-109"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="ed869-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DISABILITARE \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="ed869-110"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="ed869-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="ed869-111"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="ed869-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annullamento APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="ed869-112"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="ed869-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Disabilita \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="ed869-113"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="ed869-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DISABLE \_ Layer** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="ed869-114"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="ed869-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Disabilita \_ driver** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="ed869-115"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="ed869-116">**dwSeverity**</span><span class="sxs-lookup"><span data-stu-id="ed869-116">**dwSeverity**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-117">Questo parametro può essere APPTYPE \_ None (0).</span><span class="sxs-lookup"><span data-stu-id="ed869-117">This parameter can be APPTYPE\_NONE (0).</span></span>

</dd> <dt>

<span data-ttu-id="ed869-118">**dwHTMLHelpID**</span><span class="sxs-lookup"><span data-stu-id="ed869-118">**dwHTMLHelpID**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-119">Identificatore della Guida HTML.</span><span class="sxs-lookup"><span data-stu-id="ed869-119">The HTML Help identifier.</span></span>

</dd> <dt>

<span data-ttu-id="ed869-120">**szAppName**</span><span class="sxs-lookup"><span data-stu-id="ed869-120">**szAppName**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-121">Nome dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ed869-121">The application name.</span></span>

</dd> <dt>

<span data-ttu-id="ed869-122">**trExe**</span><span class="sxs-lookup"><span data-stu-id="ed869-122">**trExe**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-123">[**TAGREF**](tagref.md) del file eseguibile corrispondente.</span><span class="sxs-lookup"><span data-stu-id="ed869-123">The [**TAGREF**](tagref.md) of the corresponding executable file.</span></span>

</dd> <dt>

<span data-ttu-id="ed869-124">**szURL**</span><span class="sxs-lookup"><span data-stu-id="ed869-124">**szURL**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-125">URL per il collegamento di AppHelp online.</span><span class="sxs-lookup"><span data-stu-id="ed869-125">The URL for Apphelp online link.</span></span>

</dd> <dt>

<span data-ttu-id="ed869-126">**szLink**</span><span class="sxs-lookup"><span data-stu-id="ed869-126">**szLink**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-127">Testo del collegamento per **szURL**.</span><span class="sxs-lookup"><span data-stu-id="ed869-127">The link text for **szURL**.</span></span>

</dd> <dt>

<span data-ttu-id="ed869-128">**szAppTitle**</span><span class="sxs-lookup"><span data-stu-id="ed869-128">**szAppTitle**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-129">Titolo del messaggio AppHelp.</span><span class="sxs-lookup"><span data-stu-id="ed869-129">The title for the Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="ed869-130">**szContact**</span><span class="sxs-lookup"><span data-stu-id="ed869-130">**szContact**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-131">Informazioni di contatto del fornitore.</span><span class="sxs-lookup"><span data-stu-id="ed869-131">The vendor contact information.</span></span>

</dd> <dt>

<span data-ttu-id="ed869-132">**szDetails**</span><span class="sxs-lookup"><span data-stu-id="ed869-132">**szDetails**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-133">Messaggio AppHelp dettagliato.</span><span class="sxs-lookup"><span data-stu-id="ed869-133">The detailed Apphelp message.</span></span>

</dd> <dt>

<span data-ttu-id="ed869-134">**dwData**</span><span class="sxs-lookup"><span data-stu-id="ed869-134">**dwData**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-135">Dati definiti dall'utente gestiti dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="ed869-135">User-defined data managed by the application.</span></span>

</dd> <dt>

<span data-ttu-id="ed869-136">**bSPEntry**</span><span class="sxs-lookup"><span data-stu-id="ed869-136">**bSPEntry**</span></span>
</dt> <dd>

<span data-ttu-id="ed869-137">Questo membro è **true** se questa voce si trova nel database di Service Pack e **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="ed869-137">This member is **TRUE** if this entry is in the service pack database and **FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ed869-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ed869-138">Requirements</span></span>



| <span data-ttu-id="ed869-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed869-139">Requirement</span></span> | <span data-ttu-id="ed869-140">Valore</span><span class="sxs-lookup"><span data-stu-id="ed869-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ed869-141">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed869-141">Minimum supported client</span></span><br/> | <span data-ttu-id="ed869-142">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ed869-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ed869-143">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ed869-143">Minimum supported server</span></span><br/> | <span data-ttu-id="ed869-144">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ed869-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ed869-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ed869-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed869-146">**SdbReadApphelpDetailsData**</span><span class="sxs-lookup"><span data-stu-id="ed869-146">**SdbReadApphelpDetailsData**</span></span>](sdbreadapphelpdetailsdata.md)
</dt> </dl>

 

 




