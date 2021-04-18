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
# <a name="id3dxfilecreatesaveobject-method"></a>Metodo ID3DXFile:: CreateSaveObject

Crea un oggetto Save che verrà utilizzato per salvare i dati in un file con estensione x.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateSaveObject(
  [in]  LPCVOID               pData,
  [in]  D3DXF_FILESAVEOPTIONS flags,
  [in]  D3DXF_FILEFORMAT      dwFileFormat,
  [out] ID3DXFileSaveObject   **ppSaveObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pData* \[ in\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore al nome del file da utilizzare per il salvataggio dei dati.

</dd> <dt>

*flag* \[ in\]
</dt> <dd>

Tipo: **[D3DXF \_ FILESAVEOPTIONS](d3dxf.md)**

Valore che specifica il nome del file in cui salvare i dati. Questo valore può essere uno dei flag di [Opzioni di salvataggio file](d3dxf.md) .

</dd> <dt>

*dwFileFormat* \[ in\]
</dt> <dd>

Tipo: **[D3DXF \_ FileFormat](d3dxf.md)**

Indica il formato da utilizzare per il salvataggio del file con estensione x. Questo valore può essere uno dei flag dei [formati di file](d3dxf.md) . Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*ppSaveObj* \[ out\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , che rappresenta l'oggetto Salva creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Commenti

Dopo aver utilizzato questo metodo, utilizzare i metodi dell'interfaccia [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) per creare oggetti dati e salvare modelli o dati.

Per il formato di file salvato *dwFileFormat*, è necessario specificare uno dei flag binari, binari legacy o di testo nei [formati di file](d3dxf.md) . Il file può essere compresso usando il \_ flag facoltativo FileFormat \_ compresso D3DXF.

I valori del formato di file possono essere combinati in un OR logico per creare testo compresso o file binari compressi. Se si indica che il formato del file deve essere testo e compresso, il file verrà scritto prima come testo e quindi compresso. Tuttavia, i file di testo compressi non sono efficienti come file di testo binario; nella maggior parte dei casi, è pertanto necessario indicare il formato binario e compresso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)
</dt> </dl>

 

 
