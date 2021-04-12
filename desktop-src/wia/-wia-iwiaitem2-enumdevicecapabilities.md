---
description: Crea un enumeratore usato per verificare i comandi e gli eventi supportati da un dispositivo Windows Image Acquisition (WIA) 2,0.
ms.assetid: 9efb758d-a5d6-41c7-b318-2897274ccbc0
title: 'Metodo IWiaItem2:: EnumDeviceCapabilities (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.EnumDeviceCapabilities
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 3e771aa636b42d9cd7e4024a1684ebe3edf02eeb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526467"
---
# <a name="iwiaitem2enumdevicecapabilities-method"></a><span data-ttu-id="8e323-103">Metodo IWiaItem2:: EnumDeviceCapabilities</span><span class="sxs-lookup"><span data-stu-id="8e323-103">IWiaItem2::EnumDeviceCapabilities method</span></span>

<span data-ttu-id="8e323-104">Crea un enumeratore usato per verificare i comandi e gli eventi supportati da un dispositivo Windows Image Acquisition (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="8e323-104">Creates an enumerator that is used to ascertain the commands and events a Windows Image Acquisition (WIA) 2.0 device supports.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e323-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="8e323-105">Syntax</span></span>


```C++
HRESULT EnumDeviceCapabilities(
  [in]  LONG              lFlags,
  [out] IEnumWIA_DEV_CAPS **ppIEnumWIA_DEV_CAPS
);
```



## <a name="parameters"></a><span data-ttu-id="8e323-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="8e323-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8e323-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8e323-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8e323-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="8e323-108">Type: **LONG**</span></span>

<span data-ttu-id="8e323-109">Specifica un flag che seleziona il tipo di funzionalità da enumerare.</span><span class="sxs-lookup"><span data-stu-id="8e323-109">Specifies a flag that selects the type of capabilities to enumerate.</span></span> <span data-ttu-id="8e323-110">È uno dei valori seguenti.</span><span class="sxs-lookup"><span data-stu-id="8e323-110">It is one of the following values.</span></span>

<dt>

<span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>

<span data-ttu-id="8e323-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**\_comandi del dispositivo WIA \_**</span><span class="sxs-lookup"><span data-stu-id="8e323-111"><span id="WIA_DEVICE_COMMANDS"></span><span id="wia_device_commands"></span>**WIA\_DEVICE\_COMMANDS**</span></span>


</dt> <dd>

<span data-ttu-id="8e323-112">Enumera i comandi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e323-112">Enumerate device commands.</span></span>

</dd> <dt>

<span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>

<span data-ttu-id="8e323-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**\_eventi del dispositivo WIA \_**</span><span class="sxs-lookup"><span data-stu-id="8e323-113"><span id="WIA_DEVICE_EVENTS"></span><span id="wia_device_events"></span>**WIA\_DEVICE\_EVENTS**</span></span>


</dt> <dd>

<span data-ttu-id="8e323-114">Enumerare gli eventi del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e323-114">Enumerate device events.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8e323-115">*ppIEnumWIA \_ DEV \_ Caps* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="8e323-115">*ppIEnumWIA\_DEV\_CAPS* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8e323-116">Tipo: **[ **IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span><span class="sxs-lookup"><span data-stu-id="8e323-116">Type: **[**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps)\*\***</span></span>

<span data-ttu-id="8e323-117">Riceve un puntatore all'interfaccia [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) creata da questo metodo.</span><span class="sxs-lookup"><span data-stu-id="8e323-117">Receives a pointer to the [**IEnumWIA\_DEV\_CAPS**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) interface created by this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8e323-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="8e323-118">Return value</span></span>

<span data-ttu-id="8e323-119">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="8e323-119">Type: **HRESULT**</span></span>

<span data-ttu-id="8e323-120">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="8e323-120">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="8e323-121">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="8e323-121">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e323-122">Commenti</span><span class="sxs-lookup"><span data-stu-id="8e323-122">Remarks</span></span>

<span data-ttu-id="8e323-123">Questo metodo viene usato per creare un oggetto enumeratore per ottenere il set di comandi ed eventi supportati da un dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="8e323-123">This method is used to create an enumerator object to obtain the set of commands and events that a WIA 2.0 device supports.</span></span> <span data-ttu-id="8e323-124">Il parametro *è* viene usato per specificare i tipi di funzionalità del dispositivo da enumerare.</span><span class="sxs-lookup"><span data-stu-id="8e323-124">The *lFlags* parameter is used to specify which kinds of device capabilities to enumerate.</span></span> <span data-ttu-id="8e323-125">Il metodo **IWiaItem2:: EnumDeviceCapabilities** archivia l'indirizzo dell'interfaccia dell'oggetto enumeratore nel parametro *ppIEnumWIA \_ dev \_ Caps* .</span><span class="sxs-lookup"><span data-stu-id="8e323-125">The **IWiaItem2::EnumDeviceCapabilities** method stores the address of the interface of the enumerator object in the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

<span data-ttu-id="8e323-126">Questo metodo può essere chiamato solo sull'elemento radice degli oggetti [**IWiaItem2**](-wia-iwiaitem2.md) di un albero del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="8e323-126">This method can only be called on the root item of [**IWiaItem2**](-wia-iwiaitem2.md) objects of a device tree.</span></span>

<span data-ttu-id="8e323-127">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIEnumWIA \_ dev \_ Caps* .</span><span class="sxs-lookup"><span data-stu-id="8e323-127">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnumWIA\_DEV\_CAPS* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e323-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="8e323-128">Requirements</span></span>



| <span data-ttu-id="8e323-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="8e323-129">Requirement</span></span> | <span data-ttu-id="8e323-130">Valore</span><span class="sxs-lookup"><span data-stu-id="8e323-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="8e323-131">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e323-131">Minimum supported client</span></span><br/> | <span data-ttu-id="8e323-132">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8e323-132">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="8e323-133">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="8e323-133">Minimum supported server</span></span><br/> | <span data-ttu-id="8e323-134">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8e323-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="8e323-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="8e323-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e323-136"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e323-136"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="8e323-137">IDL</span><span class="sxs-lookup"><span data-stu-id="8e323-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="8e323-138"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="8e323-138"><dt>Wia.idl</dt></span></span> </dl> |



 

 
