---
title: Metodo FileExtensions della classe Win32_TSApplicationFileExtensions
description: Fornisce un elenco delle estensioni dei nomi di file gestite da un'applicazione.
ms.assetid: 833a1b68-86ed-4361-bbcb-a8d1c4a9306d
ms.tgt_platform: multiple
keywords:
- Metodo FileExtensions Servizi Desktop remoto
- Servizi Desktop remoto del metodo FileExtensions, classe Win32_TSApplicationFileExtensions
- Classe Win32_TSApplicationFileExtensions Servizi Desktop remoto, metodo FileExtensions
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileExtensions
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5aa0bff92cdc274c8dba56aa11a44791e3ad9f01
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964818"
---
# <a name="fileextensions-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="184be-106">Metodo FileExtensions della \_ classe TSApplicationFileExtensions di Win32</span><span class="sxs-lookup"><span data-stu-id="184be-106">FileExtensions method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="184be-107">Fornisce un elenco delle estensioni dei nomi di file gestite da un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="184be-107">Provides a list of the file name extensions that are handled by an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="184be-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="184be-108">Syntax</span></span>


```mof
uint32 FileExtensions(
  [in]  string AppPath,
  [out] string Extensions[]
);
```



## <a name="parameters"></a><span data-ttu-id="184be-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="184be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="184be-110">*Percorso app* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="184be-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="184be-111">Percorso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="184be-111">The path of the application.</span></span>

</dd> <dt>

<span data-ttu-id="184be-112">*Estensioni* \[ di out\]</span><span class="sxs-lookup"><span data-stu-id="184be-112">*Extensions* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="184be-113">Estensioni dei nomi di file gestite dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="184be-113">The file name extensions that are handled by the application.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="184be-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="184be-114">Remarks</span></span>

<span data-ttu-id="184be-115">Per chiamare questo metodo, è necessario essere membri del gruppo Administrators.</span><span class="sxs-lookup"><span data-stu-id="184be-115">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="184be-116">I file Managed Object Format (MOF) contengono le definizioni per le classi Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="184be-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="184be-117">I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="184be-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="184be-118">Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager.</span><span class="sxs-lookup"><span data-stu-id="184be-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="184be-119">Per ulteriori informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="184be-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="184be-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="184be-120">Requirements</span></span>



| <span data-ttu-id="184be-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="184be-121">Requirement</span></span> | <span data-ttu-id="184be-122">Valore</span><span class="sxs-lookup"><span data-stu-id="184be-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="184be-123">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="184be-123">Minimum supported client</span></span><br/> | <span data-ttu-id="184be-124">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="184be-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="184be-125">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="184be-125">Minimum supported server</span></span><br/> | <span data-ttu-id="184be-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="184be-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="184be-127">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="184be-127">Namespace</span></span><br/>                | <span data-ttu-id="184be-128">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="184be-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="184be-129">MOF</span><span class="sxs-lookup"><span data-stu-id="184be-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="184be-130"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="184be-130"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="184be-131">DLL</span><span class="sxs-lookup"><span data-stu-id="184be-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="184be-132"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="184be-132"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="184be-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="184be-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="184be-134">**\_TSApplicationFileExtensions Win32**</span><span class="sxs-lookup"><span data-stu-id="184be-134">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> </dl>

 

