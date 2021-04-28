---
description: 'Funzione D3DXCheckVersion: verificare che la versione di D3DX compilata con sia la versione in esecuzione.'
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Funzione D3DXCheckVersion (D3dx9core.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCheckVersion
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 077d64a67a46080a0f7ac9194c684f6fe8470453
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115979"
---
# <a name="d3dxcheckversion-function"></a><span data-ttu-id="d71cf-103">Funzione D3DXCheckVersion</span><span class="sxs-lookup"><span data-stu-id="d71cf-103">D3DXCheckVersion function</span></span>

<span data-ttu-id="d71cf-104">Verificare che la versione di D3DX compilata con sia la versione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="d71cf-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="d71cf-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="d71cf-105">Syntax</span></span>


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a><span data-ttu-id="d71cf-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="d71cf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d71cf-107">*D3DSDKVersion* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d71cf-107">*D3DSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d71cf-108">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d71cf-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d71cf-109">Usare la versione D3D \_ \_ SDK.</span><span class="sxs-lookup"><span data-stu-id="d71cf-109">Use D3D\_SDK\_VERSION.</span></span> <span data-ttu-id="d71cf-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d71cf-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="d71cf-111">*D3DXSDKVersion* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="d71cf-111">*D3DXSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d71cf-112">Tipo: **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d71cf-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d71cf-113">Usare D3DX \_ SDK \_ VERSION.</span><span class="sxs-lookup"><span data-stu-id="d71cf-113">Use D3DX\_SDK\_VERSION.</span></span> <span data-ttu-id="d71cf-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="d71cf-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d71cf-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="d71cf-115">Return value</span></span>

<span data-ttu-id="d71cf-116">Tipo: **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d71cf-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d71cf-117">Restituisce **TRUE** se la versione di D3DX compilata è la versione in esecuzione. In caso contrario, **viene** restituito FALSE.</span><span class="sxs-lookup"><span data-stu-id="d71cf-117">Returns **TRUE** if the version of D3DX you compiled against is the version you are running with; otherwise, **FALSE** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="d71cf-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="d71cf-118">Remarks</span></span>

<span data-ttu-id="d71cf-119">Usare questa funzione durante l'inizializzazione dell'applicazione in questo modo:</span><span class="sxs-lookup"><span data-stu-id="d71cf-119">Use this function during the initialization of your application like this:</span></span>


```
HRESULT CD3DXMyApplication::Initialize(HINSTANCE hInstance, 
  LPCSTR szWindowName, LPCSTR szClassName, UINT uWidth, UINT uHeight)
{
    HRESULT hr;
    
    if (!D3DXCheckVersion(D3D_SDK_VERSION, D3DX_SDK_VERSION))
        return E_FAIL;
    
    ...
}
```



<span data-ttu-id="d71cf-120">Usare [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) per verificare che sia installato il runtime corretto.</span><span class="sxs-lookup"><span data-stu-id="d71cf-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) to verify that the correct runtime is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="d71cf-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="d71cf-121">Requirements</span></span>



| <span data-ttu-id="d71cf-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d71cf-122">Requirement</span></span> | <span data-ttu-id="d71cf-123">Valore</span><span class="sxs-lookup"><span data-stu-id="d71cf-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d71cf-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="d71cf-124">Header</span></span><br/>  | <dl> <span data-ttu-id="d71cf-125"><dt>D3dx9core.h</dt></span><span class="sxs-lookup"><span data-stu-id="d71cf-125"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="d71cf-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="d71cf-126">Library</span></span><br/> | <dl> <span data-ttu-id="d71cf-127"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="d71cf-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d71cf-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="d71cf-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d71cf-129">Per utilizzo generico funzioni</span><span class="sxs-lookup"><span data-stu-id="d71cf-129">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
