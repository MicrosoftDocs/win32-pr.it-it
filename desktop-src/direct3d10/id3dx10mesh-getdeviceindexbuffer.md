---
description: "Accedere al buffer di indice della mesh dopo che è stato eseguito il commit nel dispositivo con ID3DX10Mesh:: CommitToDevice. Questa operazione è diversa da ID3DX10Mesh:: GetIndexBuffer, che restituisce il buffer dell'indice prima che sia stato eseguito il commit nel dispositivo."
ms.assetid: 94d21f50-91b5-4f8d-ac73-7a851bba8685
title: 'Metodo ID3DX10Mesh:: GetDeviceIndexBuffer (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Mesh.GetDeviceIndexBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3ec3e65cfc4acb5a903bcf18d2f707d39127e975
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323148"
---
# <a name="id3dx10meshgetdeviceindexbuffer-method"></a><span data-ttu-id="cc493-104">Metodo ID3DX10Mesh:: GetDeviceIndexBuffer</span><span class="sxs-lookup"><span data-stu-id="cc493-104">ID3DX10Mesh::GetDeviceIndexBuffer method</span></span>

<span data-ttu-id="cc493-105">Accedere al buffer di indice della mesh dopo che è stato eseguito il commit nel dispositivo con [**ID3DX10Mesh:: CommitToDevice**](id3dx10mesh-committodevice.md).</span><span class="sxs-lookup"><span data-stu-id="cc493-105">Access the mesh's index buffer after it has been committed to the device with [**ID3DX10Mesh::CommitToDevice**](id3dx10mesh-committodevice.md).</span></span> <span data-ttu-id="cc493-106">Questa operazione è diversa da [**ID3DX10Mesh:: GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), che restituisce il buffer dell'indice prima che sia stato eseguito il commit nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc493-106">This is different from [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), which returns the index buffer before it has been committed to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="cc493-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="cc493-107">Syntax</span></span>


```C++
HRESULT GetDeviceIndexBuffer(
  [out] ID3D10Buffer **ppIndexBuffer
);
```



## <a name="parameters"></a><span data-ttu-id="cc493-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="cc493-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cc493-109">*ppIndexBuffer* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="cc493-109">*ppIndexBuffer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cc493-110">Tipo: **[ **ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span><span class="sxs-lookup"><span data-stu-id="cc493-110">Type: **[**ID3D10Buffer**](/windows/desktop/api/D3D10/nn-d3d10-id3d10buffer)\*\***</span></span>

<span data-ttu-id="cc493-111">Buffer dell'indice dopo che è stato eseguito il commit nel dispositivo.</span><span class="sxs-lookup"><span data-stu-id="cc493-111">The index buffer after it has been committed to the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cc493-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="cc493-112">Return value</span></span>

<span data-ttu-id="cc493-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="cc493-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="cc493-114">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="cc493-114">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cc493-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="cc493-115">Remarks</span></span>

<span data-ttu-id="cc493-116">Se non è ancora stato eseguito il commit del buffer di indice della mesh nel dispositivo, questa API eseguirà automaticamente il commit del buffer dell'indice prima di restituire un puntatore al buffer.</span><span class="sxs-lookup"><span data-stu-id="cc493-116">If the mesh's index buffer has not already been committed to the device, this API will automatically commit the index buffer before it returns a pointer to the buffer.</span></span>

## <a name="requirements"></a><span data-ttu-id="cc493-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="cc493-117">Requirements</span></span>



| <span data-ttu-id="cc493-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="cc493-118">Requirement</span></span> | <span data-ttu-id="cc493-119">Valore</span><span class="sxs-lookup"><span data-stu-id="cc493-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="cc493-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="cc493-120">Header</span></span><br/>  | <dl> <span data-ttu-id="cc493-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="cc493-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="cc493-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="cc493-122">Library</span></span><br/> | <dl> <span data-ttu-id="cc493-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cc493-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cc493-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="cc493-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cc493-125">ID3DX10Mesh</span><span class="sxs-lookup"><span data-stu-id="cc493-125">ID3DX10Mesh</span></span>](id3dx10mesh.md)
</dt> <dt>

[<span data-ttu-id="cc493-126">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="cc493-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




