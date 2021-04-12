---
description: Recuperare il dispositivo associato all'oggetto Sprite.
ms.assetid: 9119b232-22c8-4b05-b584-ce176370ca97
title: 'Metodo ID3DX10Sprite:: GetDevice (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.GetDevice
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d4e7a3c6ebfcbcb83aaaed6273ea321b33a44ce1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356114"
---
# <a name="id3dx10spritegetdevice-method"></a><span data-ttu-id="ef866-103">Metodo ID3DX10Sprite:: GetDevice</span><span class="sxs-lookup"><span data-stu-id="ef866-103">ID3DX10Sprite::GetDevice method</span></span>

<span data-ttu-id="ef866-104">Recuperare il dispositivo associato all'oggetto Sprite.</span><span class="sxs-lookup"><span data-stu-id="ef866-104">Retrieve the device associated with the sprite object.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef866-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="ef866-105">Syntax</span></span>


```C++
HRESULT GetDevice(
  [out] ID3D10Device **ppDevice
);
```



## <a name="parameters"></a><span data-ttu-id="ef866-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="ef866-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef866-107">*ppDevice* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ef866-107">*ppDevice* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ef866-108">Tipo: **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span><span class="sxs-lookup"><span data-stu-id="ef866-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\*\***</span></span>

<span data-ttu-id="ef866-109">Indirizzo di un puntatore a un'interfaccia ID3D10Device, che rappresenta l'oggetto dispositivo Direct3D associato all'oggetto Sprite.</span><span class="sxs-lookup"><span data-stu-id="ef866-109">Address of a pointer to an ID3D10Device interface, representing the Direct3D device object associated with the sprite object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef866-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="ef866-110">Return value</span></span>

<span data-ttu-id="ef866-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ef866-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ef866-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ef866-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="ef866-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="ef866-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef866-114">Commenti</span><span class="sxs-lookup"><span data-stu-id="ef866-114">Remarks</span></span>

<span data-ttu-id="ef866-115">La chiamata a questo metodo aumenterà il conteggio dei riferimenti interni nell'interfaccia ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="ef866-115">Calling this method will increase the internal reference count on the ID3D10Device interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef866-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="ef866-116">Requirements</span></span>



| <span data-ttu-id="ef866-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ef866-117">Requirement</span></span> | <span data-ttu-id="ef866-118">Valore</span><span class="sxs-lookup"><span data-stu-id="ef866-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ef866-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="ef866-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ef866-120"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="ef866-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="ef866-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="ef866-121">Library</span></span><br/> | <dl> <span data-ttu-id="ef866-122"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ef866-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ef866-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="ef866-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ef866-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="ef866-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="ef866-125">Interfacce D3DX</span><span class="sxs-lookup"><span data-stu-id="ef866-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




