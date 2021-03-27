---
title: Funzione D3DX11CreateAsyncMemoryLoader (D3DX11async. h)
description: Nota la libreria dell'utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store. Vedere la sezione Osservazioni. Creare un caricatore di memoria asincrono.
ms.assetid: 0bf1e6a2-a968-4644-a7b4-e847ed4f7450
keywords:
- Funzione D3DX11CreateAsyncMemoryLoader Direct3D 11
topic_type:
- apiref
api_name:
- D3DX11CreateAsyncMemoryLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- LibDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d16c91b0537f79fb60a5b256789c13d664401ecc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104996035"
---
# <a name="d3dx11createasyncmemoryloader-function"></a><span data-ttu-id="18d40-106">D3DX11CreateAsyncMemoryLoader (funzione)</span><span class="sxs-lookup"><span data-stu-id="18d40-106">D3DX11CreateAsyncMemoryLoader function</span></span>

> [!Note]  
> <span data-ttu-id="18d40-107">La libreria di utilità D3DX (D3DX 9, D3DX 10 e D3DX 11) è deprecata per Windows 8 e non è supportata per le app di Windows Store.</span><span class="sxs-lookup"><span data-stu-id="18d40-107">The D3DX (D3DX 9, D3DX 10, and D3DX 11) utility library is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span> <span data-ttu-id="18d40-108">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="18d40-108">See Remarks.</span></span>

 

<span data-ttu-id="18d40-109">Creare un caricatore di memoria asincrono.</span><span class="sxs-lookup"><span data-stu-id="18d40-109">Create an asynchronous-memory loader.</span></span>

## <a name="syntax"></a><span data-ttu-id="18d40-110">Sintassi</span><span class="sxs-lookup"><span data-stu-id="18d40-110">Syntax</span></span>


```C++
HRESULT D3DX11CreateAsyncMemoryLoader(
  _In_  LPCVOID           pData,
  _In_  SIZE_T            cbData,
  _Out_ ID3DX11DataLoader **ppDataLoader
);
```



## <a name="parameters"></a><span data-ttu-id="18d40-111">Parametri</span><span class="sxs-lookup"><span data-stu-id="18d40-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18d40-112">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18d40-112">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18d40-113">Tipo: **[ **LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="18d40-113">Type: **[**LPCVOID**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="18d40-114">Puntatore ai dati.</span><span class="sxs-lookup"><span data-stu-id="18d40-114">Pointer to the data.</span></span>

</dd> <dt>

<span data-ttu-id="18d40-115">*cbData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="18d40-115">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18d40-116">Tipo: **[ **size \_ T**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="18d40-116">Type: **[**SIZE\_T**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="18d40-117">Dimensione dei dati.</span><span class="sxs-lookup"><span data-stu-id="18d40-117">Size of the data.</span></span>

</dd> <dt>

<span data-ttu-id="18d40-118">*ppDataLoader* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="18d40-118">*ppDataLoader* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="18d40-119">Tipo: **[ **ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="18d40-119">Type: **[**ID3DX11DataLoader**](id3dx11dataloader.md)\*\***</span></span>

<span data-ttu-id="18d40-120">Indirizzo di un puntatore al caricatore di dati asincrono (vedere [**interfaccia ID3DX11DataLoader**](id3dx11dataloader.md)).</span><span class="sxs-lookup"><span data-stu-id="18d40-120">The address of a pointer to the asynchronous-data loader (see [**ID3DX11DataLoader Interface**](id3dx11dataloader.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18d40-121">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="18d40-121">Return value</span></span>

<span data-ttu-id="18d40-122">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="18d40-122">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="18d40-123">Il valore restituito è uno dei valori elencati nei [codici restituiti di Direct3D 11](d3d11-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="18d40-123">The return value is one of the values listed in [Direct3D 11 Return Codes](d3d11-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="18d40-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="18d40-124">Remarks</span></span>

<span data-ttu-id="18d40-125">Non è presente alcuna implementazione del caricatore asincrono al di fuori di D3DX 10 e D3DX 11.</span><span class="sxs-lookup"><span data-stu-id="18d40-125">There s no implementation of the  async loader  outside of D3DX 10, and D3DX 11.</span></span>

<span data-ttu-id="18d40-126">Per le app di Windows Store, gli esempi di DirectX (ad esempio, l' [esempio di esercitazione Direct3D](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) includono il modulo **BasicLoader** che usa il modello di programmazione asincrona Windows Runtime ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span><span class="sxs-lookup"><span data-stu-id="18d40-126">For Windows Store apps, the DirectX samples (for example, the [Direct3D tutorial sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/Direct3D%20tutorial%20sample)) include the **BasicLoader** module that uses the Windows Runtime asynchronous programming model ([**AsyncBase**](/previous-versions/visualstudio/visual-studio-2012/br244878(v=vs.110))).</span></span>

<span data-ttu-id="18d40-127">Per le applicazioni desktop Win32, è possibile utilizzare il [runtime di concorrenza](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) per implementare un modello simile a quello del Windows Runtime modello di programmazione asincrona.</span><span class="sxs-lookup"><span data-stu-id="18d40-127">For Win32 desktop apps, you can use the [Concurrency Runtime](/previous-versions/visualstudio/visual-studio-2010/ee207192(v=vs.100)) to implement something similar to the Windows Runtime asynchronous programming model.</span></span>

## <a name="requirements"></a><span data-ttu-id="18d40-128">Requisiti</span><span class="sxs-lookup"><span data-stu-id="18d40-128">Requirements</span></span>



| <span data-ttu-id="18d40-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="18d40-129">Requirement</span></span> | <span data-ttu-id="18d40-130">Valore</span><span class="sxs-lookup"><span data-stu-id="18d40-130">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="18d40-131">Intestazione</span><span class="sxs-lookup"><span data-stu-id="18d40-131">Header</span></span><br/>  | <dl> <span data-ttu-id="18d40-132"><dt>D3DX11async. h</dt></span><span class="sxs-lookup"><span data-stu-id="18d40-132"><dt>D3DX11async.h</dt></span></span> </dl> |
| <span data-ttu-id="18d40-133">Libreria</span><span class="sxs-lookup"><span data-stu-id="18d40-133">Library</span></span><br/> | <dl> <span data-ttu-id="18d40-134"><dt>D3DX11. lib</dt></span><span class="sxs-lookup"><span data-stu-id="18d40-134"><dt>D3DX11.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="18d40-135">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="18d40-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18d40-136">Funzioni D3DX</span><span class="sxs-lookup"><span data-stu-id="18d40-136">D3DX Functions</span></span>](d3d11-graphics-reference-d3dx11-functions.md)
</dt> </dl>

 

