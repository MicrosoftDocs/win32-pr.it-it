---
title: Struttura GUESTOSVERSIONINFOEX (VPCCOMInterfaces. h)
description: Contiene informazioni sulla versione del sistema operativo per il sistema operativo guest.
ms.assetid: 9cfd5cac-c8ea-4e09-ba47-3563554bdafa
keywords:
- Struttura GUESTOSVERSIONINFOEX Virtual PC
topic_type:
- apiref
api_name:
- GUESTOSVERSIONINFOEX
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b633838affb9a9ff1453a0c49de9588428b038fe
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104120170"
---
# <a name="guestosversioninfoex-structure"></a><span data-ttu-id="19bcb-104">Struttura GUESTOSVERSIONINFOEX</span><span class="sxs-lookup"><span data-stu-id="19bcb-104">GUESTOSVERSIONINFOEX structure</span></span>

<span data-ttu-id="19bcb-105">\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8.</span><span class="sxs-lookup"><span data-stu-id="19bcb-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="19bcb-106">Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="19bcb-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="19bcb-107">Contiene informazioni sulla versione del sistema operativo per il sistema operativo guest.</span><span class="sxs-lookup"><span data-stu-id="19bcb-107">Contains operating system version information for the guest operating system.</span></span>

## <a name="syntax"></a><span data-ttu-id="19bcb-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="19bcb-108">Syntax</span></span>


```C++
typedef struct _GUESTOSVERSIONINFOEX {
  long    dwOSVersionInfoSize;
  long    dwMajorVersion;
  long    dwMinorVersion;
  long    dwBuildNumber;
  long    dwPlatformId;
  wchar_t szCSDVersion[128];
  short   wServicePackMajor;
  short   wServicePackMinor;
  short   wSuiteMask;
  byte    wProductType;
  byte    wReserved;
} GUESTOSVERSIONINFOEX;
```



## <a name="members"></a><span data-ttu-id="19bcb-109">Members</span><span class="sxs-lookup"><span data-stu-id="19bcb-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="19bcb-110">**dwOSVersionInfoSize**</span><span class="sxs-lookup"><span data-stu-id="19bcb-110">**dwOSVersionInfoSize**</span></span>
</dt> <dd>

<span data-ttu-id="19bcb-111">Dimensioni in byte della struttura di dati.</span><span class="sxs-lookup"><span data-stu-id="19bcb-111">The size of this data structure, in bytes.</span></span> <span data-ttu-id="19bcb-112">Impostare questo membro su `sizeof(GUESTOSVERSIONINFOEX)` .</span><span class="sxs-lookup"><span data-stu-id="19bcb-112">Set this member to `sizeof(GUESTOSVERSIONINFOEX)`.</span></span>

</dd> <dt>

<span data-ttu-id="19bcb-113">**dwMajorVersion**</span><span class="sxs-lookup"><span data-stu-id="19bcb-113">**dwMajorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="19bcb-114">Numero di versione principale.</span><span class="sxs-lookup"><span data-stu-id="19bcb-114">The major version number.</span></span>

</dd> <dt>

<span data-ttu-id="19bcb-115">**dwMinorVersion**</span><span class="sxs-lookup"><span data-stu-id="19bcb-115">**dwMinorVersion**</span></span>
</dt> <dd>

<span data-ttu-id="19bcb-116">Numero di versione secondario.</span><span class="sxs-lookup"><span data-stu-id="19bcb-116">The minor version number.</span></span>

</dd> <dt>

<span data-ttu-id="19bcb-117">**dwBuildNumber**</span><span class="sxs-lookup"><span data-stu-id="19bcb-117">**dwBuildNumber**</span></span>
</dt> <dd>

<span data-ttu-id="19bcb-118">Numero di build.</span><span class="sxs-lookup"><span data-stu-id="19bcb-118">The build number.</span></span>

</dd> <dt>

<span data-ttu-id="19bcb-119">**dwPlatformId**</span><span class="sxs-lookup"><span data-stu-id="19bcb-119">**dwPlatformId**</span></span>
</dt> <dd>

<span data-ttu-id="19bcb-120">Piattaforma del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="19bcb-120">The operating system platform.</span></span> <span data-ttu-id="19bcb-121">Questo membro può essere **una \_ piattaforma ver \_ Win32 \_ NT** (2).</span><span class="sxs-lookup"><span data-stu-id="19bcb-121">This member can be **VER\_PLATFORM\_WIN32\_NT** (2).</span></span>

