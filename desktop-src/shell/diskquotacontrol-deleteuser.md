---
description: Elimina un utente dal volume.
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: Metodo DiskQuotaControl. DeleteUser (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104225920"
---
# <a name="diskquotacontroldeleteuser-method"></a><span data-ttu-id="0f5fc-103">DiskQuotaControl. DeleteUser, metodo</span><span class="sxs-lookup"><span data-stu-id="0f5fc-103">DiskQuotaControl.DeleteUser method</span></span>

<span data-ttu-id="0f5fc-104">Elimina un utente dal volume.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-104">Deletes a user from the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f5fc-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0f5fc-105">Syntax</span></span>


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="0f5fc-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0f5fc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f5fc-107">*oUser (valore*</span><span class="sxs-lookup"><span data-stu-id="0f5fc-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="0f5fc-108">Tipo: **Object**</span><span class="sxs-lookup"><span data-stu-id="0f5fc-108">Type: **Object**</span></span>

<span data-ttu-id="0f5fc-109">Espressione di oggetto che restituisce l'oggetto [**DIDiskQuotaUser**](didiskquotauser-object.md) dell'utente.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f5fc-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0f5fc-110">Return value</span></span>

<span data-ttu-id="0f5fc-111">Questo metodo non restituisce valori.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0f5fc-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="0f5fc-112">Remarks</span></span>

<span data-ttu-id="0f5fc-113">Questo metodo ha esito negativo se l'utente è proprietario di una risorsa di archiviazione nel volume.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-113">This method fails if the user owns any storage on the volume.</span></span> <span data-ttu-id="0f5fc-114">Prima di eliminare un utente da un volume, è necessario eliminare tutte le archiviazioni per tale utente, spostarle in un altro volume o fare in modo che la sua proprietà venga trasferita a un altro utente.</span><span class="sxs-lookup"><span data-stu-id="0f5fc-114">Before you delete a user from a volume, all storage for that user must be deleted, be moved to another volume, or have its ownership transferred to another user.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f5fc-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0f5fc-115">Requirements</span></span>



| <span data-ttu-id="0f5fc-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f5fc-116">Requirement</span></span> | <span data-ttu-id="0f5fc-117">Valore</span><span class="sxs-lookup"><span data-stu-id="0f5fc-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f5fc-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f5fc-118">Minimum supported client</span></span><br/> | <span data-ttu-id="0f5fc-119">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f5fc-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0f5fc-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0f5fc-120">Minimum supported server</span></span><br/> | <span data-ttu-id="0f5fc-121">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="0f5fc-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0f5fc-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0f5fc-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f5fc-123"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f5fc-123"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="0f5fc-124">DLL</span><span class="sxs-lookup"><span data-stu-id="0f5fc-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f5fc-125"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="0f5fc-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f5fc-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="0f5fc-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f5fc-127">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="0f5fc-127">**AddUser**</span></span>](diskquotacontrol-adduser.md)
</dt> <dt>

[<span data-ttu-id="0f5fc-128">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="0f5fc-128">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




