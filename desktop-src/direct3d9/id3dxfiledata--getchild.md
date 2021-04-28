---
description: 'Metodo ID3DXFileData::GetChild: recupera un oggetto figlio in questo oggetto dati file.'
ms.assetid: 0c4f1efa-f096-443d-a482-a3c5a9138c3d
title: Metodo ID3DXFileData::GetChild (D3DX9Xof.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData.GetChild
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 7fe6c0393e5cfb9ed8aeaf5808d33175e7f9bfe5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090379"
---
# <a name="id3dxfiledatagetchild-method"></a><span data-ttu-id="6b8f9-103">Metodo ID3DXFileData::GetChild</span><span class="sxs-lookup"><span data-stu-id="6b8f9-103">ID3DXFileData::GetChild method</span></span>

<span data-ttu-id="6b8f9-104">Recupera un oggetto figlio in questo oggetto dati file.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-104">Retrieves a child object in this file data object.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b8f9-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="6b8f9-105">Syntax</span></span>


```C++
HRESULT GetChild(
  [in] SIZE_T        uiChild,
  [in] ID3DXFileData **ppChild
);
```



## <a name="parameters"></a><span data-ttu-id="6b8f9-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="6b8f9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b8f9-107">*uiChild* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6b8f9-107">*uiChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b8f9-108">Tipo: **[ **SIZE \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="6b8f9-108">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="6b8f9-109">ID dell'oggetto figlio da recuperare.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-109">ID of the child object to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="6b8f9-110">*ppChild* \[ Pollici\]</span><span class="sxs-lookup"><span data-stu-id="6b8f9-110">*ppChild* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b8f9-111">Tipo: **[ **ID3DXFileData**](id3dxfiledata.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="6b8f9-111">Type: **[**ID3DXFileData**](id3dxfiledata.md)\*\***</span></span>

<span data-ttu-id="6b8f9-112">Indirizzo di un puntatore a ricevere il puntatore a interfaccia dell'oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-112">Address of a pointer to receive the child object's interface pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b8f9-113">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="6b8f9-113">Return value</span></span>

<span data-ttu-id="6b8f9-114">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="6b8f9-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="6b8f9-115">Se il metodo ha esito positivo, il valore restituito è S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="6b8f9-116">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ NOMOREOBJECTS.</span><span class="sxs-lookup"><span data-stu-id="6b8f9-116">If the method fails, the return value can be one of the following values: D3DXFERR\_BADVALUE, D3DXFERR\_NOMOREOBJECTS.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b8f9-117">Requisiti</span><span class="sxs-lookup"><span data-stu-id="6b8f9-117">Requirements</span></span>



| <span data-ttu-id="6b8f9-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6b8f9-118">Requirement</span></span> | <span data-ttu-id="6b8f9-119">Valore</span><span class="sxs-lookup"><span data-stu-id="6b8f9-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6b8f9-120">Intestazione</span><span class="sxs-lookup"><span data-stu-id="6b8f9-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6b8f9-121"><dt>D3DX9Xof.h</dt></span><span class="sxs-lookup"><span data-stu-id="6b8f9-121"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="6b8f9-122">Libreria</span><span class="sxs-lookup"><span data-stu-id="6b8f9-122">Library</span></span><br/> | <dl> <span data-ttu-id="6b8f9-123"><dt>D3dx9.lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b8f9-123"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="6b8f9-124">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="6b8f9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b8f9-125">ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="6b8f9-125">ID3DXFileData</span></span>](id3dxfiledata.md)
</dt> </dl>

 

 
