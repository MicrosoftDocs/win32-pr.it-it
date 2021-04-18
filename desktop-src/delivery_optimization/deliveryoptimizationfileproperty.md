---
title: Enumerazione DeliveryOptimizationFileProperty (Deliveryoptimization. h)
description: L'enumerazione DeliveryOptimizationFileProperty specifica l'ID di una proprietà facoltativa per il file DO.
keywords:
- Enumerazione DeliveryOptimizationFileProperty
topic_type:
- apiref
api_name:
- DeliveryOptimizationFileProperty
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 01/18/2019
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 238ad815149f7d40dd1902b991608e0a3005eb35
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301492"
---
# <a name="deliveryoptimizationfileproperty-enumeration"></a><span data-ttu-id="dc2d5-104">Enumerazione DeliveryOptimizationFileProperty</span><span class="sxs-lookup"><span data-stu-id="dc2d5-104">DeliveryOptimizationFileProperty enumeration</span></span>

<span data-ttu-id="dc2d5-105">L'enumerazione DeliveryOptimizationFileProperty specifica l'ID di una proprietà facoltativa per il file DO.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-105">The DeliveryOptimizationFileProperty enumeration specifies the ID of an optional property for the DO file.</span></span> <span data-ttu-id="dc2d5-106">Questa enumerazione viene utilizzata nell'interfaccia IDeliveryOptimizationFile2 in cui viene passato il valore della proprietà di tipo VARIANT</span><span class="sxs-lookup"><span data-stu-id="dc2d5-106">This enumeration is used in the IDeliveryOptimizationFile2 interface where the property value of type VARIANT is passed</span></span>

## <a name="syntax"></a><span data-ttu-id="dc2d5-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="dc2d5-107">Syntax</span></span>

```C++
typedef enum _DeliveryOptimizationFileProperty {  
  DOFilePropertyId_DecryptionInfo,
  DOFilePropertyId_IntegrityCheckInfo,
  DOFilePropertyId_IntegrityCheckMandatory,
  DOFilePropertyId_DownloadSinkInterface,
  DOFilePropertyId_DownloadSinkFilePath,
  DOFilePropertyId_DownloadSinkMemoryStream,
  DOFilePropertyId_TotalSizeBytes
} DOFilePropertyId;
```

## <a name="constants"></a><span data-ttu-id="dc2d5-108">Costanti</span><span class="sxs-lookup"><span data-stu-id="dc2d5-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="dc2d5-109">DOFilePropertyId_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="dc2d5-109">DOFilePropertyId_DecryptionInfo</span></span>
</dt> <dd>

<span data-ttu-id="dc2d5-110">L'ID di proprietà DOFilePropertyId_DecryptionInfo imposta le informazioni di decrittografia sotto forma di stringa JSON.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-110">The DOFilePropertyId_DecryptionInfo property ID sets decryption information in the form of a JSON string.</span></span> <span data-ttu-id="dc2d5-111">DOFilePropertyId_DecryptionInfo è una proprietà di sola scrittura di tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-111">DOFilePropertyId_DecryptionInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="dc2d5-112">DOFilePropertyId_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="dc2d5-112">DOFilePropertyId_IntegrityCheckInfo</span></span>
</dt> <dd>

<span data-ttu-id="dc2d5-113">Il DOFilePropertyId_IntegrityCheckInfo ID proprietà imposta il percorso del file hash della parte (PHF), che viene usato da DO per eseguire i controlli di integrità del runtime sul contenuto scaricato.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-113">The DOFilePropertyId_IntegrityCheckInfo property ID sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="dc2d5-114">DOFilePropertyId_IntegrityCheckInfo è una proprietà di sola scrittura di tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-114">DOFilePropertyId_IntegrityCheckInfo is a Write only property of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="dc2d5-115">DOFilePropertyId_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="dc2d5-115">DOFilePropertyId_IntegrityCheckMandatory</span></span>
</dt> <dd>

