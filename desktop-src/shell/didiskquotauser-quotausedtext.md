---
description: Ottiene l'utilizzo del disco corrente dell'utente come stringa di testo.
title: Proprietà DIDiskQuotaUser. QuotaUsedText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: 1091d7f2d75b264b085c09af1873ac7c8ebd1617
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977207"
---
# <a name="didiskquotauserquotausedtext-property"></a><span data-ttu-id="07c3a-103">Proprietà DIDiskQuotaUser. QuotaUsedText</span><span class="sxs-lookup"><span data-stu-id="07c3a-103">DIDiskQuotaUser.QuotaUsedText property</span></span>

<span data-ttu-id="07c3a-104">Ottiene l'utilizzo del disco corrente dell'utente come stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="07c3a-104">Gets the user's current disk usage as a text string.</span></span>

<span data-ttu-id="07c3a-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="07c3a-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="07c3a-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="07c3a-106">Syntax</span></span>


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a><span data-ttu-id="07c3a-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="07c3a-107">Property value</span></span>

<span data-ttu-id="07c3a-108">Valore stringa impostato sulla quantità di spazio su disco attualmente in uso.</span><span class="sxs-lookup"><span data-stu-id="07c3a-108">A string value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="07c3a-109">Se la compressione dei file NTFS è abilitata, questa proprietà riflette la quantità di spazio su disco necessaria per i dati in uno stato non compresso.</span><span class="sxs-lookup"><span data-stu-id="07c3a-109">If NTFS file compression is enabled, this property reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="07c3a-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="07c3a-110">Requirements</span></span>



| <span data-ttu-id="07c3a-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="07c3a-111">Requirement</span></span> | <span data-ttu-id="07c3a-112">Valore</span><span class="sxs-lookup"><span data-stu-id="07c3a-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07c3a-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07c3a-113">Minimum supported client</span></span><br/> | <span data-ttu-id="07c3a-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07c3a-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07c3a-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="07c3a-115">Minimum supported server</span></span><br/> | <span data-ttu-id="07c3a-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="07c3a-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="07c3a-117">DLL</span><span class="sxs-lookup"><span data-stu-id="07c3a-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07c3a-118"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="07c3a-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07c3a-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="07c3a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07c3a-120">**Oggetto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="07c3a-120">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="07c3a-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="07c3a-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="07c3a-122">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="07c3a-122">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[<span data-ttu-id="07c3a-123">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="07c3a-123">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




