---
description: Registra i modelli personalizzati.
ms.assetid: e142a0f2-d0ef-4479-82cd-ba8d5059d1d2
title: 'Metodo ID3DXFile:: RegisterTemplates (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.RegisterTemplates
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b7864b63d55ba219c5076920acc809f824bc1820
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322990"
---
# <a name="id3dxfileregistertemplates-method"></a><span data-ttu-id="e1d55-103">Metodo ID3DXFile:: RegisterTemplates</span><span class="sxs-lookup"><span data-stu-id="e1d55-103">ID3DXFile::RegisterTemplates method</span></span>

<span data-ttu-id="e1d55-104">Registra i modelli personalizzati.</span><span class="sxs-lookup"><span data-stu-id="e1d55-104">Registers custom templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d55-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="e1d55-105">Syntax</span></span>


```C++
HRESULT RegisterTemplates(
  [in] LPCVOID pvData,
  [in] SIZE_T  cbSize
);
```



## <a name="parameters"></a><span data-ttu-id="e1d55-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="e1d55-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1d55-107">*pvData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1d55-107">*pvData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d55-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1d55-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1d55-109">Puntatore a un buffer costituito da un file con estensione x in formato testo o binario che contiene modelli.</span><span class="sxs-lookup"><span data-stu-id="e1d55-109">Pointer to a buffer consisting of a .x file in text or binary format that contains templates.</span></span>

</dd> <dt>

<span data-ttu-id="e1d55-110">*cbSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e1d55-110">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e1d55-111">Tipo: **[ **size \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e1d55-111">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e1d55-112">Dimensioni del buffer a cui punta pvData in byte.</span><span class="sxs-lookup"><span data-stu-id="e1d55-112">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1d55-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="e1d55-113">Return value</span></span>

<span data-ttu-id="e1d55-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e1d55-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e1d55-115">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e1d55-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="e1d55-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="e1d55-116">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d55-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="e1d55-117">Remarks</span></span>

<span data-ttu-id="e1d55-118">Il seguente frammento di codice fornisce una chiamata di esempio a **RegisterTemplates** e il contenuto di esempio per il buffer a cui punta **pvData** .</span><span class="sxs-lookup"><span data-stu-id="e1d55-118">The following code fragment provides an example call to **RegisterTemplates** And example contents for the buffer to which **pvData** points.</span></span>


```
#define XSKINEXP_TEMPLATES \
    "xof 0303txt 0032\
    template XSkinMeshHeader \
    { \
        <3CF169CE-FF7C-44ab-93C0-F78F62D172E2> \
        WORD nMaxSkinWeightsPerVertex; \
        WORD nMaxSkinWeightsPerFace; \
        WORD nBones; \
    } \
    template VertexDuplicationIndices \
    { \
        <B8D65549-D7C9-4995-89CF-53A9A8B031E3> \
        DWORD nIndices; \
        DWORD nOriginalVertices; \
        array DWORD indices[nIndices]; \
    } \
    template SkinWeights \
    { \
        <6F0D123B-BAD2-4167-A0D0-80224F25FABB> \
        STRING transformNodeName;\
        DWORD nWeights; \
        array DWORD vertexIndices[nWeights]; \
        array float weights[nWeights]; \
        Matrix4x4 matrixOffset; \
    }"
.
.
.
        
LPD3DXFILE pD3DXFile = NULL;

if ( FAILED 
        (hr = pD3DXFile->RegisterTemplates( 
            (LPVOID)XSKINEXP_TEMPLATES,
            sizeof( XSKINEXP_TEMPLATES ) - 1 ) ) )
goto End;
```



<span data-ttu-id="e1d55-119">Tutti i modelli devono specificare un nome e un UUID.</span><span class="sxs-lookup"><span data-stu-id="e1d55-119">All templates must specify a name and a UUID.</span></span>

<span data-ttu-id="e1d55-120">Questo metodo chiama il metodo [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) , ottenendo un puntatore all'interfaccia [**ID3DXFileEnumObject**](id3dxfileenumobject.md) chiamando [**CreateEnumObject**](id3dxfile--createenumobject.md) con **pvData** come primo parametro.</span><span class="sxs-lookup"><span data-stu-id="e1d55-120">This method calls the [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) method, obtaining an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) interface pointer by calling [**CreateEnumObject**](id3dxfile--createenumobject.md) with **pvData** as the first parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d55-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="e1d55-121">Requirements</span></span>



| <span data-ttu-id="e1d55-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1d55-122">Requirement</span></span> | <span data-ttu-id="e1d55-123">Valore</span><span class="sxs-lookup"><span data-stu-id="e1d55-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d55-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="e1d55-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e1d55-125"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="e1d55-125"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="e1d55-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="e1d55-126">Library</span></span><br/> | <dl> <span data-ttu-id="e1d55-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e1d55-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="e1d55-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="e1d55-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d55-129">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="e1d55-129">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="e1d55-130">**RegisterEnumTemplates**</span><span class="sxs-lookup"><span data-stu-id="e1d55-130">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md)
</dt> </dl>

 

 
