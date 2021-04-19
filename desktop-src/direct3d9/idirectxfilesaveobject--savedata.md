---
description: Salva un oggetto dati e i relativi elementi figlio in un file DirectX. Deprecato.
ms.assetid: 18bd5ef6-9e17-4c21-bc14-373de8df9ffb
title: 'Metodo IDirectXFileSaveObject:: SaveData (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject.SaveData
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: cb901bd984e1fcd923d0ea172fb5f387b3a9302a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322530"
---
# <a name="idirectxfilesaveobjectsavedata-method"></a><span data-ttu-id="af9c7-104">Metodo IDirectXFileSaveObject:: SaveData</span><span class="sxs-lookup"><span data-stu-id="af9c7-104">IDirectXFileSaveObject::SaveData method</span></span>

<span data-ttu-id="af9c7-105">Salva un oggetto dati e i relativi elementi figlio in un file DirectX.</span><span class="sxs-lookup"><span data-stu-id="af9c7-105">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="af9c7-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="af9c7-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="af9c7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="af9c7-107">Syntax</span></span>


```C++
HRESULT SaveData(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="af9c7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="af9c7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af9c7-109">*pDataObj* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="af9c7-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af9c7-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="af9c7-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="af9c7-111">Puntatore a un'interfaccia [**IDirectXFileData**](idirectxfiledata.md) che rappresenta l'oggetto dati del file da salvare.</span><span class="sxs-lookup"><span data-stu-id="af9c7-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to save.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af9c7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="af9c7-112">Return value</span></span>

<span data-ttu-id="af9c7-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af9c7-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af9c7-114">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="af9c7-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="af9c7-115">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti: DXFILEERR \_ BADARRAYSIZE, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="af9c7-115">If the method fails, the return value can be one of the following values: DXFILEERR\_BADARRAYSIZE, DXFILEERR\_BADVALUE.</span></span>

## <a name="requirements"></a><span data-ttu-id="af9c7-116">Requisiti</span><span class="sxs-lookup"><span data-stu-id="af9c7-116">Requirements</span></span>



| <span data-ttu-id="af9c7-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="af9c7-117">Requirement</span></span> | <span data-ttu-id="af9c7-118">Valore</span><span class="sxs-lookup"><span data-stu-id="af9c7-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="af9c7-119">Intestazione</span><span class="sxs-lookup"><span data-stu-id="af9c7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="af9c7-120"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="af9c7-120"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="af9c7-121">Libreria</span><span class="sxs-lookup"><span data-stu-id="af9c7-121">Library</span></span><br/> | <dl> <span data-ttu-id="af9c7-122"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af9c7-122"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="af9c7-123">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="af9c7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af9c7-124">IDirectXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="af9c7-124">IDirectXFileSaveObject</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 




