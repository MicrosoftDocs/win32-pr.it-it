---
description: Identifica la combinazione di dispositivi audio che l'applicazione sta attualmente usando con il DSP di acquisizione voce.
ms.assetid: f87bef33-9a48-4568-b554-7eec34f0bd55
title: Proprietà MFPKEY_WMAAECMA_DEVICEPAIR_GUID (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a586d7d31f29b20eb7ca39320d5fa57b9943715a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130546"
---
# <a name="mfpkey_wmaaecma_devicepair_guid-property"></a><span data-ttu-id="5bedc-103">\_ \_ Proprietà GUID MFPKEY WMAAECMA DEVICEPAIR \_</span><span class="sxs-lookup"><span data-stu-id="5bedc-103">MFPKEY\_WMAAECMA\_DEVICEPAIR\_GUID Property</span></span>

<span data-ttu-id="5bedc-104">Identifica la combinazione di dispositivi audio che l'applicazione sta attualmente usando con il DSP di acquisizione voce.</span><span class="sxs-lookup"><span data-stu-id="5bedc-104">Identifies the combination of audio devices that the application is currently using with the Voice Capture DSP.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="5bedc-105">Costante per IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="5bedc-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="5bedc-106">Disponibile solo tramite [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span><span class="sxs-lookup"><span data-stu-id="5bedc-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="5bedc-107">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="5bedc-107">Data Type</span></span>

<span data-ttu-id="5bedc-108">\_CLSID VT</span><span class="sxs-lookup"><span data-stu-id="5bedc-108">VT\_CLSID</span></span>

## <a name="applies-to"></a><span data-ttu-id="5bedc-109">Si applica a</span><span class="sxs-lookup"><span data-stu-id="5bedc-109">Applies To</span></span>

-   [<span data-ttu-id="5bedc-110">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="5bedc-110">Voice Capture DSP</span></span>](voicecapturedmo.md)

## <a name="remarks"></a><span data-ttu-id="5bedc-111">Commenti</span><span class="sxs-lookup"><span data-stu-id="5bedc-111">Remarks</span></span>

<span data-ttu-id="5bedc-112">Impostare questa proprietà se si utilizza il DSP in modalità filtro e il valore della proprietà [MFPKEY \_ WMAAECMA \_ Retrieve \_ TS \_ stats](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) è Variant \_ true.</span><span class="sxs-lookup"><span data-stu-id="5bedc-112">Set this property if you are using the DSP in filter mode and the value of the [MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE.</span></span>

<span data-ttu-id="5bedc-113">Quando la proprietà [**MFPKEY \_ WMAAECMA \_ Retrieve \_ TS \_ stats**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) è la variante \_ true, il DSP raccoglie le statistiche relative ai timestamp dai dispositivi audio e archivia tali informazioni nel registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="5bedc-113">When the [**MFPKEY\_WMAAECMA\_RETRIEVE\_TS\_STATS**](mfpkey-wmaaecma-retrieve-ts-statsproperty.md) property is VARIANT\_TRUE, the DSP collects statistics about the time stamps from the audio devices and stores this information in the registry.</span></span> <span data-ttu-id="5bedc-114">Queste statistiche possono cambiare per ogni combinazione di dispositivo di acquisizione audio e dispositivo di rendering audio.</span><span class="sxs-lookup"><span data-stu-id="5bedc-114">These statistics can change for each combination of audio capture device and audio rendering device.</span></span> <span data-ttu-id="5bedc-115">Pertanto, l'applicazione deve assegnare un GUID per identificare la combinazione specifica di dispositivi in uso.</span><span class="sxs-lookup"><span data-stu-id="5bedc-115">Therefore, the application must assign a GUID to identify the particular combination of devices in use.</span></span> <span data-ttu-id="5bedc-116">L'applicazione deve tenere traccia di questo GUID, in modo che possa assegnare lo stesso GUID ogni volta che usa la stessa coppia di dispositivi audio.</span><span class="sxs-lookup"><span data-stu-id="5bedc-116">The application should keep track of this GUID, so that it can assign the same GUID whenever it uses the same pair of audio devices.</span></span>

<span data-ttu-id="5bedc-117">Se si usa il DSP in modalità origine, non è necessario impostare questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="5bedc-117">If you are using the DSP in source mode, you do not need to set this property.</span></span> <span data-ttu-id="5bedc-118">Il DSP genera automaticamente un GUID basato sul valore della proprietà [MFPKEY \_ WMAAECMA \_ Device \_ indexes](mfpkey-wmaaecma-device-indexesproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="5bedc-118">The DSP automatically generates a GUID based on the value of the [MFPKEY\_WMAAECMA\_DEVICE\_INDEXES](mfpkey-wmaaecma-device-indexesproperty.md) property.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bedc-119">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5bedc-119">Requirements</span></span>



| <span data-ttu-id="5bedc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5bedc-120">Requirement</span></span> | <span data-ttu-id="5bedc-121">Valore</span><span class="sxs-lookup"><span data-stu-id="5bedc-121">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5bedc-122">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bedc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="5bedc-123">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5bedc-123">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="5bedc-124">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="5bedc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="5bedc-125">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5bedc-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5bedc-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5bedc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="5bedc-127"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="5bedc-127"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5bedc-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5bedc-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bedc-129">Proprietà Media Foundation</span><span class="sxs-lookup"><span data-stu-id="5bedc-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="5bedc-130">DSP di acquisizione vocale</span><span class="sxs-lookup"><span data-stu-id="5bedc-130">Voice Capture DSP</span></span>](voicecapturedmo.md)
</dt> </dl>

 

 
