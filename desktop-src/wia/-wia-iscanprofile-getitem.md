---
description: Ottiene il GUID della categoria dell'elemento Windows Image Acquisition (WIA) 2,0 a cui è associato il profilo.
ms.assetid: 2c816789-ad66-4b06-9160-7a86289ff373
title: 'Metodo IScanProfile:: GetItem (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 888a3bb5bcb6e6c4fc2fefff2d976eb7fc1c7f82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308264"
---
# <a name="iscanprofilegetitem-method"></a><span data-ttu-id="1e880-103">Metodo IScanProfile:: GetItem</span><span class="sxs-lookup"><span data-stu-id="1e880-103">IScanProfile::GetItem method</span></span>

<span data-ttu-id="1e880-104">Ottiene il GUID della categoria dell'elemento Windows Image Acquisition (WIA) 2,0 a cui è associato il profilo.</span><span class="sxs-lookup"><span data-stu-id="1e880-104">Gets the GUID of the category of the Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e880-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="1e880-105">Syntax</span></span>


```C++
HRESULT GetItem(
  [out] GUID *pguidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="1e880-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="1e880-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e880-107">*pguidCategory* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="1e880-107">*pguidCategory* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e880-108">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="1e880-108">Type: \**GUID\** _</span></span>

<span data-ttu-id="1e880-109">Puntatore al GUID della categoria dell'elemento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="1e880-109">A pointer to the GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="1e880-110">Si tratta sempre di una delle \_ costanti di categoria degli elementi dell'IPA WIA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="1e880-110">This is always one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e880-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="1e880-111">Return value</span></span>

<span data-ttu-id="1e880-112">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="1e880-112">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="1e880-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1e880-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e880-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e880-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1e880-115">Requisiti</span><span class="sxs-lookup"><span data-stu-id="1e880-115">Requirements</span></span>



| <span data-ttu-id="1e880-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e880-116">Requirement</span></span> | <span data-ttu-id="1e880-117">Valore</span><span class="sxs-lookup"><span data-stu-id="1e880-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e880-118">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e880-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1e880-119">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1e880-119">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="1e880-120">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="1e880-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1e880-121">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1e880-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="1e880-122">Intestazione</span><span class="sxs-lookup"><span data-stu-id="1e880-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e880-123"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e880-123"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="1e880-124">IDL</span><span class="sxs-lookup"><span data-stu-id="1e880-124">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e880-125"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e880-125"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e880-126">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="1e880-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e880-127">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="1e880-127">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="1e880-128">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="1e880-128">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




