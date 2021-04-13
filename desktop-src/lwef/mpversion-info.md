---
title: Struttura MPVERSION_INFO (MpClient. h)
description: Informazioni sulla versione per i componenti di malware Protection Manager.
ms.assetid: C18EE6FE-57E1-4814-85CA-19C3ACE275D2
keywords:
- Struttura MPVERSION_INFO le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPVERSION_INFO
topic_type:
- apiref
api_name:
- MPVERSION_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f30153c427b880600a3d8aeb3c411a8679cd64b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104341043"
---
# <a name="mpversion_info-structure"></a><span data-ttu-id="ad156-105">Struttura delle informazioni di MPVERSION \_</span><span class="sxs-lookup"><span data-stu-id="ad156-105">MPVERSION\_INFO structure</span></span>

<span data-ttu-id="ad156-106">Informazioni sulla versione per i componenti di malware Protection Manager.</span><span class="sxs-lookup"><span data-stu-id="ad156-106">Version information for the malware protection manager's components.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad156-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ad156-107">Syntax</span></span>


```C++
typedef struct tagMPVERSION_INFO {
  MPCOMPONENT_VERSION Product;
  MPCOMPONENT_VERSION Service;
  MPCOMPONENT_VERSION FileSystemFilter;
  MPCOMPONENT_VERSION Engine;
  MPCOMPONENT_VERSION ASSignature;
  MPCOMPONENT_VERSION AVSignature;
  MPCOMPONENT_VERSION NISEngine;
  MPCOMPONENT_VERSION NISSignature;
  MPCOMPONENT_VERSION Reserved[4];
} MPVERSION_INFO, *PMPVERSION_INFO;
```



## <a name="members"></a><span data-ttu-id="ad156-108">Members</span><span class="sxs-lookup"><span data-stu-id="ad156-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="ad156-109">**Prodotto**</span><span class="sxs-lookup"><span data-stu-id="ad156-109">**Product**</span></span>
</dt> <dd>

<span data-ttu-id="ad156-110">Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="ad156-110">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad156-111">Versione del prodotto.</span><span class="sxs-lookup"><span data-stu-id="ad156-111">Product version.</span></span>

</dd> <dt>

<span data-ttu-id="ad156-112">**Servizio**</span><span class="sxs-lookup"><span data-stu-id="ad156-112">**Service**</span></span>
</dt> <dd>

<span data-ttu-id="ad156-113">Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="ad156-113">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad156-114">Versione del componente del servizio.</span><span class="sxs-lookup"><span data-stu-id="ad156-114">Service component version.</span></span>

</dd> <dt>

<span data-ttu-id="ad156-115">**FileSystemFilter**</span><span class="sxs-lookup"><span data-stu-id="ad156-115">**FileSystemFilter**</span></span>
</dt> <dd>

<span data-ttu-id="ad156-116">Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="ad156-116">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad156-117">Versione del componente filtro del file System.</span><span class="sxs-lookup"><span data-stu-id="ad156-117">File system filter component version.</span></span>

</dd> <dt>

<span data-ttu-id="ad156-118">**Motore**</span><span class="sxs-lookup"><span data-stu-id="ad156-118">**Engine**</span></span>
</dt> <dd>

<span data-ttu-id="ad156-119">Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="ad156-119">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad156-120">Versione del componente del motore.</span><span class="sxs-lookup"><span data-stu-id="ad156-120">Engine component version.</span></span>

</dd> <dt>

<span data-ttu-id="ad156-121">**ASSignature**</span><span class="sxs-lookup"><span data-stu-id="ad156-121">**ASSignature**</span></span>
</dt> <dd>

<span data-ttu-id="ad156-122">Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="ad156-122">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad156-123">Versione del componente della firma antispyware.</span><span class="sxs-lookup"><span data-stu-id="ad156-123">Antispyware signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="ad156-124">**AVSignature**</span><span class="sxs-lookup"><span data-stu-id="ad156-124">**AVSignature**</span></span>
</dt> <dd>

<span data-ttu-id="ad156-125">Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="ad156-125">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad156-126">Versione del componente della firma antivirus.</span><span class="sxs-lookup"><span data-stu-id="ad156-126">Antivirus signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="ad156-127">**NISEngine**</span><span class="sxs-lookup"><span data-stu-id="ad156-127">**NISEngine**</span></span>
</dt> <dd>

<span data-ttu-id="ad156-128">Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="ad156-128">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad156-129">Versione del motore NIS.</span><span class="sxs-lookup"><span data-stu-id="ad156-129">NIS engine version.</span></span>

</dd> <dt>

<span data-ttu-id="ad156-130">**NISSignature**</span><span class="sxs-lookup"><span data-stu-id="ad156-130">**NISSignature**</span></span>
</dt> <dd>

<span data-ttu-id="ad156-131">Tipo: **[ **MPCOMPONENT \_ Version**](mpcomponent-version.md)**</span><span class="sxs-lookup"><span data-stu-id="ad156-131">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)**</span></span>

</dd> <dd>

<span data-ttu-id="ad156-132">Versione del componente firma della firma NIS.</span><span class="sxs-lookup"><span data-stu-id="ad156-132">NIS Signature signature component version.</span></span>

</dd> <dt>

<span data-ttu-id="ad156-133">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="ad156-133">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="ad156-134">Tipo: **[**MPCOMPONENT \_ versione**](mpcomponent-version.md) \[ 4\]**</span><span class="sxs-lookup"><span data-stu-id="ad156-134">Type: **[**MPCOMPONENT\_VERSION**](mpcomponent-version.md)\[4\]**</span></span>

</dd> <dd>

<span data-ttu-id="ad156-135">Campi riservati.</span><span class="sxs-lookup"><span data-stu-id="ad156-135">Reserved fields.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ad156-136">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ad156-136">Requirements</span></span>



| <span data-ttu-id="ad156-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad156-137">Requirement</span></span> | <span data-ttu-id="ad156-138">Valore</span><span class="sxs-lookup"><span data-stu-id="ad156-138">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ad156-139">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad156-139">Minimum supported client</span></span><br/> | <span data-ttu-id="ad156-140">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="ad156-140">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="ad156-141">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ad156-141">Minimum supported server</span></span><br/> | <span data-ttu-id="ad156-142">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="ad156-142">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="ad156-143">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ad156-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad156-144"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad156-144"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad156-145">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ad156-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad156-146">**versione di MPCOMPONENT \_**</span><span class="sxs-lookup"><span data-stu-id="ad156-146">**MPCOMPONENT\_VERSION**</span></span>](mpcomponent-version.md)
</dt> </dl>

 

 





