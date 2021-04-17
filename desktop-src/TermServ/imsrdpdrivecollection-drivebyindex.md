---
title: Proprietà DriveByIndex di IMsRdpDriveCollection
description: Recupera l'unità in corrispondenza dell'indice specificato.
ms.assetid: 28bb2a44-00ac-4892-881d-fdd3fe6adb6b
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto proprietà DriveByIndex
- Servizi Desktop remoto proprietà DriveByIndex, interfaccia IMsRdpDriveCollection
- Interfaccia IMsRdpDriveCollection Servizi Desktop remoto, proprietà DriveByIndex
topic_type:
- apiref
api_name:
- IMsRdpDriveCollection.DriveByIndex
- IMsRdpDriveCollection.get_DriveByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2789656b328f9615787ff2cd50a1b69c712a8138
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "104400786"
---
# <a name="imsrdpdrivecollectiondrivebyindex-property"></a><span data-ttu-id="184a0-106">IMsRdpDriveCollection::D Proprietà riveByIndex</span><span class="sxs-lookup"><span data-stu-id="184a0-106">IMsRdpDriveCollection::DriveByIndex property</span></span>

<span data-ttu-id="184a0-107">Recupera l'unità in corrispondenza dell'indice specificato.</span><span class="sxs-lookup"><span data-stu-id="184a0-107">Retrieves the drive at the specified index.</span></span>

<span data-ttu-id="184a0-108">Questa proprietà è di sola lettura.</span><span class="sxs-lookup"><span data-stu-id="184a0-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="184a0-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="184a0-109">Syntax</span></span>


```C++
HRESULT get_DriveByIndex(
  [in]          ULONG index,
  [out, retval] IMsRdpDrive **ppDevice
);
```



## <a name="property-value"></a><span data-ttu-id="184a0-110">Valore proprietà</span><span class="sxs-lookup"><span data-stu-id="184a0-110">Property value</span></span>

<span data-ttu-id="184a0-111">Puntatore di interfaccia [**IMsRdpDrive**](imsrdpdrive.md) .</span><span class="sxs-lookup"><span data-stu-id="184a0-111">An [**IMsRdpDrive**](imsrdpdrive.md) interface pointer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="184a0-112">Codici di errore</span><span class="sxs-lookup"><span data-stu-id="184a0-112">Error codes</span></span>

<span data-ttu-id="184a0-113">Se il metodo ha esito positivo, viene restituito **S \_ OK** .</span><span class="sxs-lookup"><span data-stu-id="184a0-113">If the method succeeds, **S\_OK** is returned.</span></span> <span data-ttu-id="184a0-114">Qualsiasi altro valore **HRESULT** indica che la chiamata non è riuscita.</span><span class="sxs-lookup"><span data-stu-id="184a0-114">Any other **HRESULT** value indicates that the call failed.</span></span>

## <a name="requirements"></a><span data-ttu-id="184a0-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="184a0-115">Requirements</span></span>



| <span data-ttu-id="184a0-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="184a0-116">Requirement</span></span> | <span data-ttu-id="184a0-117">Valore</span><span class="sxs-lookup"><span data-stu-id="184a0-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="184a0-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="184a0-118">Minimum supported client</span></span><br/> | <span data-ttu-id="184a0-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="184a0-119">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="184a0-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="184a0-120">Minimum supported server</span></span><br/> | <span data-ttu-id="184a0-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="184a0-121">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="184a0-122">Libreria dei tipi</span><span class="sxs-lookup"><span data-stu-id="184a0-122">Type library</span></span><br/>             | <dl> <span data-ttu-id="184a0-123"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="184a0-123"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="184a0-124">DLL</span><span class="sxs-lookup"><span data-stu-id="184a0-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="184a0-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="184a0-125"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="184a0-126">IID</span><span class="sxs-lookup"><span data-stu-id="184a0-126">IID</span></span><br/>                      | <span data-ttu-id="184a0-127">IID \_ IMsRdpDriveCollection è definito come 7ff17599-da2c-4677-Ad35-f60c04fe1585</span><span class="sxs-lookup"><span data-stu-id="184a0-127">IID\_IMsRdpDriveCollection is defined as 7ff17599-da2c-4677-ad35-f60c04fe1585</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="184a0-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="184a0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="184a0-129">**IMsRdpDriveCollection**</span><span class="sxs-lookup"><span data-stu-id="184a0-129">**IMsRdpDriveCollection**</span></span>](imsrdpdrivecollection.md)
</dt> </dl>

 

 





