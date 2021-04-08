---
description: Imposta le costanti sui rispettivi valori predefiniti. I valori predefiniti sono dichiarati nelle dichiarazioni di variabili nello shader.
ms.assetid: 593a3a1b-cf96-4d46-9917-21068def0988
title: 'Metodo ID3DXConstantTable:: sedefaults (D3DX9Shader. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXConstantTable.SetDefaults
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ed49e626c979f7146b42078cf1f65fdd6716efc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103762071"
---
# <a name="id3dxconstanttablesetdefaults-method"></a><span data-ttu-id="6a421-104">Metodo ID3DXConstantTable:: sedefaults</span><span class="sxs-lookup"><span data-stu-id="6a421-104">ID3DXConstantTable::SetDefaults method</span></span>

<span data-ttu-id="6a421-105">Imposta le costanti sui rispettivi valori predefiniti.</span><span class="sxs-lookup"><span data-stu-id="6a421-105">Sets the constants to their default values.</span></span> <span data-ttu-id="6a421-106">I valori predefiniti sono dichiarati nelle dichiarazioni di variabili nello shader.</span><span class="sxs-lookup"><span data-stu-id="6a421-106">The default values are declared in the variable declarations in the shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a421-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6a421-107">Syntax</span></span>


```C++
HRESULT SetDefaults(
  [in] LPDIRECT3DDEVICE9 pDevice
);
```



## <a name="parameters"></a><span data-ttu-id="6a421-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="6a421-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a421-109">*PDEVICE* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="6a421-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a421-110">Tipo: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="6a421-110">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="6a421-111">Puntatore a un'interfaccia [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , che rappresenta il dispositivo associato alla tabella delle costanti.</span><span class="sxs-lookup"><span data-stu-id="6a421-111">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the constant table.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a421-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6a421-112">Return value</span></span>

<span data-ttu-id="6a421-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6a421-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6a421-114">Se il metodo ha esito positivo, il valore restituito è D3D \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6a421-114">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="6a421-115">Se il metodo ha esito negativo, il valore restituito può essere D3DERR \_ INVALIDCALL.</span><span class="sxs-lookup"><span data-stu-id="6a421-115">If the method fails, the return value can be D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a421-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6a421-116">Requirements</span></span>



| <span data-ttu-id="6a421-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a421-117">Requirement</span></span> | <span data-ttu-id="6a421-118">Valore</span><span class="sxs-lookup"><span data-stu-id="6a421-118">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a421-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6a421-119">Header</span></span><br/>  | <dl> <span data-ttu-id="6a421-120"><dt>D3DX9Shader. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a421-120"><dt>D3DX9Shader.h</dt></span></span> </dl> |
| <span data-ttu-id="6a421-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="6a421-121">Library</span></span><br/> | <dl> <span data-ttu-id="6a421-122"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6a421-122"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="6a421-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6a421-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a421-124">ID3DXConstantTable</span><span class="sxs-lookup"><span data-stu-id="6a421-124">ID3DXConstantTable</span></span>](id3dxconstanttable.md)
</dt> </dl>

 

 
