---
title: Metodo FileAssociations della classe Win32_TSApplicationFileExtensions
description: Analizza il registro di sistema per ottenere le associazioni di file correnti per un'applicazione.
ms.assetid: d2c55b59-f3aa-401b-b176-b287c2e26192
ms.tgt_platform: multiple
keywords:
- Metodo FileAssociations Servizi Desktop remoto
- Servizi Desktop remoto del metodo FileAssociations, classe Win32_TSApplicationFileExtensions
- Classe Win32_TSApplicationFileExtensions Servizi Desktop remoto, metodo FileAssociations
topic_type:
- apiref
api_name:
- Win32_TSApplicationFileExtensions.FileAssociations
api_location:
- TsPubWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23ee60033344c0c448d82680bdcacfc24cb4f214
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302476"
---
# <a name="fileassociations-method-of-the-win32_tsapplicationfileextensions-class"></a><span data-ttu-id="fac2b-106">Metodo FileAssociations della \_ classe TSApplicationFileExtensions di Win32</span><span class="sxs-lookup"><span data-stu-id="fac2b-106">FileAssociations method of the Win32\_TSApplicationFileExtensions class</span></span>

<span data-ttu-id="fac2b-107">Analizza il registro di sistema per ottenere le associazioni di file correnti per un'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fac2b-107">Scans the registry to get the current file associations for an application.</span></span>

## <a name="syntax"></a><span data-ttu-id="fac2b-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fac2b-108">Syntax</span></span>


```mof
uint32 FileAssociations(
  [in]  string                  AppPath,
  [out] Win32_RDFileAssociation FileAssociations[]
);
```



## <a name="parameters"></a><span data-ttu-id="fac2b-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="fac2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fac2b-110">*Percorso app* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="fac2b-110">*AppPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fac2b-111">Specifica il percorso dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fac2b-111">Specifies the path to the application.</span></span>

</dd> <dt>

<span data-ttu-id="fac2b-112">*FileAssociation* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fac2b-112">*FileAssociations* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fac2b-113">Al termine dell'operazione sono contenute le associazioni di file per l'applicazione.</span><span class="sxs-lookup"><span data-stu-id="fac2b-113">On successful completion contains the file associations for this application.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fac2b-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fac2b-114">Requirements</span></span>



| <span data-ttu-id="fac2b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fac2b-115">Requirement</span></span> | <span data-ttu-id="fac2b-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fac2b-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fac2b-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fac2b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="fac2b-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="fac2b-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fac2b-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="fac2b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="fac2b-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="fac2b-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="fac2b-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="fac2b-121">Namespace</span></span><br/>                | <span data-ttu-id="fac2b-122">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="fac2b-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="fac2b-123">MOF</span><span class="sxs-lookup"><span data-stu-id="fac2b-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fac2b-124"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fac2b-124"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="fac2b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fac2b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fac2b-126"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fac2b-126"><dt>TsPubWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fac2b-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fac2b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fac2b-128">**\_TSApplicationFileExtensions Win32**</span><span class="sxs-lookup"><span data-stu-id="fac2b-128">**Win32\_TSApplicationFileExtensions**</span></span>](win32-tsapplicationfileextensions.md)
</dt> <dt>

[<span data-ttu-id="fac2b-129">**\_RDFileAssociation Win32**</span><span class="sxs-lookup"><span data-stu-id="fac2b-129">**Win32\_RDFileAssociation**</span></span>](win32-rdfileassociation.md)
</dt> </dl>

 

 





