---
description: Ottiene il limite di quota predefinito come stringa di testo.
title: DiskQuotaControl.DefaultQuotaLimitText - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimitText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ea1b02e0-c480-4ef1-b6e0-1ec202d5f3c5
ms.openlocfilehash: 14a5b5a0cc42bda17f922020a8485430797875e1
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841542"
---
# <a name="diskquotacontroldefaultquotalimittext-property"></a><span data-ttu-id="4ae01-103">DiskQuotaControl.DefaultQuotaLimitText - proprietà</span><span class="sxs-lookup"><span data-stu-id="4ae01-103">DiskQuotaControl.DefaultQuotaLimitText property</span></span>

<span data-ttu-id="4ae01-104">Ottiene il limite di quota predefinito come stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="4ae01-104">Gets the default quota limit as a text string.</span></span>

<span data-ttu-id="4ae01-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="4ae01-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="4ae01-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4ae01-106">Syntax</span></span>


```JScript
DefaultQuotaLimitText = DiskQuotaControl.DefaultQuotaLimitText
```



## <a name="property-value"></a><span data-ttu-id="4ae01-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="4ae01-107">Property value</span></span>

<span data-ttu-id="4ae01-108">Valore stringa che contiene il limite di quota predefinito per i nuovi utenti del volume.</span><span class="sxs-lookup"><span data-stu-id="4ae01-108">A string value that contains the default quota limit for new users of the volume.</span></span> <span data-ttu-id="4ae01-109">Ad esempio, se la quota predefinita è 10,5 MB, il valore della proprietà è "10,5 MB".</span><span class="sxs-lookup"><span data-stu-id="4ae01-109">For example, if the default quota is 10.5 MB, the value of the property is "10.5 MB".</span></span> <span data-ttu-id="4ae01-110">Se il volume non ha una quota predefinita, la proprietà viene impostata su "Nessun limite" o sull'equivalente localizzato.</span><span class="sxs-lookup"><span data-stu-id="4ae01-110">If the volume has no default quota, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="4ae01-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4ae01-111">Requirements</span></span>



| <span data-ttu-id="4ae01-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="4ae01-112">Requirement</span></span> | <span data-ttu-id="4ae01-113">Valore</span><span class="sxs-lookup"><span data-stu-id="4ae01-113">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4ae01-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ae01-114">Minimum supported client</span></span><br/> | <span data-ttu-id="4ae01-115">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ae01-115">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4ae01-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="4ae01-116">Minimum supported server</span></span><br/> | <span data-ttu-id="4ae01-117">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="4ae01-117">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="4ae01-118">DLL</span><span class="sxs-lookup"><span data-stu-id="4ae01-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4ae01-119"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="4ae01-119"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4ae01-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4ae01-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4ae01-121">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="4ae01-121">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="4ae01-122">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="4ae01-122">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




