---
title: Metodo CreateUserDiskTemplate della classe Win32_TSSessionDirectory
description: Crea un modello di disco utente.
ms.assetid: 4036a418-b082-4376-a400-16f48b98f071
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo CreateUserDiskTemplate
- Metodo CreateUserDiskTemplate Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo CreateUserDiskTemplate
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.CreateUserDiskTemplate
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e7c142834b4501639499cd0bcf102dadcc1b07d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104119203"
---
# <a name="createuserdisktemplate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="5f347-106">Metodo CreateUserDiskTemplate della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="5f347-106">CreateUserDiskTemplate method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="5f347-107">Crea un modello di disco utente.</span><span class="sxs-lookup"><span data-stu-id="5f347-107">Creates a user disk template.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f347-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5f347-108">Syntax</span></span>


```mof
uint32 CreateUserDiskTemplate(
  [in] string UserDisksStorageUrl,
  [in] uint32 UserDiskMaxSizeInGB
);
```



## <a name="parameters"></a><span data-ttu-id="5f347-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="5f347-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5f347-110">*UserDisksStorageUrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f347-110">*UserDisksStorageUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f347-111">Percorso della condivisione in cui sono archiviati tutti i dischi utente.</span><span class="sxs-lookup"><span data-stu-id="5f347-111">The location of the share where all user disks are stored.</span></span>

</dd> <dt>

<span data-ttu-id="5f347-112">*UserDiskMaxSizeInGB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5f347-112">*UserDiskMaxSizeInGB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5f347-113">Dimensione massima in gigabyte per tutti i dischi utente.</span><span class="sxs-lookup"><span data-stu-id="5f347-113">The maximum size in gigabytes, for all user disks.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5f347-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5f347-114">Requirements</span></span>



| <span data-ttu-id="5f347-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f347-115">Requirement</span></span> | <span data-ttu-id="5f347-116">Valore</span><span class="sxs-lookup"><span data-stu-id="5f347-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5f347-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f347-117">Minimum supported client</span></span><br/> | <span data-ttu-id="5f347-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="5f347-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5f347-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5f347-119">Minimum supported server</span></span><br/> | <span data-ttu-id="5f347-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="5f347-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="5f347-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="5f347-121">Namespace</span></span><br/>                | <span data-ttu-id="5f347-122">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="5f347-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="5f347-123">MOF</span><span class="sxs-lookup"><span data-stu-id="5f347-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5f347-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5f347-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="5f347-125">DLL</span><span class="sxs-lookup"><span data-stu-id="5f347-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5f347-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5f347-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f347-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5f347-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f347-128">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="5f347-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





