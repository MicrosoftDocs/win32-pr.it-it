---
description: Ottiene l'interfaccia ID3DXFile dell'oggetto che ha creato questo oggetto ID3DXFileSaveObject.
ms.assetid: 79249d17-cae3-43d9-9ccb-fa804b02a353
title: 'Metodo ID3DXFileSaveObject:: GetFile (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.GetFile
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 137f8245b94bb0ebd14e81d5f73a7ba9622a4933
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401986"
---
# <a name="id3dxfilesaveobjectgetfile-method"></a><span data-ttu-id="da742-103">Metodo ID3DXFileSaveObject:: GetFile</span><span class="sxs-lookup"><span data-stu-id="da742-103">ID3DXFileSaveObject::GetFile method</span></span>

<span data-ttu-id="da742-104">Ottiene l'interfaccia [**ID3DXFile**](id3dxfile.md) dell'oggetto che ha creato questo oggetto [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="da742-104">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="da742-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="da742-105">Syntax</span></span>


```C++
HRESULT GetFile(
  [in] ID3DXFile ppFile
);
```



## <a name="parameters"></a><span data-ttu-id="da742-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="da742-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da742-107">*ppFile* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="da742-107">*ppFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da742-108">Tipo: **[ **ID3DXFile**](id3dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="da742-108">Type: **[**ID3DXFile**](id3dxfile.md)**</span></span>

<span data-ttu-id="da742-109">Indirizzo di un puntatore a un oggetto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="da742-109">Address of a pointer to an [**ID3DXFile**](id3dxfile.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da742-110">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="da742-110">Return value</span></span>

<span data-ttu-id="da742-111">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da742-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da742-112">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="da742-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="da742-113">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, e \_ nointerface, e \_ pointer.</span><span class="sxs-lookup"><span data-stu-id="da742-113">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, E\_NOINTERFACE, E\_POINTER.</span></span>

## <a name="requirements"></a><span data-ttu-id="da742-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="da742-114">Requirements</span></span>



| <span data-ttu-id="da742-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="da742-115">Requirement</span></span> | <span data-ttu-id="da742-116">Valore</span><span class="sxs-lookup"><span data-stu-id="da742-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="da742-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="da742-117">Header</span></span><br/>  | <dl> <span data-ttu-id="da742-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="da742-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="da742-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="da742-119">Library</span></span><br/> | <dl> <span data-ttu-id="da742-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da742-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="da742-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="da742-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da742-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="da742-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




