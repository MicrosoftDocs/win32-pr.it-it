---
title: Struttura WINBIO_BDB_ANSI_381_HEADER ( \_ tipi WINBIO. h)
description: Specifica le informazioni su una serie di campioni di impronte digitali o di Palm.
ms.assetid: 8b0caa50-9bba-45c4-b4bf-514540894793
keywords:
- Struttura di WINBIO_BDB_ANSI_381_HEADER Windows Biometric Framework API
topic_type:
- apiref
api_name:
- WINBIO_BDB_ANSI_381_HEADER
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9da04643bbdff273a2594394011ba46c16bfa29d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301636"
---
# <a name="winbio_bdb_ansi_381_header-structure"></a><span data-ttu-id="ab5a7-104">\_Struttura dell'intestazione WINBIO BDB \_ ANSI \_ 381 \_</span><span class="sxs-lookup"><span data-stu-id="ab5a7-104">WINBIO\_BDB\_ANSI\_381\_HEADER structure</span></span>

<span data-ttu-id="ab5a7-105">La struttura di **\_ intestazione WINBIO BDB \_ ANSI \_ 381 \_** specifica informazioni su una serie di campioni di impronte digitali o di Palm.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-105">The **WINBIO\_BDB\_ANSI\_381\_HEADER** structure specifies information about a series of fingerprint or palm samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab5a7-106">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab5a7-106">Syntax</span></span>


```C++
typedef struct _WINBIO_BDB_ANSI_381_HEADER {
  ULONG64                  RecordLength;
  ULONG                    FormatIdentifier;
  ULONG                    VersionNumber;
  WINBIO_REGISTERED_FORMAT ProductId;
  USHORT                   CaptureDeviceId;
  USHORT                   ImageAcquisitionLevel;
  USHORT                   HorizontalScanResolution;
  USHORT                   VerticalScanResolution;
  USHORT                   HorizontalImageResolution;
  USHORT                   VerticalImageResolution;
  UCHAR                    ElementCount;
  UCHAR                    ScaleUnits;
  UCHAR                    PixelDepth;
  UCHAR                    ImageCompressionAlg;
  USHORT                   Reserved;
} WINBIO_BDB_ANSI_381_HEADER;
```



## <a name="members"></a><span data-ttu-id="ab5a7-107">Members</span><span class="sxs-lookup"><span data-stu-id="ab5a7-107">Members</span></span>

<dl> <dt>

<span data-ttu-id="ab5a7-108">**RecordLength**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-108">**RecordLength**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-109">Dimensione, in byte, della struttura più le dimensioni di tutte le strutture [**di \_ record WINBIO BDB \_ ANSI \_ 381 \_**](winbio-bdb-ansi-381-record.md) per gli esempi di impronte digitali o di Palma acquisiti da un utente finale.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-109">The size, in bytes, of this structure plus the size of all [**WINBIO\_BDB\_ANSI\_381\_RECORD**](winbio-bdb-ansi-381-record.md) structures for the fingerprint or palm samples captured from an end user.</span></span> <span data-ttu-id="ab5a7-110">Solo i sei byte bassi sono validi.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-110">Only the low six bytes are valid.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-111">**FormatIdentifier**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-111">**FormatIdentifier**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-112">Specifica il formato.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-112">Specifies the format.</span></span> <span data-ttu-id="ab5a7-113">Attualmente, deve essere 0x46495200.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-113">Currently, this must be 0x46495200.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-114">**VersionNumber**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-114">**VersionNumber**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-115">Specifica il numero di versione.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-115">Specifies the version number.</span></span> <span data-ttu-id="ab5a7-116">Attualmente deve essere 0x30313000 che corrisponde internamente a 0.1.0.0.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-116">Currently this must be 0x30313000 which corresponds internally to 0.1.0.0.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-117">**ProductId**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-117">**ProductId**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-118">Struttura [**di \_ \_ formato registrata WINBIO**](winbio-registered-format.md) che contiene il formato dati registrato come coppia proprietario/tipo.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-118">A [**WINBIO\_REGISTERED\_FORMAT**](winbio-registered-format.md) structure that contains the registered data format as an owner/type pair.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-119">**CaptureDeviceId**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-119">**CaptureDeviceId**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-120">Contiene l'ID unità del dispositivo usato per acquisire l'esempio.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-120">Contains the unit ID of the device used to capture the sample.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-121">**ImageAcquisitionLevel**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-121">**ImageAcquisitionLevel**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-122">Specifica il livello di risoluzione in corrispondenza del quale viene acquisito l'esempio.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-122">Specifies the resolution level at which the sample is captured.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-123">**HorizontalScanResolution**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-123">**HorizontalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-124">Specifica la risoluzione orizzontale dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-124">Specifies the horizontal resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-125">**VerticalScanResolution**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-125">**VerticalScanResolution**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-126">Specifica la risoluzione verticale dell'analisi.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-126">Specifies the vertical resolution of the scan.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-127">**HorizontalImageResolution**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-127">**HorizontalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-128">Specifica la risoluzione orizzontale dell'impronta digitale acquisita o dell'immagine Palm.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-128">Specifies the horizontal resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-129">**VerticalImageResolution**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-129">**VerticalImageResolution**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-130">Specifica la risoluzione verticale dell'impronta digitale acquisita o dell'immagine Palm.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-130">Specifies the vertical resolution of the captured fingerprint or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-131">**Valore elementCount**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-131">**ElementCount**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-132">Numero di record del dito o della palma nella struttura.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-132">Number of finger or palm records in this structure.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-133">**ScaleUnits**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-133">**ScaleUnits**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-134">Contiene l'unità di misura, 1 per i pollici e 2 per centimetri.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-134">Contains the unit of measure, 1 for inches and 2 for centimeters.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-135">**PixelDepth**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-135">**PixelDepth**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-136">Specifica il numero di bit in un pixel.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-136">Specifies the number of bits in a pixel.</span></span> <span data-ttu-id="ab5a7-137">Questo può essere da 1 a 16 bit per pixel per il colore.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-137">This can be 1 to 16 bits per pixel for color.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-138">**ImageCompressionAlg**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-138">**ImageCompressionAlg**</span></span>
</dt> <dd>

<span data-ttu-id="ab5a7-139">Specifica l'algoritmo usato per comprimere il dito o l'immagine Palm.</span><span class="sxs-lookup"><span data-stu-id="ab5a7-139">Specifies the algorithm used to compress the finger or palm image.</span></span>

</dd> <dt>

<span data-ttu-id="ab5a7-140">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="ab5a7-140">**Reserved**</span></span>
<span data-ttu-id="ab5a7-141"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="ab5a7-141"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="ab5a7-142">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab5a7-142">Requirements</span></span>



| <span data-ttu-id="ab5a7-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab5a7-143">Requirement</span></span> | <span data-ttu-id="ab5a7-144">Valore</span><span class="sxs-lookup"><span data-stu-id="ab5a7-144">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab5a7-145">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab5a7-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ab5a7-146">\[Solo app desktop di Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ab5a7-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="ab5a7-147">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab5a7-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ab5a7-148">Solo app desktop Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ab5a7-148">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ab5a7-149">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ab5a7-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab5a7-150"><dt>\_Tipi WinBio. h (includere WinBio. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ab5a7-150"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab5a7-151">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab5a7-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab5a7-152">Strutture delle applicazioni client</span><span class="sxs-lookup"><span data-stu-id="ab5a7-152">Client Application Structures</span></span>](client-application-structures.md)
</dt> </dl>

 

 





