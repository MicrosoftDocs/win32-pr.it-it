---
description: Crea un oggetto Save che verrà utilizzato per salvare i dati in un file con estensione x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: 'Metodo ID3DXFile:: CreateSaveObject (D3DX9Xof. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile.CreateSaveObject
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d7c5b3de020ad50abfd8834aabbdc8e6e848d71d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323073"
---
# <a name="id3dxfilecreatesaveobject-method"></a><span data-ttu-id="5c4b5-103">Metodo ID3DXFile:: CreateSaveObject</span><span class="sxs-lookup"><span data-stu-id="5c4b5-103">ID3DXFile::CreateSaveObject method</span></span>

<span data-ttu-id="5c4b5-104">Crea un oggetto Save che verrà utilizzato per salvare i dati in un file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-104">Creates a save object that will be used to save data to a .x file.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c4b5-105">Sintassi</span><span class="sxs-lookup"><span data-stu-id="5c4b5-105">Syntax</span></span>


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a><span data-ttu-id="5c4b5-106">Parametri</span><span class="sxs-lookup"><span data-stu-id="5c4b5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c4b5-107">*pData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c4b5-107">*pData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4b5-108">Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4b5-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5c4b5-109">Puntatore al nome del file da utilizzare per il salvataggio dei dati.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-109">Pointer to the name of the file to use for saving data.</span></span>

</dd> <dt>

<span data-ttu-id="5c4b5-110">*flag* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c4b5-110">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4b5-111">Tipo: **[D3DXF \_ FILESAVEOPTIONS](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4b5-111">Type: **[D3DXF\_FILESAVEOPTIONS](d3dxf.md)**</span></span>

<span data-ttu-id="5c4b5-112">Valore che specifica il nome del file in cui salvare i dati.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-112">Value that specifies the name of the file to which data is to be saved.</span></span> <span data-ttu-id="5c4b5-113">Questo valore può essere uno dei flag di [Opzioni di salvataggio file](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="5c4b5-113">This value can be one of the [File Save Options](d3dxf.md) flags.</span></span>

</dd> <dt>

<span data-ttu-id="5c4b5-114">*dwFileFormat* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="5c4b5-114">*dwFileFormat* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4b5-115">Tipo: **[D3DXF \_ FileFormat](d3dxf.md)**</span><span class="sxs-lookup"><span data-stu-id="5c4b5-115">Type: **[D3DXF\_FILEFORMAT](d3dxf.md)**</span></span>

<span data-ttu-id="5c4b5-116">Indica il formato da utilizzare per il salvataggio del file con estensione x.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-116">Indicates the format to use when saving the .x file.</span></span> <span data-ttu-id="5c4b5-117">Questo valore può essere uno dei flag dei [formati di file](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="5c4b5-117">This value can be one of the [File Formats](d3dxf.md) flags.</span></span> <span data-ttu-id="5c4b5-118">Per altre informazioni, vedere la sezione Osservazioni.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-118">For more information, see Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="5c4b5-119">*ppSaveObj* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5c4b5-119">*ppSaveObj* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c4b5-120">Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="5c4b5-120">Type: **[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***</span></span>

<span data-ttu-id="5c4b5-121">Indirizzo di un puntatore a un'interfaccia [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , che rappresenta l'oggetto Salva creato.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-121">Address of a pointer to an [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface, representing the created save object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c4b5-122">Valore restituito</span><span class="sxs-lookup"><span data-stu-id="5c4b5-122">Return value</span></span>

<span data-ttu-id="5c4b5-123">Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5c4b5-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5c4b5-124">Se il metodo ha esito positivo, il valore restituito è \_ OK.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-124">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="5c4b5-125">Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-125">If the method fails, the return value can be one of the following: D3DXFERR\_BADVALUE, D3DXFERR\_PARSEERROR.</span></span>

## <a name="remarks"></a><span data-ttu-id="5c4b5-126">Commenti</span><span class="sxs-lookup"><span data-stu-id="5c4b5-126">Remarks</span></span>

<span data-ttu-id="5c4b5-127">Dopo aver utilizzato questo metodo, utilizzare i metodi dell'interfaccia [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) per creare oggetti dati e salvare modelli o dati.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-127">After using this method, use methods of the [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interface to create data objects and to save templates or data.</span></span>

<span data-ttu-id="5c4b5-128">Per il formato di file salvato *dwFileFormat*, è necessario specificare uno dei flag binari, binari legacy o di testo nei [formati di file](d3dxf.md) .</span><span class="sxs-lookup"><span data-stu-id="5c4b5-128">For the saved file format *dwFileFormat*, one of the binary, legacy binary, or text flags in [File Formats](d3dxf.md) must be specified.</span></span> <span data-ttu-id="5c4b5-129">Il file può essere compresso usando il \_ flag facoltativo FileFormat \_ compresso D3DXF.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-129">The file can be compressed by using the optional D3DXF\_FILEFORMAT\_COMPRESSED flag.</span></span>

<span data-ttu-id="5c4b5-130">I valori del formato di file possono essere combinati in un OR logico per creare testo compresso o file binari compressi.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-130">The file format values can be combined in a logical OR to create compressed text or compressed binary files.</span></span> <span data-ttu-id="5c4b5-131">Se si indica che il formato del file deve essere testo e compresso, il file verrà scritto prima come testo e quindi compresso.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-131">If you indicate that the file format should be text and compressed, the file will be written out first as text and then compressed.</span></span> <span data-ttu-id="5c4b5-132">Tuttavia, i file di testo compressi non sono efficienti come file di testo binario; nella maggior parte dei casi, è pertanto necessario indicare il formato binario e compresso.</span><span class="sxs-lookup"><span data-stu-id="5c4b5-132">However, compressed text files are not as efficient as binary text files; in most cases, therefore, you will want to indicate binary and compressed.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c4b5-133">Requisiti</span><span class="sxs-lookup"><span data-stu-id="5c4b5-133">Requirements</span></span>



| <span data-ttu-id="5c4b5-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="5c4b5-134">Requirement</span></span> | <span data-ttu-id="5c4b5-135">Valore</span><span class="sxs-lookup"><span data-stu-id="5c4b5-135">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="5c4b5-136">Intestazione</span><span class="sxs-lookup"><span data-stu-id="5c4b5-136">Header</span></span><br/>  | <dl> <span data-ttu-id="5c4b5-137"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c4b5-137"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="5c4b5-138">Libreria</span><span class="sxs-lookup"><span data-stu-id="5c4b5-138">Library</span></span><br/> | <dl> <span data-ttu-id="5c4b5-139"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="5c4b5-139"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="5c4b5-140">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="5c4b5-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c4b5-141">ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="5c4b5-141">ID3DXFile</span></span>](id3dxfile.md)
</dt> <dt>

[<span data-ttu-id="5c4b5-142">**ID3DXFileSaveObject**</span><span class="sxs-lookup"><span data-stu-id="5c4b5-142">**ID3DXFileSaveObject**</span></span>](id3dxfilesaveobject.md)
</dt> </dl>

 

 
