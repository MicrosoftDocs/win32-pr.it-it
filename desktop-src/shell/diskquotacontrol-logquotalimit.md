---
description: Imposta o ottiene un valore booleano che indica se verrà eseguita una voce del registro eventi di sistema quando un utente supera il limite di quota assegnato.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: Proprietà DiskQuotaControl. LogQuotaLimit
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3db64d7fb06ed8bfb7ba8c2483eb413f3f01a224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977170"
---
# <a name="diskquotacontrollogquotalimit-property"></a><span data-ttu-id="71777-103">Proprietà DiskQuotaControl. LogQuotaLimit</span><span class="sxs-lookup"><span data-stu-id="71777-103">DiskQuotaControl.LogQuotaLimit property</span></span>

<span data-ttu-id="71777-104">Imposta o ottiene un valore booleano che indica se verrà eseguita una voce del registro eventi di sistema quando un utente supera il limite di quota assegnato.</span><span class="sxs-lookup"><span data-stu-id="71777-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span>

<span data-ttu-id="71777-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="71777-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="71777-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="71777-106">Syntax</span></span>


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="71777-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="71777-107">Property value</span></span>

<span data-ttu-id="71777-108">Questa proprietà è impostata su **true** se viene eseguita una voce del registro eventi di sistema quando l'utente supera il limite di quota o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="71777-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota limit, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="71777-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="71777-109">Requirements</span></span>



| <span data-ttu-id="71777-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="71777-110">Requirement</span></span> | <span data-ttu-id="71777-111">Valore</span><span class="sxs-lookup"><span data-stu-id="71777-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71777-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71777-112">Minimum supported client</span></span><br/> | <span data-ttu-id="71777-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="71777-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="71777-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="71777-114">Minimum supported server</span></span><br/> | <span data-ttu-id="71777-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="71777-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="71777-116">DLL</span><span class="sxs-lookup"><span data-stu-id="71777-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="71777-117"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="71777-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="71777-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="71777-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71777-119">**DefaultQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="71777-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="71777-120">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="71777-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="71777-121">**LogQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="71777-121">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




