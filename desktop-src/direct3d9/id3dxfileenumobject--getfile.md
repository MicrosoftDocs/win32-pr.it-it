---
description: Recupera l'oggetto ID3DXFile.
ms.assetid: 832878c6-73a4-400a-af30-57112b172977
title: 'Metodo ID3DXFileEnumObject:: GetFile (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d3b5d672ca9b462e08c75a6f3352b01b07ead43c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969410"
---
# <a name="id3dxfileenumobjectgetfile-method"></a><span data-ttu-id="fb947-103">Metodo ID3DXFileEnumObject:: GetFile</span><span class="sxs-lookup"><span data-stu-id="fb947-103">ID3DXFileEnumObject::GetFile method</span></span>

<span data-ttu-id="fb947-104">Recupera l'oggetto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="fb947-104">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb947-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="fb947-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [out] ID3DXFile **ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="fb947-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="fb947-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb947-107">*ppFile* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="fb947-107">*ppFile* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb947-108">Tipo: **[ **ID3DXFile**](id3dxfile.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="fb947-108">Type: **[**ID3DXFile**](id3dxfile.md)\*\***</span></span>

<span data-ttu-id="fb947-109">Indirizzo di un puntatore a un'interfaccia [**ID3DXFile**](id3dxfile.md) , che rappresenta l'oggetto restituito.</span><span class="sxs-lookup"><span data-stu-id="fb947-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) interface, representing the returned object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb947-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="fb947-110">Return value</span></span>

<span data-ttu-id="fb947-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb947-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb947-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb947-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="fb947-113">Se il metodo ha esito negativo, verrà restituito il valore seguente: D3DXFERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="fb947-113">If the method fails, the following value will be returned: D3DXFERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb947-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="fb947-114">Requirements</span></span>



| <span data-ttu-id="fb947-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb947-115">Requirement</span></span> | <span data-ttu-id="fb947-116">Valore</span><span class="sxs-lookup"><span data-stu-id="fb947-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="fb947-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="fb947-117">Header</span></span><br/>  | <dl> <span data-ttu-id="fb947-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb947-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="fb947-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="fb947-119">Library</span></span><br/> | <dl> <span data-ttu-id="fb947-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb947-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="fb947-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="fb947-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb947-122">ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="fb947-122">ID3DXFileEnumObject</span></span>](id3dxfileenumobject.md)
</dt> </dl>

 

 




