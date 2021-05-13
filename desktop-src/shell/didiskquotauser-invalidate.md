---
description: Cancella le informazioni utente memorizzate nella cache dell'oggetto.
title: Metodo DIDiskQuotaUser.Invalidate
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
ms.openlocfilehash: 9f8ad77c9697ed5d284cf782f431ec59b38ca415
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843272"
---
# <a name="didiskquotauserinvalidate-method"></a><span data-ttu-id="6b8ba-103">Metodo DIDiskQuotaUser.Invalidate</span><span class="sxs-lookup"><span data-stu-id="6b8ba-103">DIDiskQuotaUser.Invalidate method</span></span>

<span data-ttu-id="6b8ba-104">Cancella le informazioni utente memorizzate nella cache dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6b8ba-104">Clears the object's cached user information.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b8ba-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b8ba-105">Syntax</span></span>


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a><span data-ttu-id="6b8ba-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b8ba-106">Parameters</span></span>

<span data-ttu-id="6b8ba-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="6b8ba-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6b8ba-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b8ba-108">Return value</span></span>

<span data-ttu-id="6b8ba-109">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="6b8ba-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b8ba-110">Commenti</span><span class="sxs-lookup"><span data-stu-id="6b8ba-110">Remarks</span></span>

<span data-ttu-id="6b8ba-111">Questo metodo cancella le informazioni utente archiviate nella cache dell'oggetto.</span><span class="sxs-lookup"><span data-stu-id="6b8ba-111">This method clears the user information stored in the object's cache.</span></span> <span data-ttu-id="6b8ba-112">Alla successiva richiesta di informazioni relative alla quota, l'oggetto recupera le informazioni dal volume NTFS e aggiorna la cache.</span><span class="sxs-lookup"><span data-stu-id="6b8ba-112">The next time a request is made for quota-related information, the object retrieves the information from the NTFS volume and refreshes the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8ba-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b8ba-113">Requirements</span></span>



| <span data-ttu-id="6b8ba-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b8ba-114">Requirement</span></span> | <span data-ttu-id="6b8ba-115">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8ba-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8ba-116">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8ba-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6b8ba-117">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b8ba-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6b8ba-118">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6b8ba-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6b8ba-119">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="6b8ba-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6b8ba-120">DLL</span><span class="sxs-lookup"><span data-stu-id="6b8ba-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b8ba-121"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="6b8ba-121"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b8ba-122">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b8ba-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8ba-123">**Oggetto DIDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="6b8ba-123">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




