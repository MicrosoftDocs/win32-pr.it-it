---
description: Imposta un puntatore a una funzione di callback facoltativa che calcola la percentuale di calcoli armonici sferici (SH) completati e fornisce al chiamante la possibilità di interrompere il simulatore.
ms.assetid: 0a47610d-fa4e-4094-9adb-4fd9306b8a12
title: 'Metodo ID3DXPRTEngine:: secallback (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTEngine.SetCallBack
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e9c2cfe710bc41ff71267e381fa0bf576688f9df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322979"
---
# <a name="id3dxprtenginesetcallback-method"></a><span data-ttu-id="32ce6-103">Metodo ID3DXPRTEngine:: secallback</span><span class="sxs-lookup"><span data-stu-id="32ce6-103">ID3DXPRTEngine::SetCallBack method</span></span>

<span data-ttu-id="32ce6-104">Imposta un puntatore a una funzione di callback facoltativa che calcola la percentuale di calcoli armonici sferici (SH) completati e fornisce al chiamante la possibilità di interrompere il simulatore.</span><span class="sxs-lookup"><span data-stu-id="32ce6-104">Sets a pointer to an optional callback function that computes the percentage of spherical harmonic (SH) computations completed and gives the caller the option of aborting the simulator.</span></span>

## <a name="syntax"></a><span data-ttu-id="32ce6-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32ce6-105">Syntax</span></span>


```C++
HRESULT SetCallBack(
  [in] LPD3DXSHPRTSIMCB pCB,
  [in] FLOAT            Frequency,
  [in] LPVOID           lpUserContext
);
```



## <a name="parameters"></a><span data-ttu-id="32ce6-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="32ce6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ce6-107">*pCB* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32ce6-107">*pCB* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32ce6-108">Tipo: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span><span class="sxs-lookup"><span data-stu-id="32ce6-108">Type: **[LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md)**</span></span>

<span data-ttu-id="32ce6-109">Puntatore alla funzione di callback [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) che calcola la percentuale di calcoli SH completati.</span><span class="sxs-lookup"><span data-stu-id="32ce6-109">Pointer to the [LPD3DXSHPRTSIMCB](lpd3dxshprtsimcb.md) callback function that computes the percentage of SH computations completed.</span></span> <span data-ttu-id="32ce6-110">La funzione di callback deve essere implementata per restituire S \_ OK per tenere in esecuzione il simulatore.</span><span class="sxs-lookup"><span data-stu-id="32ce6-110">The callback function must be implemented to return S\_OK to keep running the simulator.</span></span> <span data-ttu-id="32ce6-111">Qualsiasi altro valore interrompe il simulatore.</span><span class="sxs-lookup"><span data-stu-id="32ce6-111">Any other value will abort the simulator.</span></span>

</dd> <dt>

<span data-ttu-id="32ce6-112">*Frequenza* \[ di in\]</span><span class="sxs-lookup"><span data-stu-id="32ce6-112">*Frequency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32ce6-113">Tipo: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32ce6-113">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32ce6-114">Frequenza delle chiamate di callback.</span><span class="sxs-lookup"><span data-stu-id="32ce6-114">Frequency of callback calls.</span></span> <span data-ttu-id="32ce6-115">L'inverso della frequenza è approssimativamente il numero di volte in cui la funzione di callback verrà chiamata.</span><span class="sxs-lookup"><span data-stu-id="32ce6-115">The inverse of Frequency is approximately the number of times the callback function will be called.</span></span>

</dd> <dt>

<span data-ttu-id="32ce6-116">*lpUserContext* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="32ce6-116">*lpUserContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32ce6-117">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="32ce6-117">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="32ce6-118">Puntatore a un valore definito dall'utente che viene passato alla funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="32ce6-118">Pointer to a user-defined value which is passed to the callback function.</span></span> <span data-ttu-id="32ce6-119">Usato in genere da un'applicazione per passare un puntatore a una struttura di dati che fornisce informazioni sul contesto per la funzione di callback.</span><span class="sxs-lookup"><span data-stu-id="32ce6-119">Typically used by an application to pass a pointer to a data structure that provides context information for the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ce6-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="32ce6-120">Return value</span></span>

<span data-ttu-id="32ce6-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="32ce6-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="32ce6-122">Il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="32ce6-122">The return value is S\_OK.</span></span>

## <a name="requirements"></a><span data-ttu-id="32ce6-123">Requisiti</span><span class="sxs-lookup"><span data-stu-id="32ce6-123">Requirements</span></span>



| <span data-ttu-id="32ce6-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="32ce6-124">Requirement</span></span> | <span data-ttu-id="32ce6-125">Valore</span><span class="sxs-lookup"><span data-stu-id="32ce6-125">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="32ce6-126">Intestazione</span><span class="sxs-lookup"><span data-stu-id="32ce6-126">Header</span></span><br/>  | <dl> <span data-ttu-id="32ce6-127"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="32ce6-127"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="32ce6-128">Libreria</span><span class="sxs-lookup"><span data-stu-id="32ce6-128">Library</span></span><br/> | <dl> <span data-ttu-id="32ce6-129"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="32ce6-129"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="32ce6-130">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="32ce6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ce6-131">ID3DXPRTEngine</span><span class="sxs-lookup"><span data-stu-id="32ce6-131">ID3DXPRTEngine</span></span>](id3dxprtengine.md)
</dt> </dl>

 

 
