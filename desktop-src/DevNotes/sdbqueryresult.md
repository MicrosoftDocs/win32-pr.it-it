---
description: Contiene i risultati dell'esecuzione di una query sul database di shim per un eseguibile corrispondente.
ms.assetid: 6e6df118-fb64-4a97-9280-050e3b4e3a4b
title: Struttura SDBQUERYRESULT
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SDBQUERYRESULT
api_type:
- NA
api_location: ''
ms.openlocfilehash: 9c631438d36116d47bfcb8675c390fb2974271c8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966034"
---
# <a name="sdbqueryresult-structure"></a><span data-ttu-id="b6234-103">Struttura SDBQUERYRESULT</span><span class="sxs-lookup"><span data-stu-id="b6234-103">SDBQUERYRESULT structure</span></span>

<span data-ttu-id="b6234-104">Contiene i risultati dell'esecuzione di una query sul database di shim per un eseguibile corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b6234-104">Contains the results from querying the shim database for a matching executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="b6234-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b6234-105">Syntax</span></span>


```C++
typedef struct tagSDBQUERYRESULT {
  TAGREF atrExes[SDB_MAX_EXES];
  DWORD  adwExeFlags[SDB_MAX_EXES];
  TAGREF atrLayers[SDB_MAX_LAYERS];
  DWORD  dwLayerFlags;
  TAGREF trApphelp;
  DWORD  dwExeCount;
  DWORD  dwLayerCount;
  GUID   guidID;
  DWORD  dwFlags;
  DWORD  dwCustomSDBMap;
  GUID   rgGuidDB[SDB_MAX_SDBS];
} SDBQUERYRESULT, *PSDBQUERYRESULT;
```



## <a name="members"></a><span data-ttu-id="b6234-106">Members</span><span class="sxs-lookup"><span data-stu-id="b6234-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="b6234-107">**atrExes**</span><span class="sxs-lookup"><span data-stu-id="b6234-107">**atrExes**</span></span>
</dt> <dd>

<span data-ttu-id="b6234-108">Valori **TAGREF** dei file eseguibili corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="b6234-108">The **TAGREF** values of the matching executable files.</span></span> <span data-ttu-id="b6234-109">Si noti che **sdb \_ Max \_ exe** viene definito come 16.</span><span class="sxs-lookup"><span data-stu-id="b6234-109">Note that **SDB\_MAX\_EXES** is defined as 16.</span></span>

</dd> <dt>

<span data-ttu-id="b6234-110">**adwExeFlags**</span><span class="sxs-lookup"><span data-stu-id="b6234-110">**adwExeFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b6234-111">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b6234-111">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b6234-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Disabilita \_ shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="b6234-112"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DISABILITARE \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="b6234-113"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="b6234-114"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annullamento APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="b6234-115"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Disabilita \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="b6234-116"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DISABLE \_ Layer** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="b6234-117"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Disabilita \_ driver** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="b6234-118"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b6234-119">**atrLayers**</span><span class="sxs-lookup"><span data-stu-id="b6234-119">**atrLayers**</span></span>
</dt> <dd>

<span data-ttu-id="b6234-120">Valori **TAGREF** dei livelli corrispondenti.</span><span class="sxs-lookup"><span data-stu-id="b6234-120">The **TAGREF** values of the matching layers.</span></span> <span data-ttu-id="b6234-121">Si noti che i **\_ \_ livelli SDB max** sono definiti come 8.</span><span class="sxs-lookup"><span data-stu-id="b6234-121">Note that **SDB\_MAX\_LAYERS** is defined as 8.</span></span>

</dd> <dt>

<span data-ttu-id="b6234-122">**dwLayerFlags**</span><span class="sxs-lookup"><span data-stu-id="b6234-122">**dwLayerFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b6234-123">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b6234-123">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b6234-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Disabilita \_ shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="b6234-124"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DISABILITARE \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="b6234-125"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="b6234-126"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annullamento APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="b6234-127"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Disabilita \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="b6234-128"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DISABLE \_ Layer** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="b6234-129"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Disabilita \_ driver** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="b6234-130"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b6234-131">**trApphelp**</span><span class="sxs-lookup"><span data-stu-id="b6234-131">**trApphelp**</span></span>
</dt> <dd>

<span data-ttu-id="b6234-132">Valore **TAGREF** del messaggio AppHelp del file eseguibile corrispondente.</span><span class="sxs-lookup"><span data-stu-id="b6234-132">The **TAGREF** value of the apphelp message of the corresponding executable.</span></span>

</dd> <dt>

<span data-ttu-id="b6234-133">**dwExeCount**</span><span class="sxs-lookup"><span data-stu-id="b6234-133">**dwExeCount**</span></span>
</dt> <dd>

<span data-ttu-id="b6234-134">Numero di elementi in **atrExes**.</span><span class="sxs-lookup"><span data-stu-id="b6234-134">The number of elements in **atrExes**.</span></span>

</dd> <dt>

<span data-ttu-id="b6234-135">**dwLayerCount**</span><span class="sxs-lookup"><span data-stu-id="b6234-135">**dwLayerCount**</span></span>
</dt> <dd>

