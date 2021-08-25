---
description: Crea un oggetto di salvataggio che verrà usato per salvare i dati in un file con estensione x.
ms.assetid: da064e83-605f-4c86-985d-9a0961c18e01
title: Metodo ID3DXFile::CreateSaveObject (D3DX9Xof.h)
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
ms.openlocfilehash: aaf9f884a651182429de20fe261a250c8c6567eacd99d635213682e4d755b79a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951611"
---
# <a name="id3dxfilecreatesaveobject-method"></a>Metodo ID3DXFile::CreateSaveObject

Crea un oggetto di salvataggio che verrà usato per salvare i dati in un file con estensione x.

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

*pData* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCVOID**](../winprog/windows-data-types.md)**

Puntatore al nome del file da utilizzare per il salvataggio dei dati.

</dd> <dt>

*flag* \[ Pollici\]
</dt> <dd>

Tipo: **[ \_ FILESAVEOPTIONS D3DXF](d3dxf.md)**

Valore che specifica il nome del file in cui devono essere salvati i dati. Questo valore può essere uno dei flag [Opzioni di salvataggio](d3dxf.md) file.

</dd> <dt>

*dwFileFormat* \[ Pollici\]
</dt> <dd>

Tipo: **[D3DXF \_ FILEFORMAT](d3dxf.md)**

Indica il formato da utilizzare per il salvataggio del file con estensione x. Questo valore può essere uno dei flag [formati di](d3dxf.md) file. Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*ppSaveObj* \[ Cambio\]
</dt> <dd>

Tipo: **[ **ID3DXFileSaveObject**](id3dxfilesaveobject.md)\*\***

Indirizzo di un puntatore a [**un'interfaccia ID3DXFileSaveObject,**](id3dxfilesaveobject.md) che rappresenta l'oggetto di salvataggio creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è S \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: D3DXFERR \_ BADVALUE, D3DXFERR \_ PARSEERROR.

## <a name="remarks"></a>Commenti

Dopo aver utilizzato questo metodo, usare i metodi [**dell'interfaccia ID3DXFileSaveObject**](id3dxfilesaveobject.md) per creare oggetti dati e salvare modelli o dati.

Per il formato di file *salvato dwFileFormat,* è necessario specificare uno dei flag binario, binario legacy [o](d3dxf.md) di testo nei formati di file. Il file può essere compresso usando il flag D3DXF \_ FILEFORMAT \_ COMPRESSED facoltativo.

I valori del formato di file possono essere combinati in un OR logico per creare testo compresso o file binari compressi. Se si indica che il formato del file deve essere testo e compresso, il file verrà scritto prima come testo e quindi compresso. Tuttavia, i file di testo compressi non sono efficienti come i file di testo binari. nella maggior parte dei casi, pertanto, è necessario indicare file binari e compressi.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof.h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9.lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[ID3DXFile](id3dxfile.md)
</dt> <dt>

[**ID3DXFileSaveObject**](id3dxfilesaveobject.md)
</dt> </dl>

 

 
