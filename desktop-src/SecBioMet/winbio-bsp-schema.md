---
title: Struttura WINBIO_BSP_SCHEMA ( \_ tipi WINBIO. h)
description: Descrive le funzionalità di un provider di servizi biometrico.
ms.assetid: d690c735-55a1-4e2c-8b39-d52a1972bf93
keywords:
- Struttura di WINBIO_BSP_SCHEMA Windows Biometric Framework API
- API Windows Biometric Framework puntatore alla struttura PWINBIO_BSP_SCHEMA
topic_type:
- apiref
api_name:
- WINBIO_BSP_SCHEMA
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8ae63aefb64eb22f454559b76e9922242ca9530
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476876"
---
# <a name="winbio_bsp_schema-structure"></a><span data-ttu-id="206c3-105">\_ \_ Struttura dello schema BSP WINBIO</span><span class="sxs-lookup"><span data-stu-id="206c3-105">WINBIO\_BSP\_SCHEMA structure</span></span>

<span data-ttu-id="206c3-106">La **struttura \_ \_ dello schema BSP WINBIO** descrive le funzionalità di un provider di servizi biometrico.</span><span class="sxs-lookup"><span data-stu-id="206c3-106">The **WINBIO\_BSP\_SCHEMA** structure describes the capabilities of a biometric service provider.</span></span> <span data-ttu-id="206c3-107">Questa struttura viene utilizzata dalla funzione [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) .</span><span class="sxs-lookup"><span data-stu-id="206c3-107">This structure is used by the [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="206c3-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="206c3-108">Syntax</span></span>


```C++
typedef struct _WINBIO_BSP_SCHEMA {
  WINBIO_BIOMETRIC_TYPE BiometricFactor;
  WINBIO_UUID           BspId;
  WINBIO_STRING         Description;
  WINBIO_STRING         Vendor;
  WINBIO_VERSION        Version;
} WINBIO_BSP_SCHEMA, *PWINBIO_BSP_SCHEMA;
```



## <a name="members"></a><span data-ttu-id="206c3-109">Members</span><span class="sxs-lookup"><span data-stu-id="206c3-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="206c3-110">**BiometricFactor**</span><span class="sxs-lookup"><span data-stu-id="206c3-110">**BiometricFactor**</span></span>
</dt> <dd>

<span data-ttu-id="206c3-111">Tipo di misurazione biometrica usata dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="206c3-111">The type of biometric measurement used by this device.</span></span> <span data-ttu-id="206c3-112">Attualmente deve essere **WINBIO \_ \_ impronta digitale del tipo**.</span><span class="sxs-lookup"><span data-stu-id="206c3-112">Currently this must be **WINBIO\_TYPE\_FINGERPRINT**.</span></span>

</dd> <dt>

<span data-ttu-id="206c3-113">**BspId**</span><span class="sxs-lookup"><span data-stu-id="206c3-113">**BspId**</span></span>
</dt> <dd>

<span data-ttu-id="206c3-114">Valore che identifica in modo univoco questo componente del provider di servizi biometrico.</span><span class="sxs-lookup"><span data-stu-id="206c3-114">A value that uniquely identifies this biometric service provider component.</span></span>

</dd> <dt>

<span data-ttu-id="206c3-115">**Descrizione**</span><span class="sxs-lookup"><span data-stu-id="206c3-115">**Description**</span></span>
</dt> <dd>

<span data-ttu-id="206c3-116">Stringa Unicode con terminazione **null** che contiene una descrizione del provider di servizi biometrici.</span><span class="sxs-lookup"><span data-stu-id="206c3-116">A **NULL**-terminated Unicode string that contains a description of the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="206c3-117">**Fornitore**</span><span class="sxs-lookup"><span data-stu-id="206c3-117">**Vendor**</span></span>
</dt> <dd>

<span data-ttu-id="206c3-118">Stringa Unicode con terminazione **null** che contiene il nome del fornitore che fornisce il provider di servizi biometrico.</span><span class="sxs-lookup"><span data-stu-id="206c3-118">A **NULL**-terminated Unicode string that contains the name of the vendor supplying the biometric service provider.</span></span>

</dd> <dt>

<span data-ttu-id="206c3-119">**Versione**</span><span class="sxs-lookup"><span data-stu-id="206c3-119">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="206c3-120">Struttura [**di \_ versione di WINBIO**](winbio-version.md) che contiene la versione software del componente provider di servizi biometrico.</span><span class="sxs-lookup"><span data-stu-id="206c3-120">A [**WINBIO\_VERSION**](winbio-version.md) structure the contains the software version of the biometric service provider component.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="206c3-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="206c3-121">Requirements</span></span>



| <span data-ttu-id="206c3-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="206c3-122">Requirement</span></span> | <span data-ttu-id="206c3-123">Valore</span><span class="sxs-lookup"><span data-stu-id="206c3-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="206c3-124">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="206c3-124">Minimum supported client</span></span><br/> | <span data-ttu-id="206c3-125">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="206c3-125">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="206c3-126">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="206c3-126">Minimum supported server</span></span><br/> | <span data-ttu-id="206c3-127">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="206c3-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="206c3-128">Intestazione</span><span class="sxs-lookup"><span data-stu-id="206c3-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="206c3-129"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="206c3-129"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="206c3-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="206c3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="206c3-131">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="206c3-131">Client Application Structures</span></span>](client-application-structures.md)
</dt> <dt>

[<span data-ttu-id="206c3-132">**WinBioEnumServiceProviders**</span><span class="sxs-lookup"><span data-stu-id="206c3-132">**WinBioEnumServiceProviders**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)
</dt> </dl>

 

 





