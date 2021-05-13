---
description: Imposta o ottiene lo stato delle quote disco del volume.
title: DiskQuotaControl.QuotaState - proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.QuotaState
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: b0766ecf-6e22-4481-a6a7-df873a277bc2
ms.openlocfilehash: 3580ad47a5ec6a5d0276dc0e30a4a6463aca2fb3
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843192"
---
# <a name="diskquotacontrolquotastate-property"></a><span data-ttu-id="3765f-103">DiskQuotaControl.QuotaState - proprietà</span><span class="sxs-lookup"><span data-stu-id="3765f-103">DiskQuotaControl.QuotaState property</span></span>

<span data-ttu-id="3765f-104">Imposta o ottiene lo stato delle quote disco del volume.</span><span class="sxs-lookup"><span data-stu-id="3765f-104">Sets or gets the state of the volume's disk quotas.</span></span>

<span data-ttu-id="3765f-105">Si tratta di una proprietà di lettura/scrittura.</span><span class="sxs-lookup"><span data-stu-id="3765f-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3765f-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="3765f-106">Syntax</span></span>


```JScript
iQuotaState = DiskQuotaControl.QuotaState
DiskQuotaControl.QuotaState = iQuotaState
```



## <a name="property-value"></a><span data-ttu-id="3765f-107">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="3765f-107">Property value</span></span>

<span data-ttu-id="3765f-108">Questa proprietà può essere impostata su uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="3765f-108">This property can be set to one of the following values.</span></span>



| <span data-ttu-id="3765f-109">State</span><span class="sxs-lookup"><span data-stu-id="3765f-109">State</span></span>          | <span data-ttu-id="3765f-110">Valore</span><span class="sxs-lookup"><span data-stu-id="3765f-110">Value</span></span> | <span data-ttu-id="3765f-111">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3765f-111">Description</span></span>               |
|----------------|-------|---------------------------|
| <span data-ttu-id="3765f-112">dqStateDisable</span><span class="sxs-lookup"><span data-stu-id="3765f-112">dqStateDisable</span></span> | <span data-ttu-id="3765f-113">0</span><span class="sxs-lookup"><span data-stu-id="3765f-113">0</span></span>     | <span data-ttu-id="3765f-114">Le quote disco sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="3765f-114">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="3765f-115">dqStateTrack</span><span class="sxs-lookup"><span data-stu-id="3765f-115">dqStateTrack</span></span>   | <span data-ttu-id="3765f-116">1</span><span class="sxs-lookup"><span data-stu-id="3765f-116">1</span></span>     | <span data-ttu-id="3765f-117">Le quote disco sono disabilitate.</span><span class="sxs-lookup"><span data-stu-id="3765f-117">Disk quotas are disabled.</span></span> |
| <span data-ttu-id="3765f-118">dqStateEnforce</span><span class="sxs-lookup"><span data-stu-id="3765f-118">dqStateEnforce</span></span> | <span data-ttu-id="3765f-119">2</span><span class="sxs-lookup"><span data-stu-id="3765f-119">2</span></span>     | <span data-ttu-id="3765f-120">Applicare il limite di quota.</span><span class="sxs-lookup"><span data-stu-id="3765f-120">Enforce quota limit.</span></span>      |



 

## <a name="requirements"></a><span data-ttu-id="3765f-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="3765f-121">Requirements</span></span>



| <span data-ttu-id="3765f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="3765f-122">Requirement</span></span> | <span data-ttu-id="3765f-123">Valore</span><span class="sxs-lookup"><span data-stu-id="3765f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3765f-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3765f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3765f-125">Windows 2000 Professional \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3765f-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3765f-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="3765f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3765f-127">Windows 2000 Server \[solo app desktop\]</span><span class="sxs-lookup"><span data-stu-id="3765f-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3765f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3765f-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3765f-129"><dt>Shell32.dll (versione 5.0 o successiva)</dt></span><span class="sxs-lookup"><span data-stu-id="3765f-129"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3765f-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="3765f-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3765f-131">**Oggetto DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="3765f-131">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




