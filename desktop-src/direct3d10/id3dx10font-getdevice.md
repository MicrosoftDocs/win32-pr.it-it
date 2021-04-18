---
description: Recuperare il dispositivo Direct3D associato all'oggetto tipo di carattere.
ms.assetid: aad2406e-9461-4a84-9875-74b53d68ef40
title: 'Metodo ID3DX10Font:: GetDevice (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Font.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 72719e07c62b681579162fda56000d2d6238bd52
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322761"
---
# <a name="id3dx10fontgetdevice-method"></a><span data-ttu-id="5c514-103">Metodo ID3DX10Font:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="5c514-103">ID3DX10Font::GetDevice method</span></span>

<span data-ttu-id="5c514-104">Recuperare il dispositivo Direct3D associato all'oggetto tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="5c514-104">Retrieve the Direct3D device associated with the font object.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c514-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c514-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="5c514-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c514-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c514-107">*ppDevice* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c514-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c514-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="5c514-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="5c514-109">Indirizzo di un puntatore a un'interfaccia ID3D10Device, che rappresenta l'oggetto dispositivo Direct3D associato all'oggetto del tipo di carattere.</span><span class="sxs-lookup"><span data-stu-id="5c514-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the font object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c514-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c514-110">Return value</span></span>

<span data-ttu-id="5c514-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c514-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c514-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5c514-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5c514-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DERR \_ INVALIDCALL, D3DXERR \_ INVALIDDATA.</span><span class="sxs-lookup"><span data-stu-id="5c514-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c514-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c514-114">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="5c514-115">La chiamata a questo metodo aumenterà il conteggio dei riferimenti interni nell'interfaccia ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="5c514-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span> <span data-ttu-id="5c514-116">Assicurarsi di chiamare IUnknown al termine dell'uso di questa interfaccia ID3D10Device o si disporrà di una perdita di memoria.</span><span class="sxs-lookup"><span data-stu-id="5c514-116">Be sure to call IUnknown when you are done using this ID3D10Device interface or you will have a memory leak.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="5c514-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c514-117">Requirements</span></span>



| <span data-ttu-id="5c514-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c514-118">Requirement</span></span> | <span data-ttu-id="5c514-119">Valore</span><span class="sxs-lookup"><span data-stu-id="5c514-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c514-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c514-120">Header</span></span><br/>  | <dl> <span data-ttu-id="5c514-121"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c514-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="5c514-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c514-122">Library</span></span><br/> | <dl> <span data-ttu-id="5c514-123"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c514-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5c514-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c514-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c514-125">ID3DX10Font</span><span class="sxs-lookup"><span data-stu-id="5c514-125">ID3DX10Font</span></span>](id3dx10font.md)
</dt> <dt>

[<span data-ttu-id="5c514-126">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="5c514-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




