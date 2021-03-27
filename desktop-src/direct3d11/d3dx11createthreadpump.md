---
title: Funzione D3DX11CreateThreadPump (D3DX11core. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare una pompa di thread.
ms.assetid: 8983a2e2-185f-43c0-baf0-a4c883d91220
keywords:
- Funzione D3DX11CreateThreadPump Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5551cd22a4c134570c2059cc6aeaa9538311b19
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104982337"
---
# <a name="d3dx11createthreadpump-function"></a><span data-ttu-id="ffc76-106">D3DX11CreateThreadPump (funzione)</span><span class="sxs-lookup"><span data-stu-id="ffc76-106">D3DX11CreateThreadPump function</span></span>

> [!Note]  
> <span data-ttu-id="ffc76-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="ffc76-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="ffc76-108">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="ffc76-108">See Remarks.</span></span>

 

<span data-ttu-id="ffc76-109">Creare una pompa di thread.</span><span class="sxs-lookup"><span data-stu-id="ffc76-109">Create a thread pump.</span></span>

## <a name="syntax"></a><span data-ttu-id="ffc76-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ffc76-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateThreadPump(
  _In_  UINT              cIoThreads,
  _In_  UINT              cProcThreads,
  _Out_ ID3DX11ThreadPump **ppThreadPump
);
```



## <a name="parameters"></a><span data-ttu-id="ffc76-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="ffc76-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ffc76-112">*cIoThreads* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffc76-112">*cIoThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffc76-113">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ffc76-113">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ffc76-114">Numero di thread I/O da creare.</span><span class="sxs-lookup"><span data-stu-id="ffc76-114">The number of I/O threads to create.</span></span> <span data-ttu-id="ffc76-115">Se si specifica 0, Direct3D tenterà di calcolare il numero ottimale di thread in base alla configurazione hardware.</span><span class="sxs-lookup"><span data-stu-id="ffc76-115">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="ffc76-116">*cProcThreads* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ffc76-116">*cProcThreads* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ffc76-117">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="ffc76-117">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="ffc76-118">Numero di thread di processo da creare.</span><span class="sxs-lookup"><span data-stu-id="ffc76-118">The number of process threads to create.</span></span> <span data-ttu-id="ffc76-119">Se si specifica 0, Direct3D tenterà di calcolare il numero ottimale di thread in base alla configurazione hardware.</span><span class="sxs-lookup"><span data-stu-id="ffc76-119">If 0 is specified, Direct3D will attempt to calculate the optimal number of threads based on the hardware configuration.</span></span>

</dd> <dt>

<span data-ttu-id="ffc76-120">*ppThreadPump* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ffc76-120">*ppThreadPump* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ffc76-121">Tipo: **[ **ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ffc76-121">Type: **[**ID3DX11ThreadPump**](id3dx11threadpump.md)\*\***</span></span>

<span data-ttu-id="ffc76-122">Pompa di thread creata.</span><span class="sxs-lookup"><span data-stu-id="ffc76-122">The created thread pump.</span></span> <span data-ttu-id="ffc76-123">Vedere [**interfaccia ID3DX11ThreadPump**](id3dx11threadpump.md).</span><span class="sxs-lookup"><span data-stu-id="ffc76-123">See [**ID3DX11ThreadPump Interface**](id3dx11threadpump.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ffc76-124">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ffc76-124">Return value</span></span>

<span data-ttu-id="ffc76-125">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ffc76-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ffc76-126">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="ffc76-126">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ffc76-127">Commenti</span><span class="sxs-lookup"><span data-stu-id="ffc76-127">Remarks</span></span>

<span data-ttu-id="ffc76-128">Una pompa di thread è un oggetto con utilizzo intensivo delle risorse.</span><span class="sxs-lookup"><span data-stu-id="ffc76-128">A thread pump is a very resource-intensive object.</span></span> <span data-ttu-id="ffc76-129">Per ogni applicazione è necessario creare solo un thread pump.</span><span class="sxs-lookup"><span data-stu-id="ffc76-129">Only one thread pump should be created per application.</span></span>

<span data-ttu-id="ffc76-130">Non è presente alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="ffc76-130">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="ffc76-131">Per le app di Windows Store, gli esempi di DirectX (ad esempio, l' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="ffc76-131">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="ffc76-132">Per le applicazioni desktop Win32, è possibile utilizzare il [runtime di concorrenza](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) per implementare un modello simile a quello del Windows Runtime modello di programmazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="ffc76-132">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffc76-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ffc76-133">Requirements</span></span>



| <span data-ttu-id="ffc76-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="ffc76-134">Requirement</span></span> | <span data-ttu-id="ffc76-135">Valore</span><span class="sxs-lookup"><span data-stu-id="ffc76-135">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffc76-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ffc76-136">Header</span></span><br/>  | <dl> <span data-ttu-id="ffc76-137"><dt>D3DX11core. h</dt></span><span class="sxs-lookup"><span data-stu-id="ffc76-137"><dt>D3DX11core.h</dt></span></span> </dl> |
| <span data-ttu-id="ffc76-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="ffc76-138">Library</span></span><br/> | <dl> <span data-ttu-id="ffc76-139"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ffc76-139"><dt>D3DX11.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ffc76-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ffc76-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffc76-141">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="ffc76-141">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

