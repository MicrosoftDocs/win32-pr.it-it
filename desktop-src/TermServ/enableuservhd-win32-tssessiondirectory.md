---
title: Metodo EnableUserVhd della classe Win32_TSSessionDirectory
description: Abilita un VHD del profilo utente in un server RDSH.
ms.assetid: bb39fa19-38eb-4caf-ae81-2bccd901ee2f
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo EnableUserVhd
- Metodo EnableUserVhd Servizi Desktop remoto, classe Win32_TSSessionDirectory
- Classe Win32_TSSessionDirectory Servizi Desktop remoto, metodo EnableUserVhd
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.EnableUserVhd
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 464e105d2f8f0c80126e6b9ca5e5a383b2d17628
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106302746"
---
# <a name="enableuservhd-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="b8858-106">Metodo EnableUserVhd della \_ classe TSSessionDirectory Win32</span><span class="sxs-lookup"><span data-stu-id="b8858-106">EnableUserVhd method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="b8858-107">Abilita un VHD del profilo utente in un server RDSH.</span><span class="sxs-lookup"><span data-stu-id="b8858-107">Enables a user profile VHD on an RDSH server.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8858-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b8858-108">Syntax</span></span>


```mof
uint32 EnableUserVhd(
  [in] string UvhdShareUrl,
  [in] string UvhdRoamingPolicyXml
);
```



## <a name="parameters"></a><span data-ttu-id="b8858-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="b8858-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8858-110">*UvhdShareUrl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8858-110">*UvhdShareUrl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8858-111">Percorso della condivisione in cui vengono archiviati tutti i dischi rigidi virtuali del profilo utente.</span><span class="sxs-lookup"><span data-stu-id="b8858-111">The location of the share where all user profile VHDs are stored.</span></span>

</dd> <dt>

<span data-ttu-id="b8858-112">*UvhdRoamingPolicyXml* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b8858-112">*UvhdRoamingPolicyXml* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8858-113">Criteri di roaming per il VHD del profilo utente.</span><span class="sxs-lookup"><span data-stu-id="b8858-113">The roaming policy for the user profile VHD.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8858-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b8858-114">Requirements</span></span>



| <span data-ttu-id="b8858-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8858-115">Requirement</span></span> | <span data-ttu-id="b8858-116">Valore</span><span class="sxs-lookup"><span data-stu-id="b8858-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b8858-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8858-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b8858-118">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="b8858-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b8858-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="b8858-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b8858-120">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b8858-120">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="b8858-121">Spazio dei nomi</span><span class="sxs-lookup"><span data-stu-id="b8858-121">Namespace</span></span><br/>                | <span data-ttu-id="b8858-122">Radice \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b8858-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="b8858-123">MOF</span><span class="sxs-lookup"><span data-stu-id="b8858-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b8858-124"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b8858-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="b8858-125">DLL</span><span class="sxs-lookup"><span data-stu-id="b8858-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b8858-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8858-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8858-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b8858-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8858-128">**\_TSSessionDirectory Win32**</span><span class="sxs-lookup"><span data-stu-id="b8858-128">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

 





