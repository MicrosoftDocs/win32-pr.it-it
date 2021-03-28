---
description: Ottiene la soglia di avviso dell'utente come una stringa di testo.
ms.assetid: 55b53ad0-e7cd-4417-9087-297ac96e245f
title: Proprietà DIDiskQuotaUser. QuotaThresholdText
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 511829233b93dbe164ce2feccd1247ccebf3ec3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977218"
---
# <a name="didiskquotauserquotathresholdtext-property"></a><span data-ttu-id="2245e-103">Proprietà DIDiskQuotaUser. QuotaThresholdText</span><span class="sxs-lookup"><span data-stu-id="2245e-103">DIDiskQuotaUser.QuotaThresholdText property</span></span>

<span data-ttu-id="2245e-104">Ottiene la soglia di avviso dell'utente come una stringa di testo.</span><span class="sxs-lookup"><span data-stu-id="2245e-104">Gets the user's warning threshold as a text string.</span></span>

<span data-ttu-id="2245e-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="2245e-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2245e-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="2245e-106">Syntax</span></span>


```JScript
QuotaThresholdText = DIDiskQuotaUser.QuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="2245e-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="2245e-107">Property value</span></span>

<span data-ttu-id="2245e-108">Valore stringa che contiene la soglia di avviso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="2245e-108">The string value that contains the user's warning threshold.</span></span> <span data-ttu-id="2245e-109">Se l'utilizzo del disco di un utente supera questo valore e la proprietà [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) è impostata su **true**, il sistema genera una voce del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="2245e-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="2245e-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="2245e-110">Requirements</span></span>



| <span data-ttu-id="2245e-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="2245e-111">Requirement</span></span> | <span data-ttu-id="2245e-112">Valore</span><span class="sxs-lookup"><span data-stu-id="2245e-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2245e-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2245e-113">Minimum supported client</span></span><br/> | <span data-ttu-id="2245e-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2245e-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2245e-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="2245e-115">Minimum supported server</span></span><br/> | <span data-ttu-id="2245e-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="2245e-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="2245e-117">DLL</span><span class="sxs-lookup"><span data-stu-id="2245e-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2245e-118"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="2245e-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2245e-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="2245e-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2245e-120">**Oggetto IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="2245e-120">**IDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="2245e-121">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="2245e-121">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="2245e-122">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="2245e-122">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="2245e-123">**QuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="2245e-123">**QuotaThreshold**</span></span>](didiskquotauser-quotathreshold.md)
</dt> </dl>

 

 




