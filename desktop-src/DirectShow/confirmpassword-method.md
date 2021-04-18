---
description: Il metodo DVDAdm. ConfirmPassword verifica se la password specificata corrisponde alla password salvata in precedenza.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: Metodo ConfirmPassword (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328827"
---
# <a name="confirmpassword-method"></a><span data-ttu-id="f6503-103">Metodo ConfirmPassword</span><span class="sxs-lookup"><span data-stu-id="f6503-103">ConfirmPassword Method</span></span>

> [!Note]  
> <span data-ttu-id="f6503-104">Questo componente è disponibile per l'uso nei sistemi operativi Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="f6503-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f6503-105">È possibile che in versioni successive sia stata modificata o non sia più disponibile.</span><span class="sxs-lookup"><span data-stu-id="f6503-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f6503-106">Il `DVDAdm.ConfirmPassword` metodo verifica se la password specificata corrisponde alla password salvata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="f6503-106">The `DVDAdm.ConfirmPassword` method tests whether the specified password matches the previously saved password.</span></span>

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="f6503-107">Parametri</span><span class="sxs-lookup"><span data-stu-id="f6503-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6503-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="f6503-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="f6503-109">Specifica il nome dell'utente sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="f6503-109">Specifies the user's name as a String.</span></span>

</dd> <dt>

<span data-ttu-id="f6503-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="f6503-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="f6503-111">Specifica la nuova password sotto forma di stringa.</span><span class="sxs-lookup"><span data-stu-id="f6503-111">Specifies the new password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6503-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f6503-112">Return Value</span></span>

<span data-ttu-id="f6503-113">Restituisce true se la password specificata corrisponde alla password esistente; in caso contrario, false.</span><span class="sxs-lookup"><span data-stu-id="f6503-113">Returns true if the specified password matches the existing password, false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="f6503-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f6503-114">Remarks</span></span>

<span data-ttu-id="f6503-115">Attualmente, il parametro *sUserName* viene ignorato in questo e in tutti i metodi correlati.</span><span class="sxs-lookup"><span data-stu-id="f6503-115">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6503-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f6503-116">Requirements</span></span>



| <span data-ttu-id="f6503-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6503-117">Requirement</span></span> | <span data-ttu-id="f6503-118">Valore</span><span class="sxs-lookup"><span data-stu-id="f6503-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f6503-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f6503-119">Header</span></span><br/> | <dl> <span data-ttu-id="f6503-120"><dt>Segmento. h</dt></span><span class="sxs-lookup"><span data-stu-id="f6503-120"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6503-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f6503-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6503-122">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="f6503-122">**ChangePassword**</span></span>](changepassword-method.md)
</dt> <dt>

[<span data-ttu-id="f6503-123">Oggetto MSDVDAdm</span><span class="sxs-lookup"><span data-stu-id="f6503-123">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




