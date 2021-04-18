---
description: Rimuove tutte le risorse dal dispositivo impostando i relativi puntatori su NULL. Questa operazione deve essere chiamata durante l'arresto dell'applicazione. Consente di assicurare che, quando si rilasciano tutte le relative risorse, nessuna delle quali è associata al dispositivo.
ms.assetid: f41ce97e-5a81-43a4-a8c7-7411b43c0d61
title: Funzione D3DX10UnsetAllDeviceObjects (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10UnsetAllDeviceObjects
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 4d3a113be935f77dbd62b2f3fac4c16c7cac9881
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322764"
---
# <a name="d3dx10unsetalldeviceobjects-function"></a><span data-ttu-id="7e6d5-105">D3DX10UnsetAllDeviceObjects (funzione)</span><span class="sxs-lookup"><span data-stu-id="7e6d5-105">D3DX10UnsetAllDeviceObjects function</span></span>

<span data-ttu-id="7e6d5-106">Rimuove tutte le risorse dal dispositivo impostando i relativi puntatori su **null**.</span><span class="sxs-lookup"><span data-stu-id="7e6d5-106">Removes all resources from the device by setting their pointers to **NULL**.</span></span> <span data-ttu-id="7e6d5-107">Questa operazione deve essere chiamata durante l'arresto dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="7e6d5-107">This should be called during shutdown of your application.</span></span> <span data-ttu-id="7e6d5-108">Consente di assicurare che, quando si rilasciano tutte le relative risorse, nessuna delle quali è associata al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e6d5-108">It helps ensure that when one is releasing all of their resources that none of them are bound to the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7e6d5-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="7e6d5-109">Syntax</span></span>


```C++
HRESULT D3DX10UnsetAllDeviceObjects(
  _In_ ID3D10Device *pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="7e6d5-110">Parametri</span><span class="sxs-lookup"><span data-stu-id="7e6d5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7e6d5-111">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7e6d5-111">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7e6d5-112">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="7e6d5-112">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="7e6d5-113">Puntatore al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="7e6d5-113">Pointer to the device.</span></span> <span data-ttu-id="7e6d5-114">Vedere [**interfaccia ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span><span class="sxs-lookup"><span data-stu-id="7e6d5-114">See [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7e6d5-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="7e6d5-115">Return value</span></span>

<span data-ttu-id="7e6d5-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7e6d5-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7e6d5-117">Il valore restituito è uno dei valori elencati in [codici restituiti Direct3D 10](d3d10-graphics-reference-returnvalues.md).</span><span class="sxs-lookup"><span data-stu-id="7e6d5-117">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e6d5-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="7e6d5-118">Requirements</span></span>



| <span data-ttu-id="7e6d5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e6d5-119">Requirement</span></span> | <span data-ttu-id="7e6d5-120">Valore</span><span class="sxs-lookup"><span data-stu-id="7e6d5-120">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7e6d5-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="7e6d5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="7e6d5-122"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="7e6d5-122"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="7e6d5-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="7e6d5-123">Library</span></span><br/> | <dl> <span data-ttu-id="7e6d5-124"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7e6d5-124"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="7e6d5-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="7e6d5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e6d5-126">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="7e6d5-126">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




