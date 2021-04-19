---
description: Crea un oggetto Save. Deprecato.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: 'Metodo IDirectXFile:: CreateSaveObject (DXFile. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dxof.lib
- D3dxof.dll
ms.openlocfilehash: 848010a1f701b39f5cc77a126272bc019ed01f4f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323347"
---
# <a name="idirectxfilecreatesaveobject-method"></a><span data-ttu-id="b518c-104">Metodo IDirectXFile:: CreateSaveObject</span><span class="sxs-lookup"><span data-stu-id="b518c-104">IDirectXFile::CreateSaveObject method</span></span>

<span data-ttu-id="b518c-105">Crea un oggetto Save.</span><span class="sxs-lookup"><span data-stu-id="b518c-105">Creates a save object.</span></span> <span data-ttu-id="b518c-106">Deprecato.</span><span class="sxs-lookup"><span data-stu-id="b518c-106">Deprecated.</span></span>

## <a name="syntax"></a><span data-ttu-id="b518c-107">Sintassi</span><span class="sxs-lookup"><span data-stu-id="b518c-107">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="b518c-108">Parametri</span><span class="sxs-lookup"><span data-stu-id="b518c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b518c-109">*szFileName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b518c-109">*szFileName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b518c-110">Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b518c-110">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b518c-111">Puntatore al nome del file da utilizzare per il salvataggio dei dati.</span><span class="sxs-lookup"><span data-stu-id="b518c-111">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="b518c-112">*dwFileFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b518c-112">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b518c-113">Tipo: **[ **DXFILEFORMAT**](dxfile.md)**</span><span class="sxs-lookup"><span data-stu-id="b518c-113">Type: **[**DXFILEFORMAT**](dxfile.md)**</span></span>

<span data-ttu-id="b518c-114">Indica il formato da usare quando si salva il file DirectX.</span><span class="sxs-lookup"><span data-stu-id="b518c-114">Indicates the format to use when saving the DirectX file.</span></span> <span data-ttu-id="b518c-115">Questo valore può essere uno dei flag DXFILEFORMAT \_ xxx nelle [costanti DXFILE](dxfile.md).</span><span class="sxs-lookup"><span data-stu-id="b518c-115">This value can be one of the DXFILEFORMAT\_xxx flags in [DXFILE Constants](dxfile.md).</span></span> <span data-ttu-id="b518c-116">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="b518c-116">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b518c-117">*ppSaveObj* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="b518c-117">*ppSaveObj* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b518c-118">Tipo: **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span><span class="sxs-lookup"><span data-stu-id="b518c-118">Type: **[**LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***</span></span>

<span data-ttu-id="b518c-119">Indirizzo di un puntatore a un'interfaccia [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) , che rappresenta l'oggetto Salva creato.</span><span class="sxs-lookup"><span data-stu-id="b518c-119">Address of a pointer to an [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b518c-120">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="b518c-120">Return value</span></span>

<span data-ttu-id="b518c-121">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b518c-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b518c-122">Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b518c-122">If the method succeeds, the return value is DXFILE\_OK.</span></span> <span data-ttu-id="b518c-123">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADALLOC, DXFILEERR \_ BadFile, DXFILEERR \_ BADVALUE.</span><span class="sxs-lookup"><span data-stu-id="b518c-123">If the method fails, the return value can be one of the following: DXFILEERR\_BADALLOC, DXFILEERR\_BADFILE, DXFILEERR\_BADVALUE.</span></span>

## <a name="remarks"></a><span data-ttu-id="b518c-124">Commenti</span><span class="sxs-lookup"><span data-stu-id="b518c-124">Remarks</span></span>

<span data-ttu-id="b518c-125">Dopo aver utilizzato questo metodo, utilizzare i metodi dell'interfaccia [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) per creare oggetti dati e salvare modelli o dati.</span><span class="sxs-lookup"><span data-stu-id="b518c-125">After using this method, use methods of the [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="b518c-126">Il valore predefinito per il formato di file è DXFILEFORMAT \_ Binary.</span><span class="sxs-lookup"><span data-stu-id="b518c-126">The default value for the file format is DXFILEFORMAT\_BINARY.</span></span> <span data-ttu-id="b518c-127">I valori del formato di file possono essere combinati in un OR logico per creare testo compresso o file binari compressi.</span><span class="sxs-lookup"><span data-stu-id="b518c-127">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="b518c-128">Se un file viene specificato sia come binario (0) che come testo (1), verrà salvato come file di testo poiché il valore non sarà distinguibile dal valore del formato del file di testo (0 + 1 = 1).</span><span class="sxs-lookup"><span data-stu-id="b518c-128">If a file is specified as both binary (0) and text (1), it will be saved as a text file because the value will be indistinguishable from the text file format value (0 + 1 = 1).</span></span> <span data-ttu-id="b518c-129">Se si indica che il formato del file deve essere testo e compresso, il file verrà prima scritto come testo e quindi compresso.</span><span class="sxs-lookup"><span data-stu-id="b518c-129">If you indicate that the file format should be text and compressed, the file will first be written out as text and then compressed.</span></span> <span data-ttu-id="b518c-130">Tuttavia, i file di testo compressi non sono efficienti come file di testo binario, quindi nella maggior parte dei casi sarà necessario indicare il formato binario e compresso.</span><span class="sxs-lookup"><span data-stu-id="b518c-130">However, compressed text files are not as efficient as binary text files, so in most cases you will want to indicate binary and compressed.</span></span> <span data-ttu-id="b518c-131">Se si imposta un file da comprimere senza specificare un formato, verrà generato un file binario compresso.</span><span class="sxs-lookup"><span data-stu-id="b518c-131">Setting a file to be compressed without specifying a format will result in a binary, compressed file.</span></span>

## <a name="requirements"></a><span data-ttu-id="b518c-132">Requisiti</span><span class="sxs-lookup"><span data-stu-id="b518c-132">Requirements</span></span>



| <span data-ttu-id="b518c-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="b518c-133">Requirement</span></span> | <span data-ttu-id="b518c-134">Valore</span><span class="sxs-lookup"><span data-stu-id="b518c-134">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b518c-135">Intestazione</span><span class="sxs-lookup"><span data-stu-id="b518c-135">Header</span></span><br/>  | <dl> <span data-ttu-id="b518c-136"><dt>DXFile. h</dt></span><span class="sxs-lookup"><span data-stu-id="b518c-136"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="b518c-137">Libreria</span><span class="sxs-lookup"><span data-stu-id="b518c-137">Library</span></span><br/> | <dl> <span data-ttu-id="b518c-138"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b518c-138"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b518c-139">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="b518c-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b518c-140">IDirectXFile</span><span class="sxs-lookup"><span data-stu-id="b518c-140">IDirectXFile</span></span>](idirectxfile.md)
</dt> <dt>

[<span data-ttu-id="b518c-141">**IDirectXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="b518c-141">**IDirectXFileSaveObject**</span></span>](idirectxfilesaveobject.md)
</dt> </dl>

 

 
