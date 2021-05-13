---
description: Ottiene il nome del contenitore di account dell'utente.
title: DIDiskQuotaUser.AccountContainerName - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.AccountContainerName
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 5b9b0355-ea69-4c34-b0be-fc8e5855ec73
ms.openlocfilehash: 1cb709ccc4fa0afcb56314bd097b1b0120b8b59a
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843352"
---
# <a name="didiskquotauseraccountcontainername-property"></a><span data-ttu-id="a56a0-103">DIDiskQuotaUser.AccountContainerName - proprietà</span><span class="sxs-lookup"><span data-stu-id="a56a0-103">DIDiskQuotaUser.AccountContainerName property</span></span>

<span data-ttu-id="a56a0-104">Ottiene il nome del contenitore di account dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a56a0-104">Gets the name of the user's account container.</span></span>

<span data-ttu-id="a56a0-105">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="a56a0-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a56a0-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a56a0-106">Syntax</span></span>


```JScript
AccountContainerName = DIDiskQuotaUser.AccountContainerName
```



## <a name="property-value"></a><span data-ttu-id="a56a0-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="a56a0-107">Property value</span></span>

<span data-ttu-id="a56a0-108">Valore stringa impostato sul nome del contenitore dell'account dell'utente.</span><span class="sxs-lookup"><span data-stu-id="a56a0-108">A string value that is set to the user's account container name.</span></span>

## <a name="remarks"></a><span data-ttu-id="a56a0-109">Commenti</span><span class="sxs-lookup"><span data-stu-id="a56a0-109">Remarks</span></span>

<span data-ttu-id="a56a0-110">Per gli account senza informazioni sui servizi directory, questa proprietà contiene il nome di dominio.</span><span class="sxs-lookup"><span data-stu-id="a56a0-110">For accounts without directory services information, this property contains the domain name.</span></span> <span data-ttu-id="a56a0-111">Per gli account con informazioni sui servizi directory, questa proprietà contiene un nome canonico con il nome dell'oggetto di terminazione rimosso.</span><span class="sxs-lookup"><span data-stu-id="a56a0-111">For accounts with directory services information, this property contains a canonical name with the terminating object name removed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a56a0-112">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a56a0-112">Requirements</span></span>



| <span data-ttu-id="a56a0-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a56a0-113">Requirement</span></span> | <span data-ttu-id="a56a0-114">Valore</span><span class="sxs-lookup"><span data-stu-id="a56a0-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a56a0-115">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a56a0-115">Minimum supported client</span></span><br/> | <span data-ttu-id="a56a0-116">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a56a0-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a56a0-117">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a56a0-117">Minimum supported server</span></span><br/> | <span data-ttu-id="a56a0-118">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a56a0-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a56a0-119">DLL</span><span class="sxs-lookup"><span data-stu-id="a56a0-119">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a56a0-120"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a56a0-120"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a56a0-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a56a0-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a56a0-122">**Oggetto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="a56a0-122">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




