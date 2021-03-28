---
description: Ottiene la soglia di quota predefinita come stringa di testo.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: Proprietà DiskQuotaControl. DefaultQuotaThresholdText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128439"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a><span data-ttu-id="6e9b6-103">Proprietà DiskQuotaControl. DefaultQuotaThresholdText</span><span class="sxs-lookup"><span data-stu-id="6e9b6-103">DiskQuotaControl.DefaultQuotaThresholdText property</span></span>

<span data-ttu-id="6e9b6-104">Ottiene la soglia di quota predefinita come stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="6e9b6-104">Gets the default quota threshold as a text string.</span></span>

<span data-ttu-id="6e9b6-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="6e9b6-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e9b6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6e9b6-106">Syntax</span></span>


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="6e9b6-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="6e9b6-107">Property value</span></span>

<span data-ttu-id="6e9b6-108">Valore stringa che contiene la soglia di quota predefinita per il volume.</span><span class="sxs-lookup"><span data-stu-id="6e9b6-108">A string value that contains the default quota threshold for the volume.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e9b6-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="6e9b6-109">Remarks</span></span>

<span data-ttu-id="6e9b6-110">La soglia di quota predefinita viene applicata automaticamente ai nuovi utenti del volume.</span><span class="sxs-lookup"><span data-stu-id="6e9b6-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="6e9b6-111">Se l'utilizzo del disco di un utente supera questo valore e la proprietà [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) è impostata su **true**, il sistema genera una voce del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="6e9b6-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="6e9b6-112">Se, ad esempio, la soglia predefinita è 10,0 MB, il valore della proprietà è "10,0 MB".</span><span class="sxs-lookup"><span data-stu-id="6e9b6-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="6e9b6-113">Se il volume non dispone di una soglia predefinita, la proprietà viene impostata su "nessun limite" o sull'equivalente localizzato.</span><span class="sxs-lookup"><span data-stu-id="6e9b6-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e9b6-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6e9b6-114">Requirements</span></span>



| <span data-ttu-id="6e9b6-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6e9b6-115">Requirement</span></span> | <span data-ttu-id="6e9b6-116">Valore</span><span class="sxs-lookup"><span data-stu-id="6e9b6-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e9b6-117">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e9b6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6e9b6-118">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6e9b6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6e9b6-119">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6e9b6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6e9b6-120">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6e9b6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6e9b6-121">DLL</span><span class="sxs-lookup"><span data-stu-id="6e9b6-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e9b6-122"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6e9b6-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e9b6-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6e9b6-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e9b6-124">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="6e9b6-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




