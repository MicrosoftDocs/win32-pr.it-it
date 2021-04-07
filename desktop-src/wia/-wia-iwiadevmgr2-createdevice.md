---
description: Crea un albero gerarchico di oggetti IWiaItem2 per un dispositivo Windows Image Acquisition (WIA) 2,0.
ms.assetid: df7f3cc2-da0a-4238-b280-89c72107753c
title: 'Metodo IWiaDevMgr2:: CreateDevice (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.CreateDevice
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: a548a0ef43c2621b77c4ed10acde393af21d596d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881897"
---
# <a name="iwiadevmgr2createdevice-method"></a><span data-ttu-id="0715a-103">Metodo IWiaDevMgr2:: CreateDevice</span><span class="sxs-lookup"><span data-stu-id="0715a-103">IWiaDevMgr2::CreateDevice method</span></span>

<span data-ttu-id="0715a-104">Crea un albero gerarchico di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) per un dispositivo Windows Image Acquisition (WIA) 2,0.</span><span class="sxs-lookup"><span data-stu-id="0715a-104">Creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for a Windows Image Acquisition (WIA) 2.0 device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0715a-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="0715a-105">Syntax</span></span>


```C++
HRESULT CreateDevice(
  [in]  LONG      lFlags,
  [in]  BSTR      bstrDeviceID,
  [out] IWiaItem2 **ppWiaItem2Root
);
```



## <a name="parameters"></a><span data-ttu-id="0715a-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="0715a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0715a-107">*è* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0715a-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0715a-108">Tipo: **Long**</span><span class="sxs-lookup"><span data-stu-id="0715a-108">Type: **LONG**</span></span>

<span data-ttu-id="0715a-109">Attualmente non usato.</span><span class="sxs-lookup"><span data-stu-id="0715a-109">Currently unused.</span></span> <span data-ttu-id="0715a-110">Deve essere impostato su zero.</span><span class="sxs-lookup"><span data-stu-id="0715a-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="0715a-111">*bstrDeviceID* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0715a-111">*bstrDeviceID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0715a-112">Tipo: **BSTR**</span><span class="sxs-lookup"><span data-stu-id="0715a-112">Type: **BSTR**</span></span>

<span data-ttu-id="0715a-113">Specifica l'identificatore univoco del dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="0715a-113">Specifies the unique identifier of the WIA 2.0 device.</span></span>

</dd> <dt>

<span data-ttu-id="0715a-114">*ppWiaItem2Root* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="0715a-114">*ppWiaItem2Root* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0715a-115">Tipo: **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="0715a-115">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="0715a-116">Riceve l'indirizzo di un puntatore all'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento radice nell'albero gerarchico per il dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="0715a-116">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item in the hierarchical tree for the WIA 2.0 device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0715a-117">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="0715a-117">Return value</span></span>

<span data-ttu-id="0715a-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="0715a-118">Type: **HRESULT**</span></span>

<span data-ttu-id="0715a-119">Se questo metodo ha esito positivo, restituisce **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="0715a-119">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0715a-120">In caso contrario, restituisce un codice di errore **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0715a-120">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="0715a-121">Commenti</span><span class="sxs-lookup"><span data-stu-id="0715a-121">Remarks</span></span>

<span data-ttu-id="0715a-122">Le applicazioni usano il metodo **IWiaDevMgr2:: CreateDevice** per creare un oggetto dispositivo per i dispositivi WIA 2,0 specificati dal parametro bstrDeviceID.</span><span class="sxs-lookup"><span data-stu-id="0715a-122">Applications use the **IWiaDevMgr2::CreateDevice** method to create a device object for the WIA 2.0 devices specified by the bstrDeviceID parameter.</span></span> <span data-ttu-id="0715a-123">Quando restituisce, il metodo **IWiaDevMgr2:: CreateDevice** archivia un indirizzo di un puntatore nel parametro *ppWiaItem2Root*, che fa riferimento all'elemento radice della struttura ad albero di oggetti [**IWiaItem2**](-wia-iwiaitem2.md) creati da **IWiaDevMgr2:: CreateDevice**.</span><span class="sxs-lookup"><span data-stu-id="0715a-123">When it returns, the **IWiaDevMgr2::CreateDevice** method stores an address of a pointer in the parameter *ppWiaItem2Root*, which points to the root item of the tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects created by **IWiaDevMgr2::CreateDevice**.</span></span> <span data-ttu-id="0715a-124">Le applicazioni possono usare questo albero di oggetti per controllare e recuperare i dati dal dispositivo WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="0715a-124">Applications can use this tree of objects to control and retrieve data from the WIA 2.0 device.</span></span>

<span data-ttu-id="0715a-125">Le applicazioni devono chiamare il metodo [IUnknown:: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sui puntatori ricevuti tramite il parametro *ppWiaItem2Root* .</span><span class="sxs-lookup"><span data-stu-id="0715a-125">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the pointers they receive through the *ppWiaItem2Root* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="0715a-126">Requisiti</span><span class="sxs-lookup"><span data-stu-id="0715a-126">Requirements</span></span>



| <span data-ttu-id="0715a-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="0715a-127">Requirement</span></span> | <span data-ttu-id="0715a-128">Valore</span><span class="sxs-lookup"><span data-stu-id="0715a-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0715a-129">Client minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0715a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0715a-130">\[Solo app desktop di Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0715a-130">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0715a-131">Server minimo supportato</span><span class="sxs-lookup"><span data-stu-id="0715a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0715a-132">\[Solo app desktop Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0715a-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0715a-133">Intestazione</span><span class="sxs-lookup"><span data-stu-id="0715a-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0715a-134"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="0715a-134"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="0715a-135">IDL</span><span class="sxs-lookup"><span data-stu-id="0715a-135">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0715a-136"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0715a-136"><dt>Wia.idl</dt></span></span> </dl> |



 

 