</dd> <dt>

<span data-ttu-id="19bcb-122">**szCSDVersion**</span><span class="sxs-lookup"><span data-stu-id="19bcb-122">**szCSDVersion**</span></span>
</dt> <dd>

<span data-ttu-id="19bcb-123">Stringa con terminazione null, ad esempio "Service Pack 3", che indica il Service Pack più recente installato nel sistema.</span><span class="sxs-lookup"><span data-stu-id="19bcb-123">A null-terminated string, such as "Service Pack 3", that indicates the latest Service Pack installed on the system.</span></span> <span data-ttu-id="19bcb-124">Se non è stato installato alcun Service Pack, la stringa è vuota.</span><span class="sxs-lookup"><span data-stu-id="19bcb-124">If no Service Pack has been installed, the string is empty.</span></span>

</dd> <dt>

<span data-ttu-id="19bcb-125">**wServicePackMajor**</span><span class="sxs-lookup"><span data-stu-id="19bcb-125">**wServicePackMajor**</span></span>
</dt> <dd>

<span data-ttu-id="19bcb-126">Il numero di versione principale del Service Pack più recente installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-126">The major version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="19bcb-127">**wServicePackMinor**</span><span class="sxs-lookup"><span data-stu-id="19bcb-127">**wServicePackMinor**</span></span>
</dt> <dd>

<span data-ttu-id="19bcb-128">Il numero di versione secondario del Service Pack più recente installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-128">The minor version number of the latest Service Pack installed.</span></span>

</dd> <dt>

<span data-ttu-id="19bcb-129">**wSuiteMask**</span><span class="sxs-lookup"><span data-stu-id="19bcb-129">**wSuiteMask**</span></span>
</dt> <dd>

<span data-ttu-id="19bcb-130">Maschera di maschera che identifica i gruppi di prodotti disponibili nel sistema.</span><span class="sxs-lookup"><span data-stu-id="19bcb-130">A bitmask that identifies the product suites available on the system.</span></span> <span data-ttu-id="19bcb-131">Questo membro può essere una combinazione dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="19bcb-131">This member can be a combination of the following values.</span></span>



