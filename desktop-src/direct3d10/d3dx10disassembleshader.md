---
description: Nota invece di usare questa funzione legacy, è consigliabile usare l'API D3DDisassemble. Questa funzione, che disassembla uno shader compilato in una stringa di testo che contiene istruzioni di assembly e assegnazioni di registro, non esiste più.
ms.assetid: f94264f8-121a-4bb7-bf1f-cc5d2cac6cd2
title: Funzione D3DX10DisassembleShader (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10DisassembleShader
api_type:
- HeaderDef
api_location:
- D3DX10Core.h
ms.openlocfilehash: 13716fd5d25e2e8602379ea3864c516fa5388475
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322090"
---
# <a name="d3dx10disassembleshader-function"></a><span data-ttu-id="c03a4-104">D3DX10DisassembleShader (funzione)</span><span class="sxs-lookup"><span data-stu-id="c03a4-104">D3DX10DisassembleShader function</span></span>

> [!Note]  
> <span data-ttu-id="c03a4-105">Invece di usare questa funzione legacy, è consigliabile usare l'API [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) .</span><span class="sxs-lookup"><span data-stu-id="c03a4-105">Instead of using this legacy function, we recommend that you use the [**D3DDisassemble**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble) API.</span></span>

 

<span data-ttu-id="c03a4-106">Questa funzione, che disassembla uno shader compilato in una stringa di testo che contiene istruzioni di assembly e assegnazioni di registro, non esiste più.</span><span class="sxs-lookup"><span data-stu-id="c03a4-106">This function -- which disassembles a compiled shader into a text string that contains assembly instructions and register assignments -- no longer exists.</span></span> <span data-ttu-id="c03a4-107">Usare invece [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span><span class="sxs-lookup"><span data-stu-id="c03a4-107">Instead, use [**D3DDisassemble10Effect**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3ddisassemble10effect).</span></span>

## <a name="syntax"></a><span data-ttu-id="c03a4-108">Sintassi</span><span class="sxs-lookup"><span data-stu-id="c03a4-108">Syntax</span></span>


```C++
HRESULT D3DX10DisassembleShader(
  _In_  const void       *pShader,
  _In_        SIZE_T     BytecodeLength,
  _In_        BOOL       EnableColorCode,
  _In_        LPCSTR     pComments,
  _Out_       ID3D10Blob **ppDisassembly
);
```



## <a name="parameters"></a><span data-ttu-id="c03a4-109">Parametri</span><span class="sxs-lookup"><span data-stu-id="c03a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c03a4-110">*pShader* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c03a4-110">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c03a4-111">Tipo: **const \* void**</span><span class="sxs-lookup"><span data-stu-id="c03a4-111">Type: **const void\***</span></span>

<span data-ttu-id="c03a4-112">Puntatore allo [**shader compilato**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span><span class="sxs-lookup"><span data-stu-id="c03a4-112">A pointer to the [**compiled shader**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createinputlayout).</span></span>

</dd> <dt>

<span data-ttu-id="c03a4-113">*BytecodeLength* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c03a4-113">*BytecodeLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c03a4-114">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c03a4-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c03a4-115">Dimensioni di pShader.</span><span class="sxs-lookup"><span data-stu-id="c03a4-115">The size of pShader.</span></span>

</dd> <dt>

<span data-ttu-id="c03a4-116">*EnableColorCode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c03a4-116">*EnableColorCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c03a4-117">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c03a4-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c03a4-118">Includere i tag HTML nell'output per codificare il risultato.</span><span class="sxs-lookup"><span data-stu-id="c03a4-118">Include HTML tags in the output to color code the result.</span></span>

</dd> <dt>

<span data-ttu-id="c03a4-119">*pComments* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c03a4-119">*pComments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c03a4-120">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c03a4-120">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c03a4-121">Stringa di commento nella parte superiore dello shader che identifica le costanti e le variabili dello shader.</span><span class="sxs-lookup"><span data-stu-id="c03a4-121">The comment string at the top of the shader that identifies the shader constants and variables.</span></span>

</dd> <dt>

<span data-ttu-id="c03a4-122">*ppDisassembly* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="c03a4-122">*ppDisassembly* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c03a4-123">Tipo: **[ **ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span><span class="sxs-lookup"><span data-stu-id="c03a4-123">Type: **[**ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)\*\***</span></span>

<span data-ttu-id="c03a4-124">Indirizzo di un buffer (vedere [**interfaccia ID3D10Blob**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) che contiene lo shader disassemblato.</span><span class="sxs-lookup"><span data-stu-id="c03a4-124">Address of a buffer (see [**ID3D10Blob Interface**](/windows/desktop/api/D3DCommon/nn-d3dcommon-id3d10blob)) which contains the disassembled shader.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c03a4-125">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="c03a4-125">Return value</span></span>

<span data-ttu-id="c03a4-126">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c03a4-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c03a4-127">Restituisce uno dei seguenti [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="c03a4-127">Returns one of the following [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c03a4-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="c03a4-128">Remarks</span></span>

<span data-ttu-id="c03a4-129">Questo testo restituito include un'intestazione con la versione del compilatore HLSL usata per generare questo oggetto, i commenti che descrivono il layout della memoria dei buffer costanti usati dallo shader, le firme di input e output e i punti di associazione delle risorse.</span><span class="sxs-lookup"><span data-stu-id="c03a4-129">This returned text includes a header with the version of the HLSL compiler used to generate this object, comments describing the memory layout of the constant buffers used by the shader, input and output signatures, and resource binding points.</span></span>

<span data-ttu-id="c03a4-130">Di seguito è riportato un esempio di disassemblaggio di uno shader compilato.</span><span class="sxs-lookup"><span data-stu-id="c03a4-130">Here is an example of disassembling a compiled shader.</span></span> <span data-ttu-id="c03a4-131">Nell'esempio si presuppone che si inizi con uno shader compilato (visualizzato come *pVSBuf* , che è possibile vedere nell' [esempio HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span><span class="sxs-lookup"><span data-stu-id="c03a4-131">The example assumes you start with a compiled shader (shown as *pVSBuf* which you can see in [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx)).</span></span>


```
LPCSTR commentString = NULL;
ID3D10Blob* pIDisassembly = NULL;
char* pDisassembly = NULL;
if( pVSBuf )
{
    D3D10DisassembleShader( (UINT*) pVSBuf->GetBufferPointer(), 
        pVSBuf->GetBufferSize(), TRUE, commentString, &pIDisassembly );
    if( pIDisassembly )
    {
        FILE* pFile = fopen( "shader.htm", "w" );
        if( pFile)
        {
            fputs( (char*)pIDisassembly->GetBufferPointer(), pFile );
            fclose( pFile );
        }
    }
}
```



## <a name="requirements"></a><span data-ttu-id="c03a4-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="c03a4-132">Requirements</span></span>



| <span data-ttu-id="c03a4-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="c03a4-133">Requirement</span></span> | <span data-ttu-id="c03a4-134">Valore</span><span class="sxs-lookup"><span data-stu-id="c03a4-134">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c03a4-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="c03a4-135">Header</span></span><br/> | <dl> <span data-ttu-id="c03a4-136"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="c03a4-136"><dt>D3DX10Core.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c03a4-137">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="c03a4-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c03a4-138">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="c03a4-138">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
