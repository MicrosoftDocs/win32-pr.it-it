---
description: Ottenere un puntatore a interfaccia del dispositivo Direct3D 10,1 da un puntatore a interfaccia Direct3D 10,0.
ms.assetid: cf31a67f-0493-4e79-8e73-0297ab93bbae
title: Funzione D3DX10GetFeatureLevel1 (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetFeatureLevel1
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 817eb4dd68ce797da76c0609e2ead01a21b5b270
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322145"
---
# <a name="d3dx10getfeaturelevel1-function"></a><span data-ttu-id="962c5-103">D3DX10GetFeatureLevel1 (funzione)</span><span class="sxs-lookup"><span data-stu-id="962c5-103">D3DX10GetFeatureLevel1 function</span></span>

<span data-ttu-id="962c5-104">Ottenere un puntatore a interfaccia del dispositivo Direct3D 10,1 da un puntatore a interfaccia Direct3D 10,0.</span><span class="sxs-lookup"><span data-stu-id="962c5-104">Get a Direct3D 10.1 device interface pointer from a Direct3D 10.0 interface pointer.</span></span>

## <a name="syntax"></a><span data-ttu-id="962c5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="962c5-105">Syntax</span></span>


```C++
HRESULT D3DX10GetFeatureLevel1(
  _In_  ID3D10Device  *pDevice,
  _Out_ ID3D10Device1 **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="962c5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="962c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="962c5-107">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="962c5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="962c5-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="962c5-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="962c5-109">Puntatore al dispositivo Direct3D 10,0 (vedere l'interfaccia [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) ).</span><span class="sxs-lookup"><span data-stu-id="962c5-109">Pointer to the Direct3D 10.0 device (see the [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) interface).</span></span>

</dd> <dt>

<span data-ttu-id="962c5-110">*ppDevice* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="962c5-110">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="962c5-111">Tipo: **[ **ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span><span class="sxs-lookup"><span data-stu-id="962c5-111">Type: **[**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1)\*\***</span></span>

<span data-ttu-id="962c5-112">Puntatore al dispositivo Direct3D 10,1 (vedere l'interfaccia [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) ).</span><span class="sxs-lookup"><span data-stu-id="962c5-112">Pointer to the Direct3D 10.1 device (see the [**ID3D10Device1**](/windows/desktop/api/D3D10_1/nn-d3d10_1-id3d10device1) interface).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="962c5-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="962c5-113">Return value</span></span>

<span data-ttu-id="962c5-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="962c5-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="962c5-115">Questa funzione restituisce uno dei seguenti [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="962c5-115">This function returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span> <span data-ttu-id="962c5-116">Se è possibile acquisire un'interfaccia del dispositivo Direct3D 10,1, questa funzione ha esito positivo e passa un puntatore all'interfaccia 10,1 usando il parametro *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="962c5-116">If a Direct3D 10.1 device interface can be acquired, this function succeeds and passes a pointer to the 10.1 interface using the *ppDevice* parameter.</span></span> <span data-ttu-id="962c5-117">Se non è possibile acquisire un'interfaccia del dispositivo Direct3D 10,1, questa funzione restituisce E ha \_ esito negativo e non restituisce alcun valore per il parametro *ppDevice* .</span><span class="sxs-lookup"><span data-stu-id="962c5-117">If a Direct3D 10.1 device interface cannot be acquired, this function returns E\_FAIL, and will not return anything for the *ppDevice* parameter.</span></span>

## <a name="remarks"></a><span data-ttu-id="962c5-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="962c5-118">Remarks</span></span>

<span data-ttu-id="962c5-119">Affinché questa funzione abbia esito positivo, è necessario avere acquisito il puntatore [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) fornito utilizzando una chiamata alla funzione [**D3DX10CreateDevice**](d3dx10createdevice.md) , la funzione [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) , la funzione [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) o la funzione [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) .</span><span class="sxs-lookup"><span data-stu-id="962c5-119">For this function to succeed, you must have acquired the supplied [**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device) pointer using a call to the [**D3DX10CreateDevice**](d3dx10createdevice.md) function, the [**D3DX10CreateDeviceAndSwapChain**](d3dx10createdeviceandswapchain.md) function, the [**D3D10CreateDevice1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdevice1) function, or the [**D3D10CreateDeviceAndSwapChain1**](/windows/desktop/api/D3D10_1/nf-d3d10_1-d3d10createdeviceandswapchain1) function.</span></span>

<span data-ttu-id="962c5-120">È possibile creare un dispositivo Direct3D 10,1 solo nei computer che eseguono Windows Vista Service Pack 1 o versione successiva e con l'hardware compatibile con Direct3D 10,1 installato.</span><span class="sxs-lookup"><span data-stu-id="962c5-120">You can only create a Direct3D 10.1 device on computers running Windows Vista Service Pack 1 or later, and with Direct3D 10.1-compatible hardware installed.</span></span> <span data-ttu-id="962c5-121">Questa funzione restituirà E avrà \_ esito negativo in tutti i computer che non soddisfano questi requisiti.</span><span class="sxs-lookup"><span data-stu-id="962c5-121">This function will return E\_FAIL on any computer not meeting these requirements.</span></span> <span data-ttu-id="962c5-122">Tuttavia, è possibile chiamare questa funzione in qualsiasi versione di Windows in cui è installata la DLL D3DX10.</span><span class="sxs-lookup"><span data-stu-id="962c5-122">However, you can call this function on any version of Windows that has the D3DX10 DLL installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="962c5-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="962c5-123">Requirements</span></span>



| <span data-ttu-id="962c5-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="962c5-124">Requirement</span></span> | <span data-ttu-id="962c5-125">Valore</span><span class="sxs-lookup"><span data-stu-id="962c5-125">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="962c5-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="962c5-126">Header</span></span><br/> | <dl> <span data-ttu-id="962c5-127"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="962c5-127"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="962c5-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="962c5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="962c5-129">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="962c5-129">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




