---
description: Crea un enumeratore di informazioni sulle proprietà per ogni dispositivo Windows Image Acquisition (WIA) 2,0 disponibile.
ms.assetid: e37b73d5-5192-46e4-bb1c-bd1ef41f1d6c
title: 'Metodo IWiaDevMgr2:: EnumDeviceInfo (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.EnumDeviceInfo
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bd9e9281b625f4cec5377537d82a304045b95a3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752839"
---
# <a name="iwiadevmgr2enumdeviceinfo-method"></a><span data-ttu-id="6c218-103">Metodo IWiaDevMgr2:: EnumDeviceInfo</span><span class="sxs-lookup"><span data-stu-id="6c218-103">IWiaDevMgr2::EnumDeviceInfo method</span></span>

<span data-ttu-id="6c218-104">Crea un enumeratore di informazioni sulle proprietà per ogni dispositivo Windows Image Acquisition (WIA) 2,0 disponibile.</span><span class="sxs-lookup"><span data-stu-id="6c218-104">Creates an enumerator of property information for each available Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c218-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6c218-105">Syntax</span></span>


```C++
HRESULT EnumDeviceInfo(
  [in]          LONG              lFlags,
  [out, retval] IEnumWIA_DEV_INFO **ppIEnum
);
```



## <a name="parameters"></a><span data-ttu-id="6c218-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6c218-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c218-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6c218-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c218-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="6c218-108">Type: **LONG**</span></span>

<span data-ttu-id="6c218-109">Specifica il tipo di dispositivi WIA 2,0 da enumerare.</span><span class="sxs-lookup"><span data-stu-id="6c218-109">Specifies the type of WIA 2.0 devices to enumerate.</span></span>

<dt>

<span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>

<span data-ttu-id="6c218-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**\_ \_ enumerazione locale WIA \_ DEVINFO**</span><span class="sxs-lookup"><span data-stu-id="6c218-110"><span id="WIA_DEVINFO_ENUM_LOCAL"></span><span id="wia_devinfo_enum_local"></span>**WIA\_DEVINFO\_ENUM\_LOCAL**</span></span>


</dt> <dd>

<span data-ttu-id="6c218-111">Vengono enumerati solo i dispositivi scanner attivi connessi localmente.</span><span class="sxs-lookup"><span data-stu-id="6c218-111">Only locally connected active scanner devices are enumerated.</span></span>

</dd> <dt>

<span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>

<span data-ttu-id="6c218-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA \_ DEVINFO \_ enum \_ All**</span><span class="sxs-lookup"><span data-stu-id="6c218-112"><span id="WIA_DEVINFO_ENUM_ALL"></span><span id="wia_devinfo_enum_all"></span>**WIA\_DEVINFO\_ENUM\_ALL**</span></span>


</dt> <dd>

<span data-ttu-id="6c218-113">Tutti i dispositivi vengono enumerati, sia localmente che remoti, inclusi i dispositivi inattivi (disconnessi) e i dispositivi solo STI legacy.</span><span class="sxs-lookup"><span data-stu-id="6c218-113">All devices are enumerated, both locally and remote, including inactive (disconnected) devices and legacy STI-only devices.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="6c218-114">*ppIEnum* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="6c218-114">*ppIEnum* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="6c218-115">Tipo: **[ **IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span><span class="sxs-lookup"><span data-stu-id="6c218-115">Type: **[**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info)\*\***</span></span>

<span data-ttu-id="6c218-116">Riceve l'indirizzo di un puntatore all'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="6c218-116">Receives the address of a pointer to the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c218-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6c218-117">Return value</span></span>

<span data-ttu-id="6c218-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="6c218-118">Type: **HRESULT**</span></span>

<span data-ttu-id="6c218-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6c218-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="6c218-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6c218-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c218-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="6c218-121">Remarks</span></span>

<span data-ttu-id="6c218-122">Il metodo **IWiaDevMgr2:: EnumDeviceInfo** crea un oggetto enumeratore che supporta l'interfaccia [**IEnumWIA \_ dev \_ info**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) .</span><span class="sxs-lookup"><span data-stu-id="6c218-122">The **IWiaDevMgr2::EnumDeviceInfo** method creates an enumerator object that supports the [**IEnumWIA\_DEV\_INFO**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_info) interface.</span></span> <span data-ttu-id="6c218-123">Il metodo archivia un puntatore all'interfaccia **IEnumWIA \_ dev \_ info** nel parametro *ppIEnum*.</span><span class="sxs-lookup"><span data-stu-id="6c218-123">The method stores a pointer to the **IEnumWIA\_DEV\_INFO** interface in the parameter *ppIEnum*.</span></span> <span data-ttu-id="6c218-124">Le applicazioni possono usare il puntatore all'interfaccia **IEnumWIA \_ dev \_ info** per enumerare le proprietà di ogni dispositivo WIA 2,0 collegato al computer dell'utente.</span><span class="sxs-lookup"><span data-stu-id="6c218-124">Applications can use the **IEnumWIA\_DEV\_INFO** interface pointer to enumerate the properties of each WIA 2.0 device attached to the user's computer.</span></span>

<span data-ttu-id="6c218-125">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori di interfaccia ricevuti tramite il parametro *ppIEnum* .</span><span class="sxs-lookup"><span data-stu-id="6c218-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIEnum* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c218-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6c218-126">Requirements</span></span>



| <span data-ttu-id="6c218-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6c218-127">Requirement</span></span> | <span data-ttu-id="6c218-128">Valore</span><span class="sxs-lookup"><span data-stu-id="6c218-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c218-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c218-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6c218-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6c218-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6c218-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="6c218-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6c218-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6c218-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6c218-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6c218-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c218-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c218-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c218-135">IDL</span><span class="sxs-lookup"><span data-stu-id="6c218-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="6c218-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="6c218-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
