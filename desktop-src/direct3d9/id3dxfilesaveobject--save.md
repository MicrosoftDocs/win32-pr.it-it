---
description: Salva un oggetto dati e i relativi elementi figlio in un file con estensione x su disco.
ms.assetid: a48cd1b2-d1e7-446b-8482-485ccdd59353
title: 'Metodo ID3DXFileSaveObject:: Save (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject.Save
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: c97c2ccf6c509aec1d217e3179c927fe2bb5a797
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104401961"
---
# <a name="id3dxfilesaveobjectsave-method"></a><span data-ttu-id="96389-103">Metodo ID3DXFileSaveObject:: Save</span><span class="sxs-lookup"><span data-stu-id="96389-103">ID3DXFileSaveObject::Save method</span></span>

<span data-ttu-id="96389-104">Salva un oggetto dati e i relativi elementi figlio in un file con estensione x su disco.</span><span class="sxs-lookup"><span data-stu-id="96389-104">Saves a data object and its children to a .x file on disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="96389-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="96389-105">Syntax</span></span>


```C++
HRESULT Save();
```



## <a name="parameters"></a><span data-ttu-id="96389-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="96389-106">Parameters</span></span>

<span data-ttu-id="96389-107">Questo metodo non presenta parametri.</span><span class="sxs-lookup"><span data-stu-id="96389-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="96389-108">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="96389-108">Return value</span></span>

<span data-ttu-id="96389-109">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="96389-109">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="96389-110">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="96389-110">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="96389-111">Se il metodo ha esito negativo, il valore restituito può essere il seguente: D3DXFERR \_ BADOBJECT.</span><span class="sxs-lookup"><span data-stu-id="96389-111">If the method fails, the return value can be the following: D3DXFERR\_BADOBJECT.</span></span>

## <a name="remarks"></a><span data-ttu-id="96389-112">Commenti</span><span class="sxs-lookup"><span data-stu-id="96389-112">Remarks</span></span>

<span data-ttu-id="96389-113">Quando questo metodo ha esito positivo, [**ID3DXFileSaveObject:: AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData:: AddDataObject**](id3dxfilesavedata--adddataobject.md) e [**ID3DXFileSaveData:: AddDataReference**](id3dxfilesavedata--adddatareference.md) non possono più essere chiamati fino a quando non viene creato un nuovo oggetto [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="96389-113">After this method succeeds, [**ID3DXFileSaveObject::AddDataObject**](id3dxfilesaveobject--adddataobject.md), [**ID3DXFileSaveData::AddDataObject**](id3dxfilesavedata--adddataobject.md) and [**ID3DXFileSaveData::AddDataReference**](id3dxfilesavedata--adddatareference.md) can no longer be called until a new [**ID3DXFile**](id3dxfile.md) object is created.</span></span>

## <a name="requirements"></a><span data-ttu-id="96389-114">Requisiti</span><span class="sxs-lookup"><span data-stu-id="96389-114">Requirements</span></span>



| <span data-ttu-id="96389-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="96389-115">Requirement</span></span> | <span data-ttu-id="96389-116">Valore</span><span class="sxs-lookup"><span data-stu-id="96389-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="96389-117">Intestazione</span><span class="sxs-lookup"><span data-stu-id="96389-117">Header</span></span><br/>  | <dl> <span data-ttu-id="96389-118"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="96389-118"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="96389-119">Libreria</span><span class="sxs-lookup"><span data-stu-id="96389-119">Library</span></span><br/> | <dl> <span data-ttu-id="96389-120"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="96389-120"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="96389-121">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="96389-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96389-122">ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="96389-122">ID3DXFileSaveObject</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 




