---
description: Imposta o ottiene la soglia di avviso dell'utente, in byte.
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: Proprietà DIDiskQuotaUser. QuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7ce336c84d086c4e4be369278a77e40e59474bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878758"
---
# <a name="didiskquotauserquotathreshold-property"></a><span data-ttu-id="f76be-103">Proprietà DIDiskQuotaUser. QuotaThreshold</span><span class="sxs-lookup"><span data-stu-id="f76be-103">DIDiskQuotaUser.QuotaThreshold property</span></span>

<span data-ttu-id="f76be-104">Imposta o ottiene la soglia di avviso dell'utente, in byte.</span><span class="sxs-lookup"><span data-stu-id="f76be-104">Sets or gets the user's warning threshold, in bytes.</span></span>

<span data-ttu-id="f76be-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="f76be-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="f76be-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f76be-106">Syntax</span></span>


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="f76be-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="f76be-107">Property value</span></span>

<span data-ttu-id="f76be-108">Valore **intero** che specifica o riceve la soglia di avviso dell'utente.</span><span class="sxs-lookup"><span data-stu-id="f76be-108">An **Integer** value that specifies or receives the user's warning threshold.</span></span> <span data-ttu-id="f76be-109">Se l'utilizzo del disco di un utente supera questo valore e la proprietà [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) è impostata su **true**, il sistema genera una voce del registro eventi.</span><span class="sxs-lookup"><span data-stu-id="f76be-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="f76be-110">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f76be-110">Requirements</span></span>



| <span data-ttu-id="f76be-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="f76be-111">Requirement</span></span> | <span data-ttu-id="f76be-112">Valore</span><span class="sxs-lookup"><span data-stu-id="f76be-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f76be-113">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f76be-113">Minimum supported client</span></span><br/> | <span data-ttu-id="f76be-114">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f76be-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f76be-115">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f76be-115">Minimum supported server</span></span><br/> | <span data-ttu-id="f76be-116">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="f76be-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="f76be-117">DLL</span><span class="sxs-lookup"><span data-stu-id="f76be-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f76be-118"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="f76be-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f76be-119">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f76be-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f76be-120">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="f76be-120">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="f76be-121">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="f76be-121">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="f76be-122">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="f76be-122">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="f76be-123">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="f76be-123">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




