---
title: Struttura MPRESOURCE_INFO (MpClient. h)
description: Struttura delle informazioni sulle risorse.
ms.assetid: 2D645722-3DE3-4748-B532-3E522464EA1E
keywords:
- Struttura MPRESOURCE_INFO le funzionalità legacy dell'ambiente Windows
- Funzionalità dell'ambiente Windows legacy del puntatore della struttura di PMPRESOURCE_INFO
topic_type:
- apiref
api_name:
- MPRESOURCE_INFO
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dcac6552e0a0060df1bd6a0464fbb8f610395131
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964488"
---
# <a name="mpresource_info-structure"></a><span data-ttu-id="70ea2-105">Struttura delle informazioni di MPRESOURCE \_</span><span class="sxs-lookup"><span data-stu-id="70ea2-105">MPRESOURCE\_INFO structure</span></span>

<span data-ttu-id="70ea2-106">Struttura delle informazioni sulle risorse.</span><span class="sxs-lookup"><span data-stu-id="70ea2-106">Resource information structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="70ea2-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="70ea2-107">Syntax</span></span>


```C++
typedef struct tagMPRESOURCE_INFO {
  MP_MIDL_STRING LPWSTR Scheme;
  MP_MIDL_STRING LPWSTR Path;
  MPRESOURCE_CLASS      Class;
} MPRESOURCE_INFO, *PMPRESOURCE_INFO;
```



## <a name="members"></a><span data-ttu-id="70ea2-108">Members</span><span class="sxs-lookup"><span data-stu-id="70ea2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="70ea2-109">**Schema**</span><span class="sxs-lookup"><span data-stu-id="70ea2-109">**Scheme**</span></span>
</dt> <dd>

<span data-ttu-id="70ea2-110">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="70ea2-110">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="70ea2-111">Identificatore dello schema di risorsa, ad esempio "file" o "dir".</span><span class="sxs-lookup"><span data-stu-id="70ea2-111">Resource scheme identifier such as "file" or "dir".</span></span>

</dd> <dt>

<span data-ttu-id="70ea2-112">**Percorso**</span><span class="sxs-lookup"><span data-stu-id="70ea2-112">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="70ea2-113">Tipo: **\_ \_ LPWSTR stringa MIDL MP**</span><span class="sxs-lookup"><span data-stu-id="70ea2-113">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="70ea2-114">Percorso assoluto della risorsa, in base allo **schema**.</span><span class="sxs-lookup"><span data-stu-id="70ea2-114">Absolute path of resource, based on **Scheme**.</span></span>

</dd> <dt>

<span data-ttu-id="70ea2-115">**Classe**</span><span class="sxs-lookup"><span data-stu-id="70ea2-115">**Class**</span></span>
</dt> <dd>

<span data-ttu-id="70ea2-116">Tipo: **\_ classe MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="70ea2-116">Type: **MPRESOURCE\_CLASS**</span></span>

</dd> <dd>

<span data-ttu-id="70ea2-117">Questo campo viene impostato quando la risorsa viene identificata come parte della minaccia.</span><span class="sxs-lookup"><span data-stu-id="70ea2-117">This field is set when the resource is identified as part of the threat.</span></span> <span data-ttu-id="70ea2-118">Specifica la classe di risorse, principalmente concreta rispetto alla latenza.</span><span class="sxs-lookup"><span data-stu-id="70ea2-118">It specifies the resource class, mainly concrete vs. latent.</span></span> <span data-ttu-id="70ea2-119">Può essere una combinazione di questi valori possibili:</span><span class="sxs-lookup"><span data-stu-id="70ea2-119">It can be a combination of these possible values:</span></span>



