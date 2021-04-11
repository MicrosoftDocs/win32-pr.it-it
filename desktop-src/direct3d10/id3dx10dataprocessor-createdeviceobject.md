---
description: Creare un oggetto dispositivo.
ms.assetid: 5b9b00de-c744-43c7-b383-1d3358c80741
title: 'Metodo ID3DX10DataProcessor:: CreateDeviceObject (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataProcessor.CreateDeviceObject
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 1ed362f992ca2b9d3ce6e561e08e5fe7fd0bdbe3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235041"
---
# <a name="id3dx10dataprocessorcreatedeviceobject-method"></a><span data-ttu-id="eb0ac-103">Metodo ID3DX10DataProcessor:: CreateDeviceObject</span><span class="sxs-lookup"><span data-stu-id="eb0ac-103">ID3DX10DataProcessor::CreateDeviceObject method</span></span>

<span data-ttu-id="eb0ac-104">Creare un oggetto dispositivo.</span><span class="sxs-lookup"><span data-stu-id="eb0ac-104">Create a device object.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb0ac-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="eb0ac-105">Syntax</span></span>


```C++
HRESULT CreateDeviceObject(
  [out] void **ppDataObject
);
```



## <a name="parameters"></a><span data-ttu-id="eb0ac-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="eb0ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb0ac-107">*ppDataObject* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="eb0ac-107">*ppDataObject* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eb0ac-108">Tipo: **void \* \***</span><span class="sxs-lookup"><span data-stu-id="eb0ac-108">Type: **void\*\***</span></span>

<span data-ttu-id="eb0ac-109">Indirizzo di un puntatore all'oggetto dispositivo creato.</span><span class="sxs-lookup"><span data-stu-id="eb0ac-109">Address of a pointer to the created device object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb0ac-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="eb0ac-110">Return value</span></span>

<span data-ttu-id="eb0ac-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eb0ac-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eb0ac-112">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="eb0ac-112">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb0ac-113">Requisiti</span><span class="sxs-lookup"><span data-stu-id="eb0ac-113">Requirements</span></span>



| <span data-ttu-id="eb0ac-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb0ac-114">Requirement</span></span> | <span data-ttu-id="eb0ac-115">Valore</span><span class="sxs-lookup"><span data-stu-id="eb0ac-115">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="eb0ac-116">Intestazione</span><span class="sxs-lookup"><span data-stu-id="eb0ac-116">Header</span></span><br/>  | <dl> <span data-ttu-id="eb0ac-117"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="eb0ac-117"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="eb0ac-118">Libreria</span><span class="sxs-lookup"><span data-stu-id="eb0ac-118">Library</span></span><br/> | <dl> <span data-ttu-id="eb0ac-119"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="eb0ac-119"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb0ac-120">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="eb0ac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb0ac-121">ID3DX10DataProcessor</span><span class="sxs-lookup"><span data-stu-id="eb0ac-121">ID3DX10DataProcessor</span></span>](id3dx10dataprocessor.md)
</dt> <dt>

[<span data-ttu-id="eb0ac-122">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="eb0ac-122">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




