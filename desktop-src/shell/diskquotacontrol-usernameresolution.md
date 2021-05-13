---
description: Imposta o ottiene un valore che controlla la modalità di risoluzione degli ID di sicurezza utente (SID) in nomi utente.
title: DiskQuotaControl.UserNameResolution - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.UserNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: dc936421-e66d-4762-912a-c586f9cdace4
ms.openlocfilehash: 169f4db6e135392e9548767520f6d2b0bd2d527c
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841462"
---
# <a name="diskquotacontrolusernameresolution-property"></a><span data-ttu-id="7ee75-103">DiskQuotaControl.UserNameResolution - proprietà</span><span class="sxs-lookup"><span data-stu-id="7ee75-103">DiskQuotaControl.UserNameResolution property</span></span>

<span data-ttu-id="7ee75-104">Imposta o ottiene un valore che controlla la modalità di risoluzione degli ID di sicurezza utente (SID) in nomi utente.</span><span class="sxs-lookup"><span data-stu-id="7ee75-104">Sets or gets a value that controls how user security identifier (SID) are resolved to user names.</span></span>

<span data-ttu-id="7ee75-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="7ee75-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ee75-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7ee75-106">Syntax</span></span>


```JScript
iUserNameResolution = DiskQuotaControl.UserNameResolution
DiskQuotaControl.UserNameResolution = iUserNameResolution
```



## <a name="property-value"></a><span data-ttu-id="7ee75-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="7ee75-107">Property value</span></span>

<span data-ttu-id="7ee75-108">Questa proprietà può essere impostata su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="7ee75-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="7ee75-109">Tipo di risoluzione</span><span class="sxs-lookup"><span data-stu-id="7ee75-109">Resolution Type</span></span> | <span data-ttu-id="7ee75-110">Valore</span><span class="sxs-lookup"><span data-stu-id="7ee75-110">Value</span></span> | <span data-ttu-id="7ee75-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="7ee75-111">Description</span></span>                                                                                                                                              |
|-----------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ee75-112">dqResolveNone</span><span class="sxs-lookup"><span data-stu-id="7ee75-112">dqResolveNone</span></span>   | <span data-ttu-id="7ee75-113">0</span><span class="sxs-lookup"><span data-stu-id="7ee75-113">0</span></span>     | <span data-ttu-id="7ee75-114">Non risolvere le informazioni sul nome utente.</span><span class="sxs-lookup"><span data-stu-id="7ee75-114">Do not resolve user name information.</span></span>                                                                                                                    |
| <span data-ttu-id="7ee75-115">dqResolveSync</span><span class="sxs-lookup"><span data-stu-id="7ee75-115">dqResolveSync</span></span>   | <span data-ttu-id="7ee75-116">1</span><span class="sxs-lookup"><span data-stu-id="7ee75-116">1</span></span>     | <span data-ttu-id="7ee75-117">Attendere durante la risoluzione delle informazioni sul nome.</span><span class="sxs-lookup"><span data-stu-id="7ee75-117">Wait while resolving name information.</span></span>                                                                                                                   |
| <span data-ttu-id="7ee75-118">dqResolveAsync</span><span class="sxs-lookup"><span data-stu-id="7ee75-118">dqResolveAsync</span></span>  | <span data-ttu-id="7ee75-119">2</span><span class="sxs-lookup"><span data-stu-id="7ee75-119">2</span></span>     | <span data-ttu-id="7ee75-120">Non attendere durante la risoluzione delle informazioni sul nome.</span><span class="sxs-lookup"><span data-stu-id="7ee75-120">Do not wait while resolving name information.</span></span> <span data-ttu-id="7ee75-121">[**L'evento OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) viene generato quando il nome viene risolto.</span><span class="sxs-lookup"><span data-stu-id="7ee75-121">The [**OnUserNameChanged**](diskquotacontrol-onusernamechanged.md) event fires when the name is resolved.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7ee75-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="7ee75-122">Remarks</span></span>

<span data-ttu-id="7ee75-123">Questa proprietà influisce [**sull'enumerazione degli oggetti DIDiskQuotaUser**](didiskquotauser-object.md) e sui metodi [**AddUser**](diskquotacontrol-adduser.md) [**e FindUser.**](diskquotacontrol-finduser.md)</span><span class="sxs-lookup"><span data-stu-id="7ee75-123">This property affects the enumeration of [**DIDiskQuotaUser**](didiskquotauser-object.md) objects, and the [**AddUser**](diskquotacontrol-adduser.md) and [**FindUser**](diskquotacontrol-finduser.md) methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ee75-124">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7ee75-124">Requirements</span></span>



| <span data-ttu-id="7ee75-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ee75-125">Requirement</span></span> | <span data-ttu-id="7ee75-126">Valore</span><span class="sxs-lookup"><span data-stu-id="7ee75-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ee75-127">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ee75-127">Minimum supported client</span></span><br/> | <span data-ttu-id="7ee75-128">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ee75-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7ee75-129">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="7ee75-129">Minimum supported server</span></span><br/> | <span data-ttu-id="7ee75-130">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="7ee75-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7ee75-131">DLL</span><span class="sxs-lookup"><span data-stu-id="7ee75-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ee75-132"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="7ee75-132"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ee75-133">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7ee75-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ee75-134">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="7ee75-134">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