| <span data-ttu-id="19bcb-132">Valore</span><span class="sxs-lookup"><span data-stu-id="19bcb-132">Value</span></span>                                                                                                                                                                                                                                                                                          | <span data-ttu-id="19bcb-133">Significato</span><span class="sxs-lookup"><span data-stu-id="19bcb-133">Meaning</span></span>                                                                                                                                                                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_SUITE_BACKOFFICE"></span><span id="ver_suite_backoffice"></span><dl> <span data-ttu-id="19bcb-134"><dt>**Ver \_ SUITE \_ BackOffice**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-134"><dt>**VER\_SUITE\_BACKOFFICE**</dt> <dt>0x00000004</dt></span></span> </dl>                                            | <span data-ttu-id="19bcb-135">Microsoft BackOffice Components è installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-135">Microsoft BackOffice components are installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_BLADE"></span><span id="ver_suite_blade"></span><dl> <span data-ttu-id="19bcb-136"><dt>**Ver \_ 0x00000400 \_ Blade Suite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-136"><dt>**VER\_SUITE\_BLADE**</dt> <dt>0x00000400</dt></span></span> </dl>                                                           | <span data-ttu-id="19bcb-137">Windows Server 2003, Web Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-137">Windows Server 2003, Web Edition is installed.</span></span><br/>                                                                                                                                                         |
| <span id="VER_SUITE_COMPUTE_SERVER"></span><span id="ver_suite_compute_server"></span><dl> <span data-ttu-id="19bcb-138"><dt>**Ver \_ \_ \_ Server di calcolo Suite**</dt> <dt>0x00004000</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-138"><dt>**VER\_SUITE\_COMPUTE\_SERVER**</dt> <dt>0x00004000</dt></span></span> </dl>                               | <span data-ttu-id="19bcb-139">Windows Server 2003, Compute Cluster Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-139">Windows Server 2003, Compute Cluster Edition is installed.</span></span><br/>                                                                                                                                             |
| <span id="VER_SUITE_DATACENTER"></span><span id="ver_suite_datacenter"></span><dl> <span data-ttu-id="19bcb-140"><dt>**Ver \_ SUITE \_ datacenter**</dt> <dt>0x00000080</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-140"><dt>**VER\_SUITE\_DATACENTER**</dt> <dt>0x00000080</dt></span></span> </dl>                                            | <span data-ttu-id="19bcb-141">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition o Windows 2000 Datacenter Server è installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-141">Windows Server 2008 Datacenter, Windows Server 2003, Datacenter Edition, or Windows 2000 Datacenter Server is installed.</span></span><br/>                                                                               |
| <span id="VER_SUITE_ENTERPRISE"></span><span id="ver_suite_enterprise"></span><dl> <span data-ttu-id="19bcb-142"><dt>**Ver \_ SUITE \_ Enterprise**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-142"><dt>**VER\_SUITE\_ENTERPRISE**</dt> <dt>0x00000002</dt></span></span> </dl>                                            | <span data-ttu-id="19bcb-143">Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition o Windows 2000 Advanced Server è installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-143">Windows Server 2008 Enterprise, Windows Server 2003, Enterprise Edition, or Windows 2000 Advanced Server is installed.</span></span> <span data-ttu-id="19bcb-144">Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="19bcb-144">Refer to the Remarks section for more information about this bit flag.</span></span><br/>          |
| <span id="VER_SUITE_EMBEDDEDNT"></span><span id="ver_suite_embeddednt"></span><dl> <span data-ttu-id="19bcb-145"><dt>**Ver \_ SUITE \_ EMBEDDEDNT**</dt> <dt>0x00000040</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-145"><dt>**VER\_SUITE\_EMBEDDEDNT**</dt> <dt>0x00000040</dt></span></span> </dl>                                            | <span data-ttu-id="19bcb-146">Windows XP Embedded è installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-146">Windows XP Embedded is installed.</span></span><br/>                                                                                                                                                                      |
| <span id="VER_SUITE_PERSONAL"></span><span id="ver_suite_personal"></span><dl> <span data-ttu-id="19bcb-147"><dt>**Ver \_ 0x00000200 \_ personali Suite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-147"><dt>**VER\_SUITE\_PERSONAL**</dt> <dt>0x00000200</dt></span></span> </dl>                                                  | <span data-ttu-id="19bcb-148">Windows Vista Home Premium, Windows Vista Home Basic o Windows XP Home Edition è installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-148">Windows Vista Home Premium, Windows Vista Home Basic, or Windows XP Home Edition is installed.</span></span><br/>                                                                                                         |
| <span id="VER_SUITE_SINGLEUSERTS"></span><span id="ver_suite_singleuserts"></span><dl> <span data-ttu-id="19bcb-149"><dt>**Ver \_ SUITE \_ SINGLEUSERTS**</dt> <dt>0x00000100</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-149"><dt>**VER\_SUITE\_SINGLEUSERTS**</dt> <dt>0x00000100</dt></span></span> </dl>                                      | <span data-ttu-id="19bcb-150">Desktop remoto è supportato, ma è supportata una sola sessione interattiva.</span><span class="sxs-lookup"><span data-stu-id="19bcb-150">Remote Desktop is supported, but only one interactive session is supported.</span></span> <span data-ttu-id="19bcb-151">Questo valore viene impostato a meno che il sistema non sia in esecuzione in modalità server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="19bcb-151">This value is set unless the system is running in application server mode.</span></span><br/>                                                 |
| <span id="VER_SUITE_SMALLBUSINESS"></span><span id="ver_suite_smallbusiness"></span><dl> <span data-ttu-id="19bcb-152"><dt>**Ver \_ SUITE \_ SMALLBUSINESS**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-152"><dt>**VER\_SUITE\_SMALLBUSINESS**</dt> <dt>0x00000001</dt></span></span> </dl>                                   | <span data-ttu-id="19bcb-153">Microsoft Small Business Server è stato installato nel sistema, ma potrebbe essere stato aggiornato a un'altra versione di Windows.</span><span class="sxs-lookup"><span data-stu-id="19bcb-153">Microsoft Small Business Server was once installed on the system, but may have been upgraded to another version of Windows.</span></span> <span data-ttu-id="19bcb-154">Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="19bcb-154">Refer to the Remarks section for more information about this bit flag.</span></span><br/>     |
| <span id="VER_SUITE_SMALLBUSINESS_RESTRICTED"></span><span id="ver_suite_smallbusiness_restricted"></span><dl> <span data-ttu-id="19bcb-155"><dt>**Ver \_ SUITE \_ SMALLBUSINESS con \_ restrizioni**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-155"><dt>**VER\_SUITE\_SMALLBUSINESS\_RESTRICTED**</dt> <dt>0x00000020</dt></span></span> </dl> | <span data-ttu-id="19bcb-156">Microsoft Small Business Server viene installato con la licenza client restrittiva in vigore.</span><span class="sxs-lookup"><span data-stu-id="19bcb-156">Microsoft Small Business Server is installed with the restrictive client license in force.</span></span> <span data-ttu-id="19bcb-157">Per ulteriori informazioni su questo flag di bit, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="19bcb-157">Refer to the Remarks section for more information about this bit flag.</span></span><br/>                                      |
| <span id="VER_SUITE_STORAGE_SERVER"></span><span id="ver_suite_storage_server"></span><dl> <span data-ttu-id="19bcb-158"><dt>**Ver \_ SUITE \_ storage \_ server**</dt> <dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-158"><dt>**VER\_SUITE\_STORAGE\_SERVER**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="19bcb-159">Windows Storage Server 2003 R2 o Windows Storage Server 2003 è installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-159">Windows Storage Server 2003 R2 or Windows Storage Server 2003is installed.</span></span><br/>                                                                                                                             |
| <span id="VER_SUITE_TERMINAL"></span><span id="ver_suite_terminal"></span><dl> <span data-ttu-id="19bcb-160"><dt>**Ver \_ 0x00000010 \_ terminale Suite**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-160"><dt>**VER\_SUITE\_TERMINAL**</dt> <dt>0x00000010</dt></span></span> </dl>                                                  | <span data-ttu-id="19bcb-161">Servizi terminal è installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-161">Terminal Services is installed.</span></span> <span data-ttu-id="19bcb-162">Questo valore è sempre impostato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-162">This value is always set.</span></span><br/> <span data-ttu-id="19bcb-163">Se è impostato il **\_ \_ terminale ver Suite** , ma **ver \_ Suite \_ SINGLEUSERTS** non è impostato, il sistema viene eseguito in modalità server applicazioni.</span><span class="sxs-lookup"><span data-stu-id="19bcb-163">If **VER\_SUITE\_TERMINAL** is set but **VER\_SUITE\_SINGLEUSERTS** is not set, the system is running in application server mode.</span></span><br/> |
| <span id="VER_SUITE_WH_SERVER"></span><span id="ver_suite_wh_server"></span><dl> <span data-ttu-id="19bcb-164"><dt>**Ver \_ 0x00008000 gruppo di \_ \_ server wh**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-164"><dt>**VER\_SUITE\_WH\_SERVER**</dt> <dt>0x00008000</dt></span></span> </dl>                                              | <span data-ttu-id="19bcb-165">Windows Home Server è installato.</span><span class="sxs-lookup"><span data-stu-id="19bcb-165">Windows Home Server is installed.</span></span><br/>                                                                                                                                                                      |



 

