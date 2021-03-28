---
description: Ottiene un valore booleano che indica se il file di quota per il volume è attualmente in fase di ricompilazione.
ms.assetid: 66a6bafe-bda4-41b3-9207-2ea6b8e63835
title: Proprietà DiskQuotaControl. QuotaFileRebuilding
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaFileRebuilding
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: e06b73e53670a136e53721b4e6bc6b2f635d601b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977503"
---
# <a name="diskquotacontrolquotafilerebuilding-property"></a><span data-ttu-id="aff7e-103">Proprietà DiskQuotaControl. QuotaFileRebuilding</span><span class="sxs-lookup"><span data-stu-id="aff7e-103">DiskQuotaControl.QuotaFileRebuilding property</span></span>

<span data-ttu-id="aff7e-104">Ottiene un valore booleano che indica se il file di quota per il volume è attualmente in fase di ricompilazione.</span><span class="sxs-lookup"><span data-stu-id="aff7e-104">Gets a Boolean value that indicates whether the quota file for the volume is currently being rebuilt.</span></span>

<span data-ttu-id="aff7e-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="aff7e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="aff7e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="aff7e-106">Syntax</span></span>


```JScript
bQuotaFileRebuilding = DiskQuotaControl.QuotaFileRebuilding
```



## <a name="property-value"></a><span data-ttu-id="aff7e-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="aff7e-107">Property value</span></span>

<span data-ttu-id="aff7e-108">Questa proprietà è impostata su **true** se il file della quota viene ricompilato o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="aff7e-108">This property is set to **TRUE** if the quota file is being rebuilt, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="aff7e-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="aff7e-109">Remarks</span></span>

<span data-ttu-id="aff7e-110">Il file di quote viene ricompilato automaticamente quando le quote sono abilitate nel sistema o quando una o più voci utente sono contrassegnate per l'eliminazione.</span><span class="sxs-lookup"><span data-stu-id="aff7e-110">The quota file is automatically rebuilt when quotas are enabled on the system or when one or more user entries are marked for deletion.</span></span>

## <a name="requirements"></a><span data-ttu-id="aff7e-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="aff7e-111">Requirements</span></span>



| <span data-ttu-id="aff7e-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="aff7e-112">Requirement</span></span> | <span data-ttu-id="aff7e-113">Valore</span><span class="sxs-lookup"><span data-stu-id="aff7e-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aff7e-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aff7e-114">Minimum supported client</span></span><br/> | <span data-ttu-id="aff7e-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aff7e-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aff7e-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="aff7e-116">Minimum supported server</span></span><br/> | <span data-ttu-id="aff7e-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="aff7e-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="aff7e-118">DLL</span><span class="sxs-lookup"><span data-stu-id="aff7e-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aff7e-119"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="aff7e-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aff7e-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="aff7e-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aff7e-121">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="aff7e-121">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




