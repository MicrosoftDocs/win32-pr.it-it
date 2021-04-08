---
description: Legge i dati binari. Deprecato.
ms.assetid: 530552c5-bf05-4e86-836d-d25161832c6d
title: 'Metodo IDirectXFileBinary:: Read (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileBinary.Read
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 60548640fbbb0e67909eab1fed2df24a3465bf95
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104058656"
---
# <a name="idirectxfilebinaryread-method"></a><span data-ttu-id="4c6bc-104">Metodo IDirectXFileBinary:: Read</span><span class="sxs-lookup"><span data-stu-id="4c6bc-104">IDirectXFileBinary::Read method</span></span>

<span data-ttu-id="4c6bc-105">Legge i dati binari.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-105">Reads the binary data.</span></span> <span data-ttu-id="4c6bc-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="4c6bc-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="4c6bc-107">Syntax</span></span>


```C++
HRESULT Read(
  [out] LPVOID  pvData,
  [in]  DWORD   cbSize,
  [out] LPDWORD pcbRead
);
```



## <a name="parameters"></a><span data-ttu-id="4c6bc-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="4c6bc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c6bc-109">*pvData* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4c6bc-109">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c6bc-110">Tipo: **[ **LPVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c6bc-110">Type: **[**LPVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c6bc-111">Puntatore al buffer che riceve i dati che sono stati letti.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-111">Pointer to the buffer that receives the data that has been read.</span></span>

</dd> <dt>

<span data-ttu-id="4c6bc-112">*cbSize* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4c6bc-112">*cbSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c6bc-113">Tipo: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c6bc-113">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c6bc-114">Dimensioni del buffer a cui punta pvData in byte.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-114">Size of the buffer pointed to by pvData, in bytes.</span></span>

</dd> <dt>

<span data-ttu-id="4c6bc-115">*pcbRead* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="4c6bc-115">*pcbRead* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4c6bc-116">Tipo: **[ **LPDWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="4c6bc-116">Type: **[**LPDWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="4c6bc-117">Puntatore al numero di byte effettivamente letti.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-117">Pointer to the number of bytes actually read.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c6bc-118">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="4c6bc-118">Return value</span></span>

<span data-ttu-id="4c6bc-119">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="4c6bc-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="4c6bc-120">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-120">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="4c6bc-121">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADVALUE, DXFILEERR \_ NOMOREDATA.</span><span class="sxs-lookup"><span data-stu-id="4c6bc-121">If the method fails, the return value can be one of the following values: DXFILEERR\_BADVALUE, DXFILEERR\_NOMOREDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c6bc-122">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4c6bc-122">Requirements</span></span>



| <span data-ttu-id="4c6bc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4c6bc-123">Requirement</span></span> | <span data-ttu-id="4c6bc-124">Valore</span><span class="sxs-lookup"><span data-stu-id="4c6bc-124">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4c6bc-125">Intestazione</span><span class="sxs-lookup"><span data-stu-id="4c6bc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4c6bc-126"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="4c6bc-126"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="4c6bc-127">Libreria</span><span class="sxs-lookup"><span data-stu-id="4c6bc-127">Library</span></span><br/> | <dl> <span data-ttu-id="4c6bc-128"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="4c6bc-128"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c6bc-129">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="4c6bc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c6bc-130">IDirectXFileBinary</span><span class="sxs-lookup"><span data-stu-id="4c6bc-130">IDirectXFileBinary</span></span>](idirectxfilebinary.md)
</dt> </dl>

 

 