</dd> <dt>

<span data-ttu-id="19bcb-166">**wProductType**</span><span class="sxs-lookup"><span data-stu-id="19bcb-166">**wProductType**</span></span>
</dt> <dd>

<span data-ttu-id="19bcb-167">Eventuali ulteriori informazioni sul sistema.</span><span class="sxs-lookup"><span data-stu-id="19bcb-167">Any additional information about the system.</span></span> <span data-ttu-id="19bcb-168">Il membro può essere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="19bcb-168">This member can be one of the following values.</span></span>



| <span data-ttu-id="19bcb-169">Valore</span><span class="sxs-lookup"><span data-stu-id="19bcb-169">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="19bcb-170">Significato</span><span class="sxs-lookup"><span data-stu-id="19bcb-170">Meaning</span></span>                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="VER_NT_DOMAIN_CONTROLLER"></span><span id="ver_nt_domain_controller"></span><dl> <span data-ttu-id="19bcb-171"><dt>**Ver \_ \_ \_ Controller di dominio NT**</dt> <dt>0x0000002</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-171"><dt>**VER\_NT\_DOMAIN\_CONTROLLER**</dt> <dt>0x0000002</dt></span></span> </dl> | <span data-ttu-id="19bcb-172">Il sistema è un controller di dominio e il sistema operativo è Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="19bcb-172">The system is a domain controller and the operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/>                                                                                                   |
| <span id="VER_NT_SERVER"></span><span id="ver_nt_server"></span><dl> <span data-ttu-id="19bcb-173"><dt>**Ver \_ NT \_ Server**</dt> <dt>0x0000003</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-173"><dt>**VER\_NT\_SERVER**</dt> <dt>0x0000003</dt></span></span> </dl>                                   | <span data-ttu-id="19bcb-174">Il sistema operativo è Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003 o Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="19bcb-174">The operating system is Windows Server 2008 R2, Windows Server 2008, Windows Server 2003 R2, Windows Server 2003, or Windows 2000 Server.</span></span><br/> <span data-ttu-id="19bcb-175">Si noti che un server che è anche un controller di dominio viene segnalato come **\_ controller di \_ dominio \_ ver NT**, non come **\_ \_ Server ver NT**.</span><span class="sxs-lookup"><span data-stu-id="19bcb-175">Note that a server that is also a domain controller is reported as **VER\_NT\_DOMAIN\_CONTROLLER**, not **VER\_NT\_SERVER**.</span></span><br/> |
| <span id="VER_NT_WORKSTATION"></span><span id="ver_nt_workstation"></span><dl> <span data-ttu-id="19bcb-176"><dt>**Ver \_ \_Workstation NT**</dt> <dt>0x0000001</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-176"><dt>**VER\_NT\_WORKSTATION**</dt> <dt>0x0000001</dt></span></span> </dl>                    | <span data-ttu-id="19bcb-177">Il sistema operativo è Windows 7, Windows Vista, Windows XP o Windows 2000 Professional.</span><span class="sxs-lookup"><span data-stu-id="19bcb-177">The operating system is Windows 7, Windows Vista, Windows XP, or Windows 2000 Professional.</span></span><br/>                                                                                                                                                                                       |



 

