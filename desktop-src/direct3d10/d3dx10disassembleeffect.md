---
description: Nota invece di usare questa funzione legacy, è consigliabile usare l'API D3DDisassemble. Questa funzione, che disassembla un effetto compilato in una stringa di testo che contiene istruzioni di assembly e assegnazioni di registro, è stata deprecata.
ms.assetid: 218ac120-33ce-44db-84a7-99fef3281f07
title: Funzione D3DX10DisassembleEffect (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleEffect
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 67fe19365616e779bd17ab689550b34737288317
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969426"
---
# <a name="d3dx10disassembleeffect-function"></a><span data-ttu-id="842b7-104">D3DX10DisassembleEffect (funzione)</span><span class="sxs-lookup"><span data-stu-id="842b7-104">D3DX10DisassembleEffect function</span></span>

> [!Note]  
> <span data-ttu-id="842b7-105">Invece di usare questa funzione legacy, è consigliabile usare l'API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="842b7-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="842b7-106">Questa funzione, che disassembla un effetto compilato in una stringa di testo che contiene istruzioni di assembly e assegnazioni di registro, è stata deprecata.</span><span class="sxs-lookup"><span data-stu-id="842b7-106">This function -- which disassembles a compiled effect into a text string that contains assembly instructions and register assignments -- has been deprecated.</span></span> <span data-ttu-id="842b7-107">Usare invece [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="842b7-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="842b7-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="842b7-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleEffect(
  _In_  ID3D10Effect *pEffect,
  _In_  BOOL         EnableColorCode,
  _Out_ ID3D10Blob   **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="842b7-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="842b7-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="842b7-110">*pEffect* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="842b7-110">*pEffect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="842b7-111">Tipo: **[ **ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span><span class="sxs-lookup"><span data-stu-id="842b7-111">Type: **[**ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)\***</span></span>

<span data-ttu-id="842b7-112">Un puntatore all'interfaccia effetto (vedere [**interfaccia ID3D10Effect**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span><span class="sxs-lookup"><span data-stu-id="842b7-112">A pointer to the effect interface (see [**ID3D10Effect Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)).</span></span>

</dd> <dt>

<span data-ttu-id="842b7-113">*EnableColorCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="842b7-113">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="842b7-114">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="842b7-114">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="842b7-115">Includere i tag HTML nell'output per codificare il risultato.</span><span class="sxs-lookup"><span data-stu-id="842b7-115">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="842b7-116">*ppDisassembly* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="842b7-116">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="842b7-117">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="842b7-117">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="842b7-118">Indirizzo di un buffer (vedere [**interfaccia ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene l'effetto disassemblato.</span><span class="sxs-lookup"><span data-stu-id="842b7-118">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="842b7-119">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="842b7-119">Return value</span></span>

<span data-ttu-id="842b7-120">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="842b7-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="842b7-121">Restituisce uno dei seguenti [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="842b7-121">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="842b7-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="842b7-122">Requirements</span></span>



| <span data-ttu-id="842b7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="842b7-123">Requirement</span></span> | <span data-ttu-id="842b7-124">Valore</span><span class="sxs-lookup"><span data-stu-id="842b7-124">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="842b7-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="842b7-125">Header</span></span><br/> | <dl> <span data-ttu-id="842b7-126"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="842b7-126"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="842b7-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="842b7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="842b7-128">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="842b7-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
