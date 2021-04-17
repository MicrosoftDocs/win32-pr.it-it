---
description: Aggiunge un oggetto dati come oggetto figlio. Deprecato.
ms.assetid: 43771dd6-c17f-4376-9b0a-459ba61ff4c5
title: 'Metodo IDirectXFileData:: AddDataObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData.AddDataObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 393526bb249b0337964bee0af5be1b55b8dd513e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355399"
---
# <a name="idirectxfiledataadddataobject-method"></a><span data-ttu-id="518e7-104">Metodo IDirectXFileData:: AddDataObject</span><span class="sxs-lookup"><span data-stu-id="518e7-104">IDirectXFileData::AddDataObject method</span></span>

<span data-ttu-id="518e7-105">Aggiunge un oggetto dati come oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="518e7-105">Adds a data object as a child object.</span></span> <span data-ttu-id="518e7-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="518e7-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="518e7-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="518e7-107">Syntax</span></span>


```C++
HRESULT AddDataObject(
  [in] LPDIRECTXFILEDATA pDataObj
);
```



## <a name="parameters"></a><span data-ttu-id="518e7-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="518e7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="518e7-109">*pDataObj* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="518e7-109">*pDataObj* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="518e7-110">Tipo: **[ **LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span><span class="sxs-lookup"><span data-stu-id="518e7-110">Type: **[**LPDIRECTXFILEDATA**](idirectxfiledata.md)**</span></span>

<span data-ttu-id="518e7-111">Puntatore a un'interfaccia [**IDirectXFileData**](idirectxfiledata.md) , che rappresenta l'oggetto dati del file da aggiungere come oggetto figlio.</span><span class="sxs-lookup"><span data-stu-id="518e7-111">Pointer to an [**IDirectXFileData**](idirectxfiledata.md) interface, representing the file data object to add as a child object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="518e7-112">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="518e7-112">Return value</span></span>

<span data-ttu-id="518e7-113">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="518e7-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="518e7-114">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="518e7-114">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="518e7-115">Se il metodo ha esito negativo, il valore restituito può essere uno dei valori seguenti. DXFILEERR \_ BADALLOC DXFILEERR \_ BADVALUE</span><span class="sxs-lookup"><span data-stu-id="518e7-115">If the method fails, the return value can be one of the following values.DXFILEERR\_BADALLOC DXFILEERR\_BADVALUE</span></span>

## <a name="remarks"></a><span data-ttu-id="518e7-116">Commenti</span><span class="sxs-lookup"><span data-stu-id="518e7-116">Remarks</span></span>

<span data-ttu-id="518e7-117">Usare il metodo [**IDirectXFileSaveObject:: CreateDataObject**](idirectxfilesaveobject--createdataobject.md) per creare l'oggetto [**IDirectXFileData**](idirectxfiledata.md) prima di chiamare questo metodo.</span><span class="sxs-lookup"><span data-stu-id="518e7-117">Use the [**IDirectXFileSaveObject::CreateDataObject**](idirectxfilesaveobject--createdataobject.md) method to create the [**IDirectXFileData**](idirectxfiledata.md) object before calling this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="518e7-118">Requisiti</span><span class="sxs-lookup"><span data-stu-id="518e7-118">Requirements</span></span>



| <span data-ttu-id="518e7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="518e7-119">Requirement</span></span> | <span data-ttu-id="518e7-120">Valore</span><span class="sxs-lookup"><span data-stu-id="518e7-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="518e7-121">Intestazione</span><span class="sxs-lookup"><span data-stu-id="518e7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="518e7-122"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="518e7-122"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="518e7-123">Libreria</span><span class="sxs-lookup"><span data-stu-id="518e7-123">Library</span></span><br/> | <dl> <span data-ttu-id="518e7-124"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="518e7-124"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="518e7-125">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="518e7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="518e7-126">IDirectXFileData</span><span class="sxs-lookup"><span data-stu-id="518e7-126">IDirectXFileData</span></span>](idirectxfiledata.md)
</dt> <dt>

[<span data-ttu-id="518e7-127">**IDirectXFileSaveObject::CreateDataObject**</span><span class="sxs-lookup"><span data-stu-id="518e7-127">**IDirectXFileSaveObject::CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md)
</dt> </dl>

 

 




