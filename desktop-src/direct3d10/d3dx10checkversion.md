---
description: Verificare che la versione di D3DX compilata con sia la versione in esecuzione.
ms.assetid: 57085b07-f77b-425e-a889-22c3071d7143
title: Funzione D3DX10CheckVersion (D3DX10Core. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CheckVersion
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3b41996f16cb97d91dc59f8d368f13b905992388
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323381"
---
# <a name="d3dx10checkversion-function"></a><span data-ttu-id="4c595-103">D3DX10CheckVersion (funzione)</span><span class="sxs-lookup"><span data-stu-id="4c595-103">D3DX10CheckVersion function</span></span>

<span data-ttu-id="4c595-104">Verificare che la versione di D3DX compilata con sia la versione in esecuzione.</span><span class="sxs-lookup"><span data-stu-id="4c595-104">Verify that the version of D3DX you compiled with is the version that you are running.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c595-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c595-105">Syntax</span></span>


```C++
HRESULT D3DX10CheckVersion(
  _In_ UINT D3DSdkVersion,
  _In_ UINT D3DX10SdkVersion
);
```



## <a name="parameters"></a><span data-ttu-id="4c595-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c595-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c595-107">*D3DSdkVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c595-107">*D3DSdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c595-108">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c595-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c595-109">Usare la \_ versione dell'SDK di D3D10 \_ .</span><span class="sxs-lookup"><span data-stu-id="4c595-109">Use D3D10\_SDK\_VERSION.</span></span> <span data-ttu-id="4c595-110">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4c595-110">See remarks.</span></span>

</dd> <dt>

<span data-ttu-id="4c595-111">*D3DX10SdkVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c595-111">*D3DX10SdkVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c595-112">Tipo: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c595-112">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c595-113">Usare la \_ versione dell'SDK di d3dx10 \_ .</span><span class="sxs-lookup"><span data-stu-id="4c595-113">Use D3DX10\_SDK\_VERSION.</span></span> <span data-ttu-id="4c595-114">Vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="4c595-114">See remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c595-115">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c595-115">Return value</span></span>

<span data-ttu-id="4c595-116">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c595-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c595-117">Se la versione non corrisponde, la funzione restituirà FALSE (un numero minore o uguale a 0, il numero stesso non ha significato).</span><span class="sxs-lookup"><span data-stu-id="4c595-117">If the version doesn't match, the function will return FALSE (a number less than or equal to 0, the number itself has no meaning).</span></span>

## <a name="remarks"></a><span data-ttu-id="4c595-118">Commenti</span><span class="sxs-lookup"><span data-stu-id="4c595-118">Remarks</span></span>

<span data-ttu-id="4c595-119">Usare questa funzione durante l'inizializzazione dell'applicazione.</span><span class="sxs-lookup"><span data-stu-id="4c595-119">Use this function during the initialization of your application.</span></span>


```
HRESULT hr;
    
if( FAILED( D3DX10CheckVersion(D3D10_SDK_VERSION, D3DX10_SDK_VERSION) ) )
    return E_FAIL;
```



## <a name="requirements"></a><span data-ttu-id="4c595-120">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c595-120">Requirements</span></span>



| <span data-ttu-id="4c595-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c595-121">Requirement</span></span> | <span data-ttu-id="4c595-122">Valore</span><span class="sxs-lookup"><span data-stu-id="4c595-122">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c595-123">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c595-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4c595-124"><dt>D3DX10Core. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c595-124"><dt>D3DX10Core.h</dt></span></span> </dl> |
| <span data-ttu-id="4c595-125">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c595-125">Library</span></span><br/> | <dl> <span data-ttu-id="4c595-126"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c595-126"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="4c595-127">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c595-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c595-128">Funzioni per utilizzo generico</span><span class="sxs-lookup"><span data-stu-id="4c595-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
