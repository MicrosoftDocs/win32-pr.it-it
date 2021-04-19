---
description: Cancella il nome utente dal controllo smart card.
ms.assetid: fff50db5-0610-4985-94c6-96d7ce990219
title: 'Metodo ISCrdEnr:: resetUser'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.resetUser
- SCrdEnr.resetUser
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3b00721229890f82b00e7e7a41ccb8796a81b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317714"
---
# <a name="iscrdenrresetuser-method"></a><span data-ttu-id="7a1c4-103">Metodo ISCrdEnr:: resetUser</span><span class="sxs-lookup"><span data-stu-id="7a1c4-103">ISCrdEnr::resetUser method</span></span>

<span data-ttu-id="7a1c4-104">Il metodo **resetUser** Cancella il nome utente dal controllo smart card.</span><span class="sxs-lookup"><span data-stu-id="7a1c4-104">The **resetUser** method clears the user name from the smart card control.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a1c4-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7a1c4-105">Syntax</span></span>


```C++
HRESULT resetUser();
```



## <a name="parameters"></a><span data-ttu-id="7a1c4-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="7a1c4-106">Parameters</span></span>

<span data-ttu-id="7a1c4-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="7a1c4-107">This method has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a1c4-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="7a1c4-108">Remarks</span></span>

<span data-ttu-id="7a1c4-109">Questo metodo cancella qualsiasi nome utente esistente e certificato registrato in precedenza dalla memoria.</span><span class="sxs-lookup"><span data-stu-id="7a1c4-109">This method clears any existing user name and previously enrolled certificate from memory.</span></span> <span data-ttu-id="7a1c4-110">Tuttavia, il certificato registrato in precedenza non viene rimosso dalla smart card.</span><span class="sxs-lookup"><span data-stu-id="7a1c4-110">The previously enrolled certificate is not removed from the smart card, however.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a1c4-111">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7a1c4-111">Requirements</span></span>



| <span data-ttu-id="7a1c4-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a1c4-112">Requirement</span></span> | <span data-ttu-id="7a1c4-113">Valore</span><span class="sxs-lookup"><span data-stu-id="7a1c4-113">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a1c4-114">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a1c4-114">Minimum supported client</span></span><br/> | <span data-ttu-id="7a1c4-115">Nessuno supportato</span><span class="sxs-lookup"><span data-stu-id="7a1c4-115">None supported</span></span><br/>                                                               |
| <span data-ttu-id="7a1c4-116">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7a1c4-116">Minimum supported server</span></span><br/> | <span data-ttu-id="7a1c4-117">\[Solo app desktop Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="7a1c4-117">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7a1c4-118">DLL</span><span class="sxs-lookup"><span data-stu-id="7a1c4-118">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a1c4-119"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a1c4-119"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="7a1c4-120">IID</span><span class="sxs-lookup"><span data-stu-id="7a1c4-120">IID</span></span><br/>                      | <span data-ttu-id="7a1c4-121">IID \_ ISCrdEnr è definito come 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="7a1c4-121">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="7a1c4-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7a1c4-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a1c4-123">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="7a1c4-123">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="7a1c4-124">**ISCrdEnr:: GetUserName**</span><span class="sxs-lookup"><span data-stu-id="7a1c4-124">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="7a1c4-125">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="7a1c4-125">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="7a1c4-126">**ISCrdEnr:: seusername**</span><span class="sxs-lookup"><span data-stu-id="7a1c4-126">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




