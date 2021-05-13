---
description: Imposta o ottiene il limite di quota corrente dell'utente.
title: DIDiskQuotaUser.QuotaLimit - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7eee1be7-8ad5-4796-910c-987fe3fd6338
ms.openlocfilehash: b1971871bdeb18e3c7dd4c7978152bbec276fa8b
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841632"
---
# <a name="didiskquotauserquotalimit-property"></a><span data-ttu-id="045b6-103">DIDiskQuotaUser.QuotaLimit - proprietà</span><span class="sxs-lookup"><span data-stu-id="045b6-103">DIDiskQuotaUser.QuotaLimit property</span></span>

<span data-ttu-id="045b6-104">Imposta o ottiene il limite di quota corrente [**dell'utente.**](diskquotacontrol-object.md)</span><span class="sxs-lookup"><span data-stu-id="045b6-104">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span>

<span data-ttu-id="045b6-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="045b6-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="045b6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="045b6-106">Syntax</span></span>


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="045b6-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="045b6-107">Property value</span></span>

<span data-ttu-id="045b6-108">Valore **intero** che specifica o riceve il limite di quota corrente dell'utente, in byte.</span><span class="sxs-lookup"><span data-stu-id="045b6-108">An **Integer** value that specifies or receives the user's current quota limit, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="045b6-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="045b6-109">Requirements</span></span>



| <span data-ttu-id="045b6-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="045b6-110">Requirement</span></span> | <span data-ttu-id="045b6-111">Valore</span><span class="sxs-lookup"><span data-stu-id="045b6-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="045b6-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="045b6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="045b6-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="045b6-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="045b6-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="045b6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="045b6-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="045b6-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="045b6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="045b6-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="045b6-117"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="045b6-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="045b6-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="045b6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="045b6-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="045b6-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="045b6-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="045b6-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="045b6-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="045b6-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




