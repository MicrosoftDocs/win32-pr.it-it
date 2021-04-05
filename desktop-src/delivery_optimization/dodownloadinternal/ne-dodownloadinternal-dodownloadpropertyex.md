---
title: Enumerazione DODownloadPropertyEx
description: Specifica l'ID delle proprietà estese per l'operazione di download.
keywords:
- Enumerazione DODownloadPropertyEx, DODownloadPropertyEx
topic_type:
- apiref
api_name:
- DODownloadPropertyEx
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/29/2019
ms.openlocfilehash: 5df0f53778d9059ef8767f5b8052940847e36c00
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873945"
---
# <a name="dodownloadpropertyex-enumeration"></a><span data-ttu-id="61083-104">Enumerazione DODownloadPropertyEx</span><span class="sxs-lookup"><span data-stu-id="61083-104">DODownloadPropertyEx enumeration</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61083-105">L'enumerazione **DODownloadPropertyEx** è deprecata.</span><span class="sxs-lookup"><span data-stu-id="61083-105">The **DODownloadPropertyEx** enumeration is deprecated.</span></span> <span data-ttu-id="61083-106">Usare invece l'enumerazione [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) con [IDODownload:: GetProperty](../do/nf-do-idodownload-getproperty.md) e [IDODownload:: SetProperty](../do/nf-do-idodownload-setproperty.md).</span><span class="sxs-lookup"><span data-stu-id="61083-106">Instead, use the [DODownloadProperty](../deliveryoptimizationdownloadtypes/ne-deliveryoptimizationdownloadtypes-dodownloadproperty.md) enumeration with [IDODownload::GetProperty](../do/nf-do-idodownload-getproperty.md) and [IDODownload::SetProperty](../do/nf-do-idodownload-setproperty.md).</span></span>

<span data-ttu-id="61083-107">L'enumerazione **DODownloadPropertyEx** specifica l'ID delle proprietà estese per l'operazione di download.</span><span class="sxs-lookup"><span data-stu-id="61083-107">The **DODownloadPropertyEx** enumeration specifies the ID of extended properties for the DO download operation.</span></span> <span data-ttu-id="61083-108">Questa enumerazione viene usata dall'interfaccia **IDODownloadInternal** e un valore **Variant** viene usato per ottenere e impostare il valore della proprietà.</span><span class="sxs-lookup"><span data-stu-id="61083-108">This enumeration is used by the **IDODownloadInternal** interface, and a **VARIANT** value is used to get and set the property value.</span></span>

## <a name="syntax"></a><span data-ttu-id="61083-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="61083-109">Syntax</span></span>

```cpp
typedef enum _DODownloadPropertyEx
{
  DODownloadPropertyEx_UpdateId = 0,
  DODownloadPropertyEx_CorrelationVector,
  DODownloadPropertyEx_DecryptionInfo,    
  DODownloadPropertyEx_IntegrityCheckInfo,   
  DODownloadPropertyEx_IntegrityCheckMandatory, 
  DODownloadPropertyEx_TotalSizeBytes, 
  DODownloadPropertyEx_TempLocalFileUsage 
} DODownloadPropertyEx;
```
## <a name="constants"></a><span data-ttu-id="61083-110">Costanti</span><span class="sxs-lookup"><span data-stu-id="61083-110">Constants</span></span>

