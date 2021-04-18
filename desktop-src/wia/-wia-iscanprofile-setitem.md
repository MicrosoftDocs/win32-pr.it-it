---
description: Imposta il GUID della categoria dell'elemento Windows Image Acquisition (WIA) 2,0 a cui è associato il profilo.
ms.assetid: e359abcb-b5d5-45a4-b650-2b278ba1ff6a
title: 'Metodo IScanProfile:: SetItem (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.SetItem
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: d4b20aae0740656b46dd26824947fc27513afcac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308259"
---
# <a name="iscanprofilesetitem-method"></a><span data-ttu-id="04d51-103">Metodo IScanProfile:: SetItem</span><span class="sxs-lookup"><span data-stu-id="04d51-103">IScanProfile::SetItem method</span></span>

<span data-ttu-id="04d51-104">Imposta il GUID della categoria dell'elemento Windows Image Acquisition (WIA) 2,0 a cui è associato il profilo.</span><span class="sxs-lookup"><span data-stu-id="04d51-104">Sets the GUID of the category of Windows Image Acquisition (WIA) 2.0 item that the profile is associated with.</span></span>

## <a name="syntax"></a><span data-ttu-id="04d51-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="04d51-105">Syntax</span></span>


```C++
HRESULT SetItem(
  [in] GUID guidCategory
);
```



## <a name="parameters"></a><span data-ttu-id="04d51-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="04d51-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="04d51-107">*guidCategory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="04d51-107">*guidCategory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="04d51-108">Tipo: **GUID**</span><span class="sxs-lookup"><span data-stu-id="04d51-108">Type: **GUID**</span></span>

<span data-ttu-id="04d51-109">GUID della categoria dell'elemento WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="04d51-109">The GUID of the category of the WIA 2.0 item.</span></span> <span data-ttu-id="04d51-110">Deve corrispondere a una delle costanti di \_ categoria degli elementi dell'IPA WIA \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="04d51-110">This must be one of the WIA\_IPA\_ITEM\_CATEGORY constants.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="04d51-111">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="04d51-111">Return value</span></span>

<span data-ttu-id="04d51-112">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="04d51-112">Type: **HRESULT**</span></span>

<span data-ttu-id="04d51-113">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="04d51-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="04d51-114">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="04d51-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="04d51-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="04d51-115">Remarks</span></span>

<span data-ttu-id="04d51-116">Gli utenti possono modificare la categoria con il metodo [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) .</span><span class="sxs-lookup"><span data-stu-id="04d51-116">Users can change the category with the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method.</span></span>

<span data-ttu-id="04d51-117">Le modifiche apportate a un profilo non vengono salvate su disco fino a quando l'applicazione non chiama il metodo [**IScanProfile:: Save**](-wia-iscanprofile-save.md) .</span><span class="sxs-lookup"><span data-stu-id="04d51-117">Changes to a profile are not saved to disk until the application calls the [**IScanProfile::Save**](-wia-iscanprofile-save.md) method.</span></span>

<span data-ttu-id="04d51-118">Se due applicazioni creano oggetti del profilo di analisi dallo stesso file XML e ogni applicazione scrive le modifiche nel relativo oggetto, solo le modifiche apportate dall'applicazione che chiama [**IScanProfile:: Save**](-wia-iscanprofile-save.md) Last vengono salvate su disco.</span><span class="sxs-lookup"><span data-stu-id="04d51-118">If two applications create scan profile objects from the same XML file, and each application writes changes to its object, only the changes made by the application that calls [**IScanProfile::Save**](-wia-iscanprofile-save.md) last are saved to disk.</span></span>

## <a name="requirements"></a><span data-ttu-id="04d51-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="04d51-119">Requirements</span></span>



| <span data-ttu-id="04d51-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="04d51-120">Requirement</span></span> | <span data-ttu-id="04d51-121">Valore</span><span class="sxs-lookup"><span data-stu-id="04d51-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="04d51-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04d51-122">Minimum supported client</span></span><br/> | <span data-ttu-id="04d51-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="04d51-123">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="04d51-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="04d51-124">Minimum supported server</span></span><br/> | <span data-ttu-id="04d51-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="04d51-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="04d51-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="04d51-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="04d51-127"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="04d51-127"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="04d51-128">IDL</span><span class="sxs-lookup"><span data-stu-id="04d51-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="04d51-129"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="04d51-129"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="04d51-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="04d51-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="04d51-131">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="04d51-131">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="04d51-132">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="04d51-132">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