<span data-ttu-id="dc2d5-116">Il DOFilePropertyId_IntegrityCheckMandatory ID proprietà imposta un flag booleano che indica se l'utilizzo di PHF è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-116">The DOFilePropertyId_IntegrityCheckMandatory property ID sets a boolean flag indicating whether usage of the PHF is mandatory.</span></span> <span data-ttu-id="dc2d5-117">Se TRUE, il download verrà interrotto dopo che il controllo di integrità non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-117">If TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="dc2d5-118">DOFilePropertyId_IntegrityCheckMandatory è una proprietà di lettura/scrittura di tipo VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-118">DOFilePropertyId_IntegrityCheckMandatory is a Read/Write property of type VT_BOOL.</span></span>

</dd> <dt>

<span data-ttu-id="dc2d5-119">DOFilePropertyId_DownloadSinkFilePath</span><span class="sxs-lookup"><span data-stu-id="dc2d5-119">DOFilePropertyId_DownloadSinkFilePath</span></span>
</dt> <dd>

<span data-ttu-id="dc2d5-120">L'ID della proprietà DOFilePropertyId_DownloadSinkFilePath imposta un percorso file system completo in cui devono essere archiviate le parti scaricate.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-120">The DOFilePropertyId_DownloadSinkFilePath property ID sets a fully qualified file system location where DO should store the downloaded pieces.</span></span> <span data-ttu-id="dc2d5-121">DOFilePropertyId_DownloadSinkFilePath è di tipo VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-121">DOFilePropertyId_DownloadSinkFilePath is of type VT_BSTR.</span></span>

</dd> <dt>

<span data-ttu-id="dc2d5-122">DOFilePropertyId_DownloadSinkMemoryStream</span><span class="sxs-lookup"><span data-stu-id="dc2d5-122">DOFilePropertyId_DownloadSinkMemoryStream</span></span>
</dt> <dd>

<span data-ttu-id="dc2d5-123">L'ID di proprietà DOFilePropertyId_DownloadSinkMemoryStream è deprecato.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-123">The DOFilePropertyId_DownloadSinkMemoryStream property ID is deprecated.</span></span> <span data-ttu-id="dc2d5-124">Non usare.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-124">Do not use.</span></span>

</dd> <dt>

<span data-ttu-id="dc2d5-125">DOFilePropertyId_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="dc2d5-125">DOFilePropertyId_TotalSizeBytes</span></span>
</dt> <dd>

<span data-ttu-id="dc2d5-126">Il DOFilePropertyId_TotalSizeBytes ID proprietà specifica la dimensione totale del download.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-126">The DOFilePropertyId_TotalSizeBytes property ID specifies the total download size.</span></span> <span data-ttu-id="dc2d5-127">DOFilePropertyId_TotalSizeBytes è di tipo VT_UI8.</span><span class="sxs-lookup"><span data-stu-id="dc2d5-127">DOFilePropertyId_TotalSizeBytes is of type VT_UI8.</span></span>
</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dc2d5-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="dc2d5-128">Requirements</span></span>

| <span data-ttu-id="dc2d5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="dc2d5-129">Requirement</span></span> | <span data-ttu-id="dc2d5-130">Valore</span><span class="sxs-lookup"><span data-stu-id="dc2d5-130">Value</span></span> |
|-------------------------------|----------------------------------------------------------|
| <span data-ttu-id="dc2d5-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc2d5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="dc2d5-132">Solo app desktop Windows 10 versione 1803 \[\]</span><span class="sxs-lookup"><span data-stu-id="dc2d5-132">Windows 10, version 1803 \[desktop apps only\]</span></span><br/>      |
| <span data-ttu-id="dc2d5-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="dc2d5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="dc2d5-134">Windows Server, versione 1709 \[ solo per le app desktop\]</span><span class="sxs-lookup"><span data-stu-id="dc2d5-134">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>  |
| <span data-ttu-id="dc2d5-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="dc2d5-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc2d5-136"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc2d5-136"><dt>Deliveryoptimization.h</dt></span></span> </dl>               |
