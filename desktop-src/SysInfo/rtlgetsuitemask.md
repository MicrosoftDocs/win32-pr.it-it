---
description: Recupera una maschera di bit che identifica i gruppi di prodotti disponibili nel sistema. Se questa funzione viene chiamata in un'applicazione che viene eseguita nel contesto di un silo di server, viene invece recuperata la maschera di gruppo per il silo del server.
ms.assetid: 1D6434FD-D7BD-45F9-B7C3-238890AF9928
title: Funzione RtlGetSuiteMask (ntddk. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlGetSuiteMask
api_type:
- DllExport
api_location:
- ntdll.dll
ms.openlocfilehash: ed8d8906273d18125131251636bc6199d166547b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315298"
---
# <a name="rtlgetsuitemask-function"></a><span data-ttu-id="1ecb9-104">RtlGetSuiteMask (funzione)</span><span class="sxs-lookup"><span data-stu-id="1ecb9-104">RtlGetSuiteMask function</span></span>

<span data-ttu-id="1ecb9-105">\[Alcune informazioni si riferiscono al prodotto pre-rilasciato che può essere modificato in modo sostanziale prima del rilascio commerciale.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-105">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1ecb9-106">Microsoft non riconosce alcuna garanzia, espressa o implicita, in merito alle informazioni qui fornite.\]</span><span class="sxs-lookup"><span data-stu-id="1ecb9-106">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1ecb9-107">Recupera una maschera di bit che identifica i gruppi di prodotti disponibili nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-107">Retrieves a bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="1ecb9-108">Se questa funzione viene chiamata in un'applicazione che viene eseguita nel contesto di un silo di server, viene invece recuperata la maschera di gruppo per il silo del server.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-108">If this function is called in an application that runs in the context of a server silo, the suite mask for the server silo is retrieved instead.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ecb9-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1ecb9-109">Syntax</span></span>


```C++
ULONG NTAPI RtlGetSuiteMask(void);
```



## <a name="parameters"></a><span data-ttu-id="1ecb9-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="1ecb9-110">Parameters</span></span>

<span data-ttu-id="1ecb9-111">Questa funzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1ecb9-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ecb9-112">Return value</span></span>

<span data-ttu-id="1ecb9-113">Maschera di bit che identifica i gruppi di prodotti disponibili nel sistema.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-113">A bit mask that identifies the product suites available on the system.</span></span> <span data-ttu-id="1ecb9-114">La maschera di bit può includere i valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-114">The bit mask can include the following values.</span></span>



| <span data-ttu-id="1ecb9-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1ecb9-115">Return value</span></span>                                                                          | <span data-ttu-id="1ecb9-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="1ecb9-116">Description</span></span>                                                                                                                                                                                                                                             |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1ecb9-117"><dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-117"><dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="1ecb9-118">Microsoft Small Business Server è stato installato nel sistema, ma potrebbe essere stato aggiornato a un'altra versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-118">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="1ecb9-119">Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-119">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                           |
| <dl> <span data-ttu-id="1ecb9-120"><dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-120"><dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="1ecb9-121">Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server è installato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-121">Windows 10 Enterprise, Windows 8.1 Enterprise, Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="1ecb9-122">Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-122">Refer to the Remarks section for more information about this bit flag.</span></span><br/> |
| <dl> <span data-ttu-id="1ecb9-123"><dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-123"><dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="1ecb9-124">Microsoft BackOffice Components è installato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-124">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="1ecb9-125"><dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-125"><dt>0x00000008</dt></span></span> </dl> | <span data-ttu-id="1ecb9-126">Communications Server 2003, Communications Server 2005, Communications Server 2007 o Communications Server 2007 R2 è installato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-126">Communications Server 2003, Communications Server 2005, Communications Server 2007, or Communications Server 2007 R2 is installed.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="1ecb9-127"><dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-127"><dt>0x00000010</dt></span></span> </dl> | <span data-ttu-id="1ecb9-128">Servizi terminal è installato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-128">Terminal Services is installed.</span></span> <span data-ttu-id="1ecb9-129">Questo valore è sempre impostato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-129">This value is always set.</span></span><br/> <span data-ttu-id="1ecb9-130">Se **TerminalServer** è impostato ma **SingleUserTS** non è impostato, il sistema viene eseguito in modalità server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-130">If **TerminalServer** is set but **SingleUserTS** is not set, the system is running in application server mode.</span></span><br/>                                                         |
| <dl> <span data-ttu-id="1ecb9-131"><dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-131"><dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="1ecb9-132">Microsoft Small Business Server viene installato con la licenza client restrittiva in vigore.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-132">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="1ecb9-133">Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-133">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                                                            |
| <dl> <span data-ttu-id="1ecb9-134"><dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-134"><dt>0x00000040</dt></span></span> </dl> | <span data-ttu-id="1ecb9-135">Windows XP Embedded è installato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-135">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="1ecb9-136"><dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-136"><dt>0x00000080</dt></span></span> </dl> | <span data-ttu-id="1ecb9-137">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server è installato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-137">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="1ecb9-138"><dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-138"><dt>0x00000100</dt></span></span> </dl> | <span data-ttu-id="1ecb9-139">Desktop remoto è supportato, ma è supportata una sola sessione interattiva.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-139">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="1ecb9-140">Questo valore viene impostato a meno che il sistema non sia in esecuzione in modalità server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-140">This value is set unless the system is running in application server mode.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="1ecb9-141"><dt>0x00000200</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-141"><dt>0x00000200</dt></span></span> </dl> | <span data-ttu-id="1ecb9-142">Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-142">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                                                               |
| <dl> <span data-ttu-id="1ecb9-143"><dt>0x00000400</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-143"><dt>0x00000400</dt></span></span> </dl> | <span data-ttu-id="1ecb9-144">Windows Server 2003, Web Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-144">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                                                               |
| <dl> <span data-ttu-id="1ecb9-145"><dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-145"><dt>0x00002000</dt></span></span> </dl> | <span data-ttu-id="1ecb9-146">Windows Storage Server 2003 R2 o Windows Storage Server 2003 è installato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-146">Windows Storage Server 2003 R2 or Windows Storage Server 2003 is installed.</span></span><br/>                                                                                                                                                                  |
| <dl> <span data-ttu-id="1ecb9-147"><dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-147"><dt>0x00004000</dt></span></span> </dl> | <span data-ttu-id="1ecb9-148">Windows Server 2003, Compute Cluster Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-148">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                                                                   |
| <dl> <span data-ttu-id="1ecb9-149"><dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-149"><dt>0x00008000</dt></span></span> </dl> | <span data-ttu-id="1ecb9-150">Windows Home Server è installato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-150">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="1ecb9-151">Commenti</span><span class="sxs-lookup"><span data-stu-id="1ecb9-151">Remarks</span></span>

<span data-ttu-id="1ecb9-152">Si consiglia di non basarsi solo sul flag 0x00000001 per determinare se Small Business Server è stato installato nel sistema, poiché sia questo flag che il flag 0x00000020 vengono impostati quando viene installato questo gruppo di prodotti.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-152">You should not rely upon only the 0x00000001 flag to determine whether Small Business Server has been installed on the system, as both this flag and the 0x00000020 flag are set when this product suite is installed.</span></span> <span data-ttu-id="1ecb9-153">Se si aggiorna questa installazione a Windows Server, Standard Edition, il flag 0x00000020 verrà cancellato, tuttavia, il flag 0x00000001 rimarrà impostato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-153">If you upgrade this installation to Windows Server, Standard Edition, the 0x00000020 flag will be cleared however, the 0x00000001 flag will remain set.</span></span> <span data-ttu-id="1ecb9-154">In questo caso, significa che Small Business Server è stato installato in questo sistema.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-154">In this case, this indicates that Small Business Server was once installed on this system.</span></span> <span data-ttu-id="1ecb9-155">Se questa installazione viene aggiornata ulteriormente a Windows Server, Enterprise Edition, il flag 0x00000001 rimarrà impostato.</span><span class="sxs-lookup"><span data-stu-id="1ecb9-155">If this installation is further upgraded to Windows Server, Enterprise Edition, the 0x00000001 flag will remain set.</span></span>

## <a name="requirements"></a><span data-ttu-id="1ecb9-156">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1ecb9-156">Requirements</span></span>



| <span data-ttu-id="1ecb9-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="1ecb9-157">Requirement</span></span> | <span data-ttu-id="1ecb9-158">Valore</span><span class="sxs-lookup"><span data-stu-id="1ecb9-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1ecb9-159">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ecb9-159">Minimum supported client</span></span><br/> | <span data-ttu-id="1ecb9-160">\[Solo app desktop Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="1ecb9-160">Windows 10 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="1ecb9-161">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1ecb9-161">Minimum supported server</span></span><br/> | <span data-ttu-id="1ecb9-162">\[Solo app desktop Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="1ecb9-162">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1ecb9-163">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1ecb9-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ecb9-164"><dt>Ntddk. h</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-164"><dt>Ntddk.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ecb9-165">Libreria</span><span class="sxs-lookup"><span data-stu-id="1ecb9-165">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ecb9-166"><dt>Ntdll. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-166"><dt>Ntdll.lib</dt></span></span> </dl> |
| <span data-ttu-id="1ecb9-167">DLL</span><span class="sxs-lookup"><span data-stu-id="1ecb9-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ecb9-168"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ecb9-168"><dt>Ntdll.dll</dt></span></span> </dl> |



 

 




