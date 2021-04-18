---
description: Imposta il profilo di analisi specificato come profilo predefinito.
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'Metodo IScanProfileMgr:: IsDefault (Scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312429"
---
# <a name="iscanprofilemgrsetdefault-method"></a><span data-ttu-id="f8446-103">Metodo IScanProfileMgr:: sedefault</span><span class="sxs-lookup"><span data-stu-id="f8446-103">IScanProfileMgr::SetDefault method</span></span>

<span data-ttu-id="f8446-104">Imposta il profilo di analisi specificato come profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="f8446-104">Sets the specified scan profile as the default profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8446-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="f8446-105">Syntax</span></span>


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="f8446-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="f8446-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8446-107">*pScanProfile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f8446-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8446-108">Tipo: \**[**IScanProfile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="f8446-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="f8446-109">Puntatore al profilo.</span><span class="sxs-lookup"><span data-stu-id="f8446-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8446-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="f8446-110">Return value</span></span>

<span data-ttu-id="f8446-111">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f8446-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f8446-112">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="f8446-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f8446-113">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="f8446-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f8446-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="f8446-114">Remarks</span></span>

<span data-ttu-id="f8446-115">Usare il metodo **IScanProfileMgr:: sedefault** per aggiungere un `<Default>` elemento al profilo o rimuovere tale elemento dal profilo predefinito precedente del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f8446-115">Use the **IScanProfileMgr::SetDefault** method to add a `<Default>` element to the profile or to remove that element from the device's previous default profile.</span></span>

<span data-ttu-id="f8446-116">Usare il metodo [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) per modificare il profilo predefinito.</span><span class="sxs-lookup"><span data-stu-id="f8446-116">Use the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method to change the default profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8446-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="f8446-117">Requirements</span></span>



| <span data-ttu-id="f8446-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="f8446-118">Requirement</span></span> | <span data-ttu-id="f8446-119">Valore</span><span class="sxs-lookup"><span data-stu-id="f8446-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f8446-120">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8446-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f8446-121">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f8446-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f8446-122">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="f8446-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f8446-123">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f8446-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f8446-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="f8446-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="f8446-125"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="f8446-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="f8446-126">IDL</span><span class="sxs-lookup"><span data-stu-id="f8446-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f8446-127"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="f8446-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f8446-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="f8446-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8446-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="f8446-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="f8446-130">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="f8446-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




