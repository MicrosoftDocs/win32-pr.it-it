---
description: Imposta o ottiene un valore booleano che indica se verrà eseguita una voce del registro eventi di sistema quando un utente supera la soglia di quota assegnata.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: Proprietà DiskQuotaControl. LogQuotaThreshold
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fbbf83ae978e46a3867d27c23e8b8f726ba0d7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977167"
---
# <a name="diskquotacontrollogquotathreshold-property"></a><span data-ttu-id="883f6-103">Proprietà DiskQuotaControl. LogQuotaThreshold</span><span class="sxs-lookup"><span data-stu-id="883f6-103">DiskQuotaControl.LogQuotaThreshold property</span></span>

<span data-ttu-id="883f6-104">Imposta o ottiene un valore booleano che indica se verrà eseguita una voce del registro eventi di sistema quando un utente supera la soglia di quota assegnata.</span><span class="sxs-lookup"><span data-stu-id="883f6-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span>

<span data-ttu-id="883f6-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="883f6-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="883f6-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="883f6-106">Syntax</span></span>


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="883f6-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="883f6-107">Property value</span></span>

<span data-ttu-id="883f6-108">Questa proprietà è impostata su **true** se viene eseguita una voce del registro eventi di sistema quando l'utente supera la soglia di avviso della quota o **false** in caso contrario.</span><span class="sxs-lookup"><span data-stu-id="883f6-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota warning threshold, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="883f6-109">Requisiti</span><span class="sxs-lookup"><span data-stu-id="883f6-109">Requirements</span></span>



| <span data-ttu-id="883f6-110">Requisito</span><span class="sxs-lookup"><span data-stu-id="883f6-110">Requirement</span></span> | <span data-ttu-id="883f6-111">Valore</span><span class="sxs-lookup"><span data-stu-id="883f6-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="883f6-112">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="883f6-112">Minimum supported client</span></span><br/> | <span data-ttu-id="883f6-113">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="883f6-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="883f6-114">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="883f6-114">Minimum supported server</span></span><br/> | <span data-ttu-id="883f6-115">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="883f6-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="883f6-116">DLL</span><span class="sxs-lookup"><span data-stu-id="883f6-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="883f6-117"><dt>Shell32.dll (versione 5,0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="883f6-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="883f6-118">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="883f6-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="883f6-119">**DefaultQuotaThreshold**</span><span class="sxs-lookup"><span data-stu-id="883f6-119">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="883f6-120">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="883f6-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="883f6-121">**LogQuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="883f6-121">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