</dd> <dt>

<span data-ttu-id="19bcb-178">**wReserved**</span><span class="sxs-lookup"><span data-stu-id="19bcb-178">**wReserved**</span></span>
</dt> <dd>

<span data-ttu-id="19bcb-179">Riservato per utilizzi futuri.</span><span class="sxs-lookup"><span data-stu-id="19bcb-179">Reserved for future use.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="19bcb-180">Requisiti</span><span class="sxs-lookup"><span data-stu-id="19bcb-180">Requirements</span></span>



| <span data-ttu-id="19bcb-181">Requisito</span><span class="sxs-lookup"><span data-stu-id="19bcb-181">Requirement</span></span> | <span data-ttu-id="19bcb-182">Valore</span><span class="sxs-lookup"><span data-stu-id="19bcb-182">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19bcb-183">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19bcb-183">Minimum supported client</span></span><br/> | <span data-ttu-id="19bcb-184">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="19bcb-184">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19bcb-185">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="19bcb-185">Minimum supported server</span></span><br/> | <span data-ttu-id="19bcb-186">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="19bcb-186">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="19bcb-187">Fine del supporto client</span><span class="sxs-lookup"><span data-stu-id="19bcb-187">End of client support</span></span><br/>    | <span data-ttu-id="19bcb-188">Windows 7</span><span class="sxs-lookup"><span data-stu-id="19bcb-188">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="19bcb-189">Prodotto</span><span class="sxs-lookup"><span data-stu-id="19bcb-189">Product</span></span><br/>                  | <span data-ttu-id="19bcb-190">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="19bcb-190">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="19bcb-191">Intestazione</span><span class="sxs-lookup"><span data-stu-id="19bcb-191">Header</span></span><br/>                   | <dl> <span data-ttu-id="19bcb-192"><dt>VPCCOMInterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="19bcb-192"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="19bcb-193">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="19bcb-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19bcb-194">**IVMGuestOS::GetOsVersionInfo**</span><span class="sxs-lookup"><span data-stu-id="19bcb-194">**IVMGuestOS::GetOsVersionInfo**</span></span>](ivmguestos-getosversioninfo.md)
</dt> </dl>

 

