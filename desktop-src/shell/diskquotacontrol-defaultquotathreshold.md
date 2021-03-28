---
description: Ottiene o imposta la soglia di quota predefinita.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: Proprietà DiskQuotaControl. DefaultQuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a4ce4205ee8bcc73c78bd1aabe7d8659ac3f5489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977194"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a><span data-ttu-id="e3dfc-103">Proprietà DiskQuotaControl. DefaultQuotaThreshold</span><span class="sxs-lookup"><span data-stu-id="e3dfc-103">DiskQuotaControl.DefaultQuotaThreshold property</span></span>

<span data-ttu-id="e3dfc-104">Ottiene o imposta la soglia di quota predefinita.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-104">Sets or gets the default quota threshold.</span></span>

<span data-ttu-id="e3dfc-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3dfc-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e3dfc-106">Syntax</span></span>


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="e3dfc-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="e3dfc-107">Property value</span></span>

<span data-ttu-id="e3dfc-108">Valore **intero** impostato sulla soglia di avviso predefinita per i nuovi utenti, in byte.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-108">An **Integer** value that is set to the default warning threshold for new users, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="e3dfc-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="e3dfc-109">Remarks</span></span>

<span data-ttu-id="e3dfc-110">La soglia di quota predefinita viene applicata automaticamente ai nuovi utenti del volume.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="e3dfc-111">Se l'utilizzo del disco di un utente supera questo valore e la proprietà [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) è impostata su **true**, il sistema genera una voce del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="e3dfc-112">Se, ad esempio, la soglia predefinita è 10,0 MB, il valore della proprietà è "10,0 MB".</span><span class="sxs-lookup"><span data-stu-id="e3dfc-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="e3dfc-113">Se il volume non dispone di una soglia predefinita, la proprietà viene impostata su "nessun limite" o sull'equivalente localizzato.</span><span class="sxs-lookup"><span data-stu-id="e3dfc-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="e3dfc-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e3dfc-114">Requirements</span></span>



| <span data-ttu-id="e3dfc-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3dfc-115">Requirement</span></span> | <span data-ttu-id="e3dfc-116">Valore</span><span class="sxs-lookup"><span data-stu-id="e3dfc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3dfc-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3dfc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e3dfc-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e3dfc-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e3dfc-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="e3dfc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e3dfc-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="e3dfc-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e3dfc-121">DLL</span><span class="sxs-lookup"><span data-stu-id="e3dfc-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e3dfc-122"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="e3dfc-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e3dfc-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e3dfc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e3dfc-124">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="e3dfc-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




