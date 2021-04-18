---
title: Metodo IMsRdpDriveCollection RescanDrives
description: Aggiorna l'elenco di oggetti nella raccolta. | Metodo IMsRdpDriveCollection RescanDrives
ms.assetid: 5997b76c-d130-4375-b6ff-5ea871f059cc
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto del metodo RescanDrives
- Metodo RescanDrives Servizi Desktop remoto, interfaccia IMsRdpDriveCollection
- Interfaccia IMsRdpDriveCollection Servizi Desktop remoto, metodo RescanDrives
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.RescanDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7488187e44caeaedb7c73b01ff8a3711e20dcdd1
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/09/2021
ms.locfileid: "106321237"
---
# <a name="imsrdpdrivecollectionrescandrives-method"></a><span data-ttu-id="ab59a-107">Metodo IMsRdpDriveCollection:: RescanDrives</span><span class="sxs-lookup"><span data-stu-id="ab59a-107">IMsRdpDriveCollection::RescanDrives method</span></span>

<span data-ttu-id="ab59a-108">Aggiorna l'elenco di oggetti nella raccolta.</span><span class="sxs-lookup"><span data-stu-id="ab59a-108">Refreshes the list of objects in the collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab59a-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ab59a-109">Syntax</span></span>


```C++
HRESULT RescanDrives(
  [in] VARIANT_BOOL vboolDynRedir
);
```



## <a name="parameters"></a><span data-ttu-id="ab59a-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="ab59a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab59a-111">*vboolDynRedir* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ab59a-111">*vboolDynRedir* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab59a-112">Stato di reindirizzamento predefinito che verrà applicato alle unità o ai dispositivi appena individuati.</span><span class="sxs-lookup"><span data-stu-id="ab59a-112">The default redirection state that will be applied to any newly discovered devices or drives.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab59a-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ab59a-113">Return value</span></span>

<span data-ttu-id="ab59a-114">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="ab59a-114">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="ab59a-115">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="ab59a-115">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab59a-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ab59a-116">Requirements</span></span>



| <span data-ttu-id="ab59a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab59a-117">Requirement</span></span> | <span data-ttu-id="ab59a-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ab59a-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab59a-119">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab59a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ab59a-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ab59a-120">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="ab59a-121">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="ab59a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ab59a-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ab59a-122">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="ab59a-123">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="ab59a-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="ab59a-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab59a-124"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ab59a-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ab59a-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab59a-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab59a-126"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="ab59a-127">IID</span><span class="sxs-lookup"><span data-stu-id="ab59a-127">IID</span></span><br/>                      | <span data-ttu-id="ab59a-128">IID \_ IMsRdpDriveCollection è definito come 7ff17599-da2c-4677-Ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="ab59a-128">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ab59a-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ab59a-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab59a-130">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="ab59a-130">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





