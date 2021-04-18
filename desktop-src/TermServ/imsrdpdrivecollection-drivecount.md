---
title: Proprietà DriveCount di IMsRdpDriveCollection
description: Recupera il numero di oggetti nella raccolta. | Proprietà DriveCount di IMsRdpDriveCollection
ms.assetid: 33b39657-2cc1-4f1e-b23a-809a9737ed8d
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DriveCount
- Servizi Desktop remoto proprietà DriveCount, interfaccia IMsRdpDriveCollection
- Interfaccia IMsRdpDriveCollection Servizi Desktop remoto, proprietà DriveCount
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveCount
- IMsRdpDriveCollection.get_DriveCount
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af724344cd7d88676483c13d1a6a8cfeb8548294
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321925"
---
# <a name="imsrdpdrivecollectiondrivecount-property"></a><span data-ttu-id="d9f69-107">IMsRdpDriveCollection::D Proprietà riveCount</span><span class="sxs-lookup"><span data-stu-id="d9f69-107">IMsRdpDriveCollection::DriveCount property</span></span>

<span data-ttu-id="d9f69-108">Recupera il numero di oggetti nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="d9f69-108">Retrieves the count of objects in the collection.</span></span>

<span data-ttu-id="d9f69-109">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="d9f69-109">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d9f69-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d9f69-110">Syntax</span></span>


```C++
HRESULT get_DriveCount(
  [out] ULONG *pDriveCount
);
```



## <a name="property-value"></a><span data-ttu-id="d9f69-111">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="d9f69-111">Property value</span></span>

<span data-ttu-id="d9f69-112">Conteggio oggetti.</span><span class="sxs-lookup"><span data-stu-id="d9f69-112">The object count.</span></span>

## <a name="error-codes"></a><span data-ttu-id="d9f69-113">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="d9f69-113">Error codes</span></span>

<span data-ttu-id="d9f69-114">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="d9f69-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="d9f69-115">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="d9f69-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9f69-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d9f69-116">Requirements</span></span>



| <span data-ttu-id="d9f69-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="d9f69-117">Requirement</span></span> | <span data-ttu-id="d9f69-118">Valore</span><span class="sxs-lookup"><span data-stu-id="d9f69-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d9f69-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9f69-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d9f69-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9f69-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="d9f69-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="d9f69-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d9f69-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9f69-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d9f69-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="d9f69-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="d9f69-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9f69-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="d9f69-125">DLL</span><span class="sxs-lookup"><span data-stu-id="d9f69-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9f69-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9f69-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="d9f69-127">IID</span><span class="sxs-lookup"><span data-stu-id="d9f69-127">IID</span></span><br/>                      | <span data-ttu-id="d9f69-128">IID \_ IMsRdpDriveCollection è definito come 7ff17599-da2c-4677-Ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="d9f69-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d9f69-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d9f69-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9f69-130">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="d9f69-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





