---
description: Salva le modifiche apportate a un profilo su disco.
ms.assetid: e844bd4c-93c3-44a3-b7d5-0beb71c9fa17
title: 'Metodo IScanProfile:: Save (scanprofile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.Save
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 6d4787380344a7bf8adb70f4cb5a3eaacdea403a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527085"
---
# <a name="iscanprofilesave-method"></a><span data-ttu-id="a610a-103">Metodo IScanProfile:: Save</span><span class="sxs-lookup"><span data-stu-id="a610a-103">IScanProfile::Save method</span></span>

<span data-ttu-id="a610a-104">Salva le modifiche apportate a un profilo su disco.</span><span class="sxs-lookup"><span data-stu-id="a610a-104">Saves changes to a profile to disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="a610a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a610a-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="a610a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a610a-106">Parameters</span></span>

<span data-ttu-id="a610a-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="a610a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a610a-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a610a-108">Return value</span></span>

<span data-ttu-id="a610a-109">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="a610a-109">Type: **HRESULT**</span></span>

<span data-ttu-id="a610a-110">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="a610a-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="a610a-111">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a610a-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="a610a-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="a610a-112">Remarks</span></span>

<span data-ttu-id="a610a-113">Un profilo di analisi salvato è un file XML archiviato in% USERPROFILE% \\ dati applicazione \\ Microsoft \\ Document Center \\ UserScanProfiles.</span><span class="sxs-lookup"><span data-stu-id="a610a-113">A saved scan profile is an XML file stored at %USERPROFILE%\\Application Data\\Microsoft\\Document Center\\UserScanProfiles.</span></span>

<span data-ttu-id="a610a-114">Se più di un processo scrive nell'oggetto [**IScanProfile**](-wia-iscanprofile.md) , quello che chiama **IScanProfile:: Save** Last è l'unico processo le cui modifiche vengono salvate.</span><span class="sxs-lookup"><span data-stu-id="a610a-114">If more than one process writes to the [**IScanProfile**](-wia-iscanprofile.md) object, the one that calls **IScanProfile::Save** last is the only process whose changes are saved.</span></span>

<span data-ttu-id="a610a-115">Il metodo **IScanProfile:: Save** convalida il profilo prima del salvataggio.</span><span class="sxs-lookup"><span data-stu-id="a610a-115">The **IScanProfile::Save** method validates the profile before saving.</span></span> <span data-ttu-id="a610a-116">Il profilo è sempre considerato valido a meno che la categoria dell'elemento Windows Image Acquisition (WIA) 2,0 associato al profilo sia WIA Category piano \_ \_ o WIA \_ Category \_ feeder.</span><span class="sxs-lookup"><span data-stu-id="a610a-116">The profile is always considered valid unless the category of the Windows Image Acquisition (WIA) 2.0 item associated with the profile is either WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER.</span></span> <span data-ttu-id="a610a-117">Se la categoria è la categoria WIA piano \_ \_ o \_ il \_ feeder di categoria WIA, le proprietà seguenti devono essere valide per l'elemento, se le proprietà sono contenute nel profilo:</span><span class="sxs-lookup"><span data-stu-id="a610a-117">If the category is WIA\_CATEGORY\_FLATBED or WIA\_CATEGORY\_FEEDER, the following properties must be valid for the item, if the properties are contained in the profile:</span></span>

<span data-ttu-id="a610a-118">\_luminosità IP \_ WIA</span><span class="sxs-lookup"><span data-stu-id="a610a-118">WIA\_IPS\_BRIGHTNESS</span></span>

<span data-ttu-id="a610a-119">\_contrasto indirizzi IP WIA \_</span><span class="sxs-lookup"><span data-stu-id="a610a-119">WIA\_IPS\_CONTRAST</span></span>

<span data-ttu-id="a610a-120">tipo di dati \_ IPA WIA \_</span><span class="sxs-lookup"><span data-stu-id="a610a-120">WIA\_IPA\_DATATYPE</span></span>

<span data-ttu-id="a610a-121">\_indirizzi IP WIA \_ XRES</span><span class="sxs-lookup"><span data-stu-id="a610a-121">WIA\_IPS\_XRES</span></span>

<span data-ttu-id="a610a-122">\_formato ipa \_ WIA</span><span class="sxs-lookup"><span data-stu-id="a610a-122">WIA\_IPA\_FORMAT</span></span>

<span data-ttu-id="a610a-123">Se, inoltre, la categoria è il \_ feeder di categoria WIA \_ , la \_ proprietà delle dimensioni di pagina degli indirizzi IP WIA \_ \_ deve essere valida, se presente nel profilo.</span><span class="sxs-lookup"><span data-stu-id="a610a-123">In addition, if the category is WIA\_CATEGORY\_FEEDER, the WIA\_IPS\_PAGE\_SIZE property must be valid, if it is present in the profile.</span></span> <span data-ttu-id="a610a-124">Per ulteriori informazioni su queste proprietà, vedere la pagina relativa alle [**costanti della proprietà Item di scanner WIA**](-wia-wiaitempropscanneritem.md).</span><span class="sxs-lookup"><span data-stu-id="a610a-124">For more information about these properties, see [**Scanner WIA Item Property Constants**](-wia-wiaitempropscanneritem.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a610a-125">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a610a-125">Requirements</span></span>



| <span data-ttu-id="a610a-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a610a-126">Requirement</span></span> | <span data-ttu-id="a610a-127">Valore</span><span class="sxs-lookup"><span data-stu-id="a610a-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="a610a-128">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a610a-128">Minimum supported client</span></span><br/> | <span data-ttu-id="a610a-129">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a610a-129">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a610a-130">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="a610a-130">Minimum supported server</span></span><br/> | <span data-ttu-id="a610a-131">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a610a-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a610a-132">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a610a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="a610a-133"><dt>Scanprofile. h</dt></span><span class="sxs-lookup"><span data-stu-id="a610a-133"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="a610a-134">IDL</span><span class="sxs-lookup"><span data-stu-id="a610a-134">IDL</span></span><br/>                      | <dl> <span data-ttu-id="a610a-135"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="a610a-135"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a610a-136">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a610a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a610a-137">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="a610a-137">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="a610a-138">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="a610a-138">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