| <span data-ttu-id="61083-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="61083-111">Requirement</span></span> | <span data-ttu-id="61083-112">Valore</span><span class="sxs-lookup"><span data-stu-id="61083-112">Value</span></span> |
|-|-|
| <span data-ttu-id="61083-113">DODownloadPropertyEx_UpdateId</span><span class="sxs-lookup"><span data-stu-id="61083-113">DODownloadPropertyEx_UpdateId</span></span> | <span data-ttu-id="61083-114">Riservato.</span><span class="sxs-lookup"><span data-stu-id="61083-114">Reserved.</span></span> <span data-ttu-id="61083-115">Non usare.</span><span class="sxs-lookup"><span data-stu-id="61083-115">Do not use.</span></span> |
| <span data-ttu-id="61083-116">DODownloadPropertyEx_CorrelationVector</span><span class="sxs-lookup"><span data-stu-id="61083-116">DODownloadPropertyEx_CorrelationVector</span></span> | <span data-ttu-id="61083-117">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="61083-117">Optional.</span></span> <span data-ttu-id="61083-118">Imposta un vettore di correlazione specifico per scopi di telemetria.</span><span class="sxs-lookup"><span data-stu-id="61083-118">Sets a specific correlation vector for telemetry purposes.</span></span> <span data-ttu-id="61083-119">Il tipo VARIANT è VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="61083-119">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="61083-120">DODownloadPropertyEx_DecryptionInfo</span><span class="sxs-lookup"><span data-stu-id="61083-120">DODownloadPropertyEx_DecryptionInfo</span></span> | <span data-ttu-id="61083-121">Riservato.</span><span class="sxs-lookup"><span data-stu-id="61083-121">Reserved.</span></span> <span data-ttu-id="61083-122">Non usare.</span><span class="sxs-lookup"><span data-stu-id="61083-122">Do not use.</span></span> |
| <span data-ttu-id="61083-123">DODownloadPropertyEx_IntegrityCheckInfo</span><span class="sxs-lookup"><span data-stu-id="61083-123">DODownloadPropertyEx_IntegrityCheckInfo</span></span> | <span data-ttu-id="61083-124">Facoltativo di sola scrittura.</span><span class="sxs-lookup"><span data-stu-id="61083-124">Optional write-only.</span></span> <span data-ttu-id="61083-125">Imposta il percorso del file hash della parte (PHF), usato da DO per eseguire i controlli di integrità di runtime sul contenuto scaricato.</span><span class="sxs-lookup"><span data-stu-id="61083-125">Sets the piece hash file (PHF) location, which is used by DO to perform runtime integrity checks on the downloaded content.</span></span> <span data-ttu-id="61083-126">Il tipo VARIANT è VT_BSTR.</span><span class="sxs-lookup"><span data-stu-id="61083-126">VARIANT type is VT_BSTR.</span></span> |
| <span data-ttu-id="61083-127">DODownloadPropertyEx_IntegrityCheckMandatory</span><span class="sxs-lookup"><span data-stu-id="61083-127">DODownloadPropertyEx_IntegrityCheckMandatory</span></span> | <span data-ttu-id="61083-128">facoltativo.</span><span class="sxs-lookup"><span data-stu-id="61083-128">Optional.</span></span> <span data-ttu-id="61083-129">Imposta un flag booleano che indica se l'utilizzo del file hash della parte (PHF) è obbligatorio.</span><span class="sxs-lookup"><span data-stu-id="61083-129">Sets a boolean flag indicating whether usage of the piece hash file (PHF) is mandatory.</span></span> <span data-ttu-id="61083-130">Se VARIANT_TRUE, il download verrà interrotto dopo che il controllo di integrità non è riuscito.</span><span class="sxs-lookup"><span data-stu-id="61083-130">If VARIANT_TRUE, the download will be aborted once the integrity check is failed.</span></span> <span data-ttu-id="61083-131">Il tipo VARIANT è VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="61083-131">VARIANT type is VT_BOOL.</span></span> |
| <span data-ttu-id="61083-132">DODownloadPropertyEx_TotalSizeBytes</span><span class="sxs-lookup"><span data-stu-id="61083-132">DODownloadPropertyEx_TotalSizeBytes</span></span> | <span data-ttu-id="61083-133">Riservato.</span><span class="sxs-lookup"><span data-stu-id="61083-133">Reserved.</span></span> <span data-ttu-id="61083-134">Non usare.</span><span class="sxs-lookup"><span data-stu-id="61083-134">Do not use.</span></span> |
| <span data-ttu-id="61083-135">DODownloadPropertyEx_TempLocalFileUsage</span><span class="sxs-lookup"><span data-stu-id="61083-135">DODownloadPropertyEx_TempLocalFileUsage</span></span> | <span data-ttu-id="61083-136">Riservato.</span><span class="sxs-lookup"><span data-stu-id="61083-136">Reserved.</span></span> <span data-ttu-id="61083-137">Non usare.</span><span class="sxs-lookup"><span data-stu-id="61083-137">Do not use.</span></span> |

## <a name="requirements"></a><span data-ttu-id="61083-138">Requisiti</span><span class="sxs-lookup"><span data-stu-id="61083-138">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="61083-139">**Client minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="61083-139">**Minimum supported client**</span></span> | <span data-ttu-id="61083-140">Solo applicazioni Win32 Windows 10 versione 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="61083-140">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="61083-141">**Server minimo supportato**</span><span class="sxs-lookup"><span data-stu-id="61083-141">**Minimum supported server**</span></span> | <span data-ttu-id="61083-142">Windows Server, \[ solo applicazioni Win32 versione 1809\]</span><span class="sxs-lookup"><span data-stu-id="61083-142">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="61083-143">**Intestazione**</span><span class="sxs-lookup"><span data-stu-id="61083-143">**Header**</span></span> | <span data-ttu-id="61083-144">DODownloadInternal. h</span><span class="sxs-lookup"><span data-stu-id="61083-144">DODownloadInternal.h</span></span> |
