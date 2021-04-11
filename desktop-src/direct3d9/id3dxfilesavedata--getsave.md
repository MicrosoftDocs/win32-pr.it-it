---
description: Recupera un puntatore a questo nodo dati del file ID3DXFileSaveObject.
ms.assetid: 092d1c6f-0a53-4b8e-84ec-bc76f3f647ac
title: 'Metodo ID3DXFileSaveData:: getsave (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData.GetSave
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 4e23296ad0a866a0ad289a9a587c433411ef9bb8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235195"
---
# <a name="id3dxfilesavedatagetsave-method"></a><span data-ttu-id="a5f15-103">Metodo ID3DXFileSaveData:: getsave</span><span class="sxs-lookup"><span data-stu-id="a5f15-103">ID3DXFileSaveData::GetSave method</span></span>

<span data-ttu-id="a5f15-104">Recupera un puntatore a questo nodo dati del file [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="a5f15-104">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5f15-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="a5f15-105">Syntax</span></span>


```C++
HRESULT GetSave(
  [out] ID3DXFileSaveObject **ppObj
);
```



## <a name="parameters"></a><span data-ttu-id="a5f15-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="a5f15-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a5f15-107">*ppObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="a5f15-107">*ppObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a5f15-108">Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="a5f15-108">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="a5f15-109">Indirizzo di un puntatore a un'interfaccia [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) che rappresenta questo nodo dati del file.</span><span class="sxs-lookup"><span data-stu-id="a5f15-109">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface representing this file data node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a5f15-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="a5f15-110">Return value</span></span>

<span data-ttu-id="a5f15-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a5f15-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a5f15-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a5f15-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="a5f15-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="a5f15-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5f15-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="a5f15-114">Requirements</span></span>



| <span data-ttu-id="a5f15-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="a5f15-115">Requirement</span></span> | <span data-ttu-id="a5f15-116">Valore</span><span class="sxs-lookup"><span data-stu-id="a5f15-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a5f15-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="a5f15-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a5f15-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="a5f15-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="a5f15-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="a5f15-119">Library</span></span><br/> | <dl> <span data-ttu-id="a5f15-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a5f15-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a5f15-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="a5f15-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5f15-122">ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="a5f15-122">ID3DXFileSaveData</span></span>](id3dxfilesavedata.md)
</dt> </dl>

 

 




