---
description: Ottiene lo stato dell'account dell'utente.
title: DIDiskQuotaUser.AccountStatus - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountStatus
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: ff2234f7-4758-43c7-a3c2-8fb980b27c04
ms.openlocfilehash: e27e86fadab02616f91a4838acfc4be93e985ebd
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841652"
---
# <a name="didiskquotauseraccountstatus-property"></a><span data-ttu-id="bb126-103">DIDiskQuotaUser.AccountStatus - proprietà</span><span class="sxs-lookup"><span data-stu-id="bb126-103">DIDiskQuotaUser.AccountStatus property</span></span>

<span data-ttu-id="bb126-104">Ottiene lo stato dell'account dell'utente.</span><span class="sxs-lookup"><span data-stu-id="bb126-104">Gets the status of the user's account.</span></span>

<span data-ttu-id="bb126-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="bb126-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb126-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="bb126-106">Syntax</span></span>


```JScript
iAccountStatus = DIDiskQuotaUser.AccountStatus
```



## <a name="property-value"></a><span data-ttu-id="bb126-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="bb126-107">Property value</span></span>

<span data-ttu-id="bb126-108">Questa proprietà può assumere uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="bb126-108">This property can take one of the following values.</span></span>



| <span data-ttu-id="bb126-109">Stato</span><span class="sxs-lookup"><span data-stu-id="bb126-109">Status</span></span>            | <span data-ttu-id="bb126-110">Valore</span><span class="sxs-lookup"><span data-stu-id="bb126-110">Value</span></span> | <span data-ttu-id="bb126-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="bb126-111">Description</span></span>                         |
|-------------------|-------|-------------------------------------|
| <span data-ttu-id="bb126-112">dqAcctResolved</span><span class="sxs-lookup"><span data-stu-id="bb126-112">dqAcctResolved</span></span>    | <span data-ttu-id="bb126-113">0</span><span class="sxs-lookup"><span data-stu-id="bb126-113">0</span></span>     | <span data-ttu-id="bb126-114">Le informazioni sull'account vengono risolte.</span><span class="sxs-lookup"><span data-stu-id="bb126-114">Account information is resolved.</span></span>    |
| <span data-ttu-id="bb126-115">dqAcctUnavailable</span><span class="sxs-lookup"><span data-stu-id="bb126-115">dqAcctUnavailable</span></span> | <span data-ttu-id="bb126-116">1</span><span class="sxs-lookup"><span data-stu-id="bb126-116">1</span></span>     | <span data-ttu-id="bb126-117">Le informazioni sull'account non sono disponibili.</span><span class="sxs-lookup"><span data-stu-id="bb126-117">Account information is unavailable.</span></span> |
| <span data-ttu-id="bb126-118">dqAcctDeleted</span><span class="sxs-lookup"><span data-stu-id="bb126-118">dqAcctDeleted</span></span>     | <span data-ttu-id="bb126-119">2</span><span class="sxs-lookup"><span data-stu-id="bb126-119">2</span></span>     | <span data-ttu-id="bb126-120">L'account è stato eliminato.</span><span class="sxs-lookup"><span data-stu-id="bb126-120">Account has been deleted.</span></span>           |
| <span data-ttu-id="bb126-121">dqAcctInvalid</span><span class="sxs-lookup"><span data-stu-id="bb126-121">dqAcctInvalid</span></span>     | <span data-ttu-id="bb126-122">3</span><span class="sxs-lookup"><span data-stu-id="bb126-122">3</span></span>     | <span data-ttu-id="bb126-123">L'account non è valido.</span><span class="sxs-lookup"><span data-stu-id="bb126-123">Account is invalid.</span></span>                 |
| <span data-ttu-id="bb126-124">dqAcctUnknown</span><span class="sxs-lookup"><span data-stu-id="bb126-124">dqAcctUnknown</span></span>     | <span data-ttu-id="bb126-125">4</span><span class="sxs-lookup"><span data-stu-id="bb126-125">4</span></span>     | <span data-ttu-id="bb126-126">Impossibile trovare l'account.</span><span class="sxs-lookup"><span data-stu-id="bb126-126">Account cannot be found.</span></span>            |
| <span data-ttu-id="bb126-127">dqAcctUnresolved</span><span class="sxs-lookup"><span data-stu-id="bb126-127">dqAcctUnresolved</span></span>  | <span data-ttu-id="bb126-128">5</span><span class="sxs-lookup"><span data-stu-id="bb126-128">5</span></span>     | <span data-ttu-id="bb126-129">Le informazioni sull'account non sono risolte.</span><span class="sxs-lookup"><span data-stu-id="bb126-129">Account information is unresolved.</span></span>  |



 

## <a name="requirements"></a><span data-ttu-id="bb126-130">Requisiti</span><span class="sxs-lookup"><span data-stu-id="bb126-130">Requirements</span></span>



| <span data-ttu-id="bb126-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="bb126-131">Requirement</span></span> | <span data-ttu-id="bb126-132">Valore</span><span class="sxs-lookup"><span data-stu-id="bb126-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb126-133">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb126-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bb126-134">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb126-134">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb126-135">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="bb126-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bb126-136">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="bb126-136">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="bb126-137">DLL</span><span class="sxs-lookup"><span data-stu-id="bb126-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bb126-138"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="bb126-138"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb126-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="bb126-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb126-140">**Oggetto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="bb126-140">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




