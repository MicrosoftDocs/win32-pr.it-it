---
description: Verificare che la versione di D3DX compilata con sia la versione in esecuzione.
ms.assetid: a4e745dd-d573-4e8f-9516-f6a7475f5cc5
title: Funzione D3DXCheckVersion (D3dx9core. h)
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
ms.openlocfilehash: 7b392d706e54780924115471906096f6b63d1a80
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323019"
---
# <a name="d3dxcheckversion-function"></a><span data-ttu-id="a1906-103">D3DXCheckVersion (funzione)</span><span class="sxs-lookup"><span data-stu-id="a1906-103">D3DXCheckVersion function</span></span>

<span data-ttu-id="a1906-104">Verificare che la versione di D3DX compilata con sia la versione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="a1906-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1906-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a1906-105">Syntax</span></span>


```C++
BOOL D3DXCheckVersion(
  _In_ UINT D3DSDKVersion,
  _In_ UINT D3DXSDKVersion
);
```



## <a name="parameters"></a><span data-ttu-id="a1906-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a1906-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1906-107">*D3DSDKVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1906-107">*D3DSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1906-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1906-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1906-109">Usare la \_ versione di D3D SDK \_ .</span><span class="sxs-lookup"><span data-stu-id="a1906-109">Use D3D\_SDK\_VERSION.</span></span> <span data-ttu-id="a1906-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a1906-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="a1906-111">*D3DXSDKVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a1906-111">*D3DXSDKVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a1906-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1906-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1906-113">Usare la \_ versione dell'SDK di D3DX \_ .</span><span class="sxs-lookup"><span data-stu-id="a1906-113">Use D3DX\_SDK\_VERSION.</span></span> <span data-ttu-id="a1906-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="a1906-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1906-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a1906-115">Return value</span></span>

<span data-ttu-id="a1906-116">Tipo: **[ **bool**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a1906-116">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a1906-117">Restituisce **true** se la versione di D3DX compilata in base a è la versione in esecuzione con; in caso contrario, viene restituito **false** .</span><span class="sxs-lookup"><span data-stu-id="a1906-117">Returns **TRUE** if the version of D3DX you compiled against is the version you are running with; otherwise, **FALSE** is returned.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1906-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="a1906-118">Remarks</span></span>

<span data-ttu-id="a1906-119">Usare questa funzione durante l'inizializzazione dell'applicazione come la seguente:</span><span class="sxs-lookup"><span data-stu-id="a1906-119">Use this function during the initialization of your application like this:</span></span>


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



<span data-ttu-id="a1906-120">Usare [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) per verificare che sia installato il runtime corretto.</span><span class="sxs-lookup"><span data-stu-id="a1906-120">Use [**Direct3DCreate9**](/windows/win32/api/d3d9/nf-d3d9-direct3dcreate9) to verify that the correct runtime is installed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1906-121">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a1906-121">Requirements</span></span>



| <span data-ttu-id="a1906-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1906-122">Requirement</span></span> | <span data-ttu-id="a1906-123">Valore</span><span class="sxs-lookup"><span data-stu-id="a1906-123">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a1906-124">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a1906-124">Header</span></span><br/>  | <dl> <span data-ttu-id="a1906-125"><dt>D3dx9core. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1906-125"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a1906-126">Libreria</span><span class="sxs-lookup"><span data-stu-id="a1906-126">Library</span></span><br/> | <dl> <span data-ttu-id="a1906-127"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1906-127"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a1906-128">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a1906-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1906-129">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="a1906-129">General Purpose Functions</span></span>](dx9-graphics-reference-d3dx-functions-general-purpose.md)
</dt> </dl>

 

 