<span data-ttu-id="b6234-136">Numero di elementi in **atrLayers**.</span><span class="sxs-lookup"><span data-stu-id="b6234-136">The number of elements in **atrLayers**.</span></span>

</dd> <dt>

<span data-ttu-id="b6234-137">**guidID**</span><span class="sxs-lookup"><span data-stu-id="b6234-137">**guidID**</span></span>
</dt> <dd>

<span data-ttu-id="b6234-138">GUID dell'ultimo file eseguibile.</span><span class="sxs-lookup"><span data-stu-id="b6234-138">The GUID of the last executable file.</span></span>

</dd> <dt>

<span data-ttu-id="b6234-139">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="b6234-139">**dwFlags**</span></span>
</dt> <dd>

<span data-ttu-id="b6234-140">Il parametro può essere costituito da uno o più dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="b6234-140">This parameter can be one or more of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="b6234-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG \_ Disabilita \_ shim** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="b6234-141"><span id="SHIMREG_DISABLE_SHIM"></span><span id="shimreg_disable_shim"></span>**SHIMREG\_DISABLE\_SHIM** (0x00000001)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG \_ DISABILITARE \_ APPHELP** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="b6234-142"><span id="SHIMREG_DISABLE_APPHELP"></span><span id="shimreg_disable_apphelp"></span>**SHIMREG\_DISABLE\_APPHELP** (0x00000002)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG \_ APPHELP \_ NOUI** (0x00000004)</span><span class="sxs-lookup"><span data-stu-id="b6234-143"><span id="SHIMREG_APPHELP_NOUI"></span><span id="shimreg_apphelp_noui"></span>**SHIMREG\_APPHELP\_NOUI** (0x00000004)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG \_ \_Annullamento APPHELP** (0x10000000)</span><span class="sxs-lookup"><span data-stu-id="b6234-144"><span id="SHIMREG_APPHELP_CANCEL"></span><span id="shimreg_apphelp_cancel"></span>**SHIMREG\_APPHELP\_CANCEL** (0x10000000)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG \_ Disabilita \_ SxS** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="b6234-145"><span id="SHIMREG_DISABLE_SXS"></span><span id="shimreg_disable_sxs"></span>**SHIMREG\_DISABLE\_SXS** (0x00000010)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG \_ DISABLE \_ Layer** (0x00000020)</span><span class="sxs-lookup"><span data-stu-id="b6234-146"><span id="SHIMREG_DISABLE_LAYER"></span><span id="shimreg_disable_layer"></span>**SHIMREG\_DISABLE\_LAYER** (0x00000020)</span></span>
</dt> <dt>

<span data-ttu-id="b6234-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG \_ Disabilita \_ driver** (0x00000040)</span><span class="sxs-lookup"><span data-stu-id="b6234-147"><span id="SHIMREG_DISABLE_DRIVER"></span><span id="shimreg_disable_driver"></span>**SHIMREG\_DISABLE\_DRIVER** (0x00000040)</span></span>
</dt> </dl> </dd> <dt>

<span data-ttu-id="b6234-148">**dwCustomSDBMap**</span><span class="sxs-lookup"><span data-stu-id="b6234-148">**dwCustomSDBMap**</span></span>
</dt> <dd>

<span data-ttu-id="b6234-149">Mappa dei database di shim personalizzati.</span><span class="sxs-lookup"><span data-stu-id="b6234-149">A map of the custom shim databases.</span></span> <span data-ttu-id="b6234-150">I bit corrispondenti vengono impostati se **rgGuidDB** è valido.</span><span class="sxs-lookup"><span data-stu-id="b6234-150">The corresponding bits are set if **rgGuidDB** is valid.</span></span>

</dd> <dt>

<span data-ttu-id="b6234-151">**rgGuidDB**</span><span class="sxs-lookup"><span data-stu-id="b6234-151">**rgGuidDB**</span></span>
</dt> <dd>

<span data-ttu-id="b6234-152">GUID dei database shim.</span><span class="sxs-lookup"><span data-stu-id="b6234-152">The GUIDs of the shim databases.</span></span> <span data-ttu-id="b6234-153">Si noti che **sdb \_ Max \_ SDB** è definito come 16.</span><span class="sxs-lookup"><span data-stu-id="b6234-153">Note that **SDB\_MAX\_SDBS** is defined as 16.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b6234-154">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b6234-154">Requirements</span></span>



| <span data-ttu-id="b6234-155">Requisito</span><span class="sxs-lookup"><span data-stu-id="b6234-155">Requirement</span></span> | <span data-ttu-id="b6234-156">Valore</span><span class="sxs-lookup"><span data-stu-id="b6234-156">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b6234-157">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6234-157">Minimum supported client</span></span><br/> | <span data-ttu-id="b6234-158">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b6234-158">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b6234-159">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b6234-159">Minimum supported server</span></span><br/> | <span data-ttu-id="b6234-160">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b6234-160">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b6234-161">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b6234-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b6234-162">**SdbGetMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="b6234-162">**SdbGetMatchingExe**</span></span>](sdbgetmatchingexe.md)
</dt> </dl>

 

 




