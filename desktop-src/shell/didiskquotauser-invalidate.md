---
description: Cancella le informazioni utente memorizzate nella cache dell'oggetto.
title: DIDiskQuotaUser. Invalidate (metodo)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 2b07ae6fd210b8722378a771cda97c2c04572c66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525344"
---
# <a name="didiskquotauserinvalidate-method"></a><span data-ttu-id="a1edc-103">DIDiskQuotaUser. Invalidate (metodo)</span><span class="sxs-lookup"><span data-stu-id="a1edc-103">DIDiskQuotaUser.Invalidate method</span></span>

<span data-ttu-id="a1edc-104">Cancella le informazioni utente memorizzate nella cache dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1edc-104">Clears the object's cached user information.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1edc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1edc-105">Syntax</span></span>


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a><span data-ttu-id="a1edc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1edc-106">Parameters</span></span>

<span data-ttu-id="a1edc-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a1edc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a1edc-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1edc-108">Return value</span></span>

<span data-ttu-id="a1edc-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="a1edc-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1edc-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1edc-110">Remarks</span></span>

<span data-ttu-id="a1edc-111">Questo metodo consente di cancellare le informazioni utente archiviate nella cache dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="a1edc-111">This method clears the user information stored in the object's cache.</span></span> <span data-ttu-id="a1edc-112">La volta successiva che viene effettuata una richiesta per le informazioni relative alla quota, l'oggetto recupera le informazioni dal volume NTFS e aggiorna la cache.</span><span class="sxs-lookup"><span data-stu-id="a1edc-112">The next time a request is made for quota-related information, the object retrieves the information from the NTFS volume and refreshes the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1edc-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1edc-113">Requirements</span></span>



| <span data-ttu-id="a1edc-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1edc-114">Requirement</span></span> | <span data-ttu-id="a1edc-115">Valore</span><span class="sxs-lookup"><span data-stu-id="a1edc-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1edc-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1edc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a1edc-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a1edc-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a1edc-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a1edc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a1edc-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="a1edc-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="a1edc-120">DLL</span><span class="sxs-lookup"><span data-stu-id="a1edc-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1edc-121"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="a1edc-121"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1edc-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1edc-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1edc-123">**Oggetto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="a1edc-123">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




