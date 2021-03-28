---
description: Imposta o ottiene il limite di quota corrente dell'utente.
title: Proprietà DIDiskQuotaUser. QuotaLimit
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
ms.openlocfilehash: 6c13c0d38c3c5f4387b7ee90165057edb111124a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977223"
---
# <a name="didiskquotauserquotalimit-property"></a><span data-ttu-id="3fa59-103">Proprietà DIDiskQuotaUser. QuotaLimit</span><span class="sxs-lookup"><span data-stu-id="3fa59-103">DIDiskQuotaUser.QuotaLimit property</span></span>

<span data-ttu-id="3fa59-104">Imposta o ottiene il [**limite di quota**](diskquotacontrol-object.md)corrente dell'utente.</span><span class="sxs-lookup"><span data-stu-id="3fa59-104">Sets or gets the user's current [**quota limit**](diskquotacontrol-object.md).</span></span>

<span data-ttu-id="3fa59-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3fa59-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fa59-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3fa59-106">Syntax</span></span>


```JScript
iQuotaLimit = DIDiskQuotaUser.QuotaLimit
DIDiskQuotaUser.QuotaLimit = iQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="3fa59-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3fa59-107">Property value</span></span>

<span data-ttu-id="3fa59-108">Valore **intero** che specifica o riceve il limite di quota corrente dell'utente, in byte.</span><span class="sxs-lookup"><span data-stu-id="3fa59-108">An **Integer** value that specifies or receives the user's current quota limit, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="3fa59-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3fa59-109">Requirements</span></span>



| <span data-ttu-id="3fa59-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fa59-110">Requirement</span></span> | <span data-ttu-id="3fa59-111">Valore</span><span class="sxs-lookup"><span data-stu-id="3fa59-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fa59-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fa59-112">Minimum supported client</span></span><br/> | <span data-ttu-id="3fa59-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3fa59-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3fa59-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3fa59-114">Minimum supported server</span></span><br/> | <span data-ttu-id="3fa59-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3fa59-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3fa59-116">DLL</span><span class="sxs-lookup"><span data-stu-id="3fa59-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3fa59-117"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="3fa59-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fa59-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3fa59-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa59-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="3fa59-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="3fa59-120">**DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="3fa59-120">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="3fa59-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="3fa59-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> </dl>

 

 




