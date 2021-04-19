---
description: 'Accedere al buffer dei vertici della mesh dopo che è stato eseguito il commit nel dispositivo con ID3DX10Mesh:: CommitToDevice. Questa operazione è diversa da ID3DX10Mesh:: GetVertexBuffer, che restituisce il buffer dei vertici prima che sia stato eseguito il commit nel dispositivo.'
ms.assetid: 621d9105-e55d-47b8-8557-8adb7db19d66
title: 'Metodo ID3DX10Mesh:: GetDeviceVertexBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceVertexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9943050d174acb4e8f8e676f56a95cfdcde88f5a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323147"
---
# <a name="id3dx10meshgetdevicevertexbuffer-method"></a><span data-ttu-id="209e1-104">Metodo ID3DX10Mesh:: GetDeviceVertexBuffer</span><span class="sxs-lookup"><span data-stu-id="209e1-104">ID3DX10Mesh::GetDeviceVertexBuffer method</span></span>

<span data-ttu-id="209e1-105">Accedere al buffer dei vertici della mesh dopo che è stato eseguito il commit nel dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md).</span><span class="sxs-lookup"><span data-stu-id="209e1-105">Access the mesh's vertex buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="209e1-106">Questa operazione è diversa da [**ID3DX10Mesh:: GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), che restituisce il buffer dei vertici prima che sia stato eseguito il commit nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="209e1-106">This is different from [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), which returns the vertex buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="209e1-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="209e1-107">Syntax</span></span>


```C++
HRESULT GetDeviceVertexBuffer(
  [in]  UINT         iBuffer,
  [out] ID3D10Buffer **ppVertexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="209e1-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="209e1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="209e1-109">*IBuffer* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="209e1-109">*iBuffer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="209e1-110">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="209e1-110">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="209e1-111">Indice che identifica il buffer dei vertici a cui accedere.</span><span class="sxs-lookup"><span data-stu-id="209e1-111">An index identifying which vertex buffer to access.</span></span>

</dd> <dt>

<span data-ttu-id="209e1-112">*ppVertexBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="209e1-112">*ppVertexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="209e1-113">Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="209e1-113">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="209e1-114">Buffer dei vertici dopo che è stato eseguito il commit nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="209e1-114">The vertex buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="209e1-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="209e1-115">Return value</span></span>

<span data-ttu-id="209e1-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="209e1-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="209e1-117">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="209e1-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="209e1-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="209e1-118">Requirements</span></span>



| <span data-ttu-id="209e1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="209e1-119">Requirement</span></span> | <span data-ttu-id="209e1-120">Valore</span><span class="sxs-lookup"><span data-stu-id="209e1-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="209e1-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="209e1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="209e1-122"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="209e1-122"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="209e1-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="209e1-123">Library</span></span><br/> | <dl> <span data-ttu-id="209e1-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="209e1-124"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="209e1-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="209e1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="209e1-126">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="209e1-126">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="209e1-127">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="209e1-127">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