| <span data-ttu-id="70ea2-120">Valore</span><span class="sxs-lookup"><span data-stu-id="70ea2-120">Value</span></span>                                                                                                                                                                                                                                                                        | <span data-ttu-id="70ea2-121">Significato</span><span class="sxs-lookup"><span data-stu-id="70ea2-121">Meaning</span></span>                                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <span id="MP_RESOURCE_CLASS_UNKNOWN"></span><span id="mp_resource_class_unknown"></span><dl> <span data-ttu-id="70ea2-122"><dt>**MP \_ Classe di risorse \_ \_ sconosciuta**</dt> <dt>0x0000</dt></span><span class="sxs-lookup"><span data-stu-id="70ea2-122"><dt>**MP\_RESOURCE\_CLASS\_UNKNOWN**</dt> <dt>0x0000</dt></span></span> </dl>              |                                                                       |
| <span id="MP_RESOURCE_CLASS_CONCRETE"></span><span id="mp_resource_class_concrete"></span><dl> <span data-ttu-id="70ea2-123"><dt>**MP \_ 0x0001 \_ \_ concrete della classe di risorse**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="70ea2-123"><dt>**MP\_RESOURCE\_CLASS\_CONCRETE**</dt> <dt>0x0001</dt></span></span> </dl>           | <span data-ttu-id="70ea2-124">Si escludono a vicenda con la **\_ classe di risorse MP \_ \_ latente**.</span><span class="sxs-lookup"><span data-stu-id="70ea2-124">Mutually exclusive with **MP\_RESOURCE\_CLASS\_LATENT**.</span></span><br/>   |
| <span id="MP_RESOURCE_CLASS_LATENT"></span><span id="mp_resource_class_latent"></span><dl> <span data-ttu-id="70ea2-125"><dt>**MP \_ Classe di risorse \_ \_ latenza**</dt> <dt>0x0002</dt></span><span class="sxs-lookup"><span data-stu-id="70ea2-125"><dt>**MP\_RESOURCE\_CLASS\_LATENT**</dt> <dt>0x0002</dt></span></span> </dl>                 | <span data-ttu-id="70ea2-126">Si escludono a vicenda con la **\_ classe di risorse MP \_ \_ concreta**.</span><span class="sxs-lookup"><span data-stu-id="70ea2-126">Mutually exclusive with **MP\_RESOURCE\_CLASS\_CONCRETE**.</span></span><br/> |
| <span id="MP_RESOURCE_CLASS_SAMPLE_FILE"></span><span id="mp_resource_class_sample_file"></span><dl> <span data-ttu-id="70ea2-127"><dt>**MP \_ Classe di risorse \_ \_ \_ file di esempio**</dt> <dt>0x0004</dt></span><span class="sxs-lookup"><span data-stu-id="70ea2-127"><dt>**MP\_RESOURCE\_CLASS\_SAMPLE\_FILE**</dt> <dt>0x0004</dt></span></span> </dl> |                                                                       |
| <span id="MP_RESOURCE_CLASS_SHARED"></span><span id="mp_resource_class_shared"></span><dl> <span data-ttu-id="70ea2-128"><dt>**MP \_ Classe di risorse \_ \_ Shared**</dt> <dt>0x0100</dt></span><span class="sxs-lookup"><span data-stu-id="70ea2-128"><dt>**MP\_RESOURCE\_CLASS\_SHARED**</dt> <dt>0x0100</dt></span></span> </dl>                 |                                                                       |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="70ea2-129">Requisiti</span><span class="sxs-lookup"><span data-stu-id="70ea2-129">Requirements</span></span>



| <span data-ttu-id="70ea2-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="70ea2-130">Requirement</span></span> | <span data-ttu-id="70ea2-131">Valore</span><span class="sxs-lookup"><span data-stu-id="70ea2-131">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="70ea2-132">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70ea2-132">Minimum supported client</span></span><br/> | <span data-ttu-id="70ea2-133">\[Solo app desktop di Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="70ea2-133">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="70ea2-134">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="70ea2-134">Minimum supported server</span></span><br/> | <span data-ttu-id="70ea2-135">\[Solo app desktop Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="70ea2-135">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="70ea2-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="70ea2-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="70ea2-137"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="70ea2-137"><dt>MpClient.h</dt></span></span> </dl> |



 

 





