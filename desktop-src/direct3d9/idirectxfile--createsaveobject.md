---
description: Crea un oggetto di salvataggio. Deprecato.
ms.assetid: 50a7dbde-1dd4-4aae-a9ab-97d6f99618c0
title: Metodo IDirectXFile::CreateSaveObject (DXFile.h)
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
ms.openlocfilehash: c3646f54b1f232c6eec3e1b3d06441a8e6a7c090f784e3c4c016f7f1bcfc3b03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119491851"
---
# <a name="idirectxfilecreatesaveobject-method"></a>Metodo IDirectXFile::CreateSaveObject

Crea un oggetto di salvataggio. Deprecato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT CreateSaveObject(
  [in]          LPCSTR                  szFileName,
  [in]          DXFILEFORMAT            dwFileFormat,
  [out, retval] LPDIRECTXFILESAVEOBJECT *ppSaveObj
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*szFileName* \[ Pollici\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome del file da utilizzare per il salvataggio dei dati.

</dd> <dt>

*dwFileFormat* \[ Pollici\]
</dt> <dd>

Tipo: **[ **DXFILEFORMAT**](dxfile.md)**

Indica il formato da usare per il salvataggio del file DirectX. Questo valore può essere uno dei flag DXFILEFORMAT \_ xxx nelle [costanti DXFILE](dxfile.md). Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*ppSaveObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***

Indirizzo di un puntatore a [**un'interfaccia IDirectXFileSaveObject,**](idirectxfilesaveobject.md) che rappresenta l'oggetto di salvataggio creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADALLOC, DXFILEERR \_ BADFILE, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Dopo aver utilizzato questo metodo, usare i metodi [**dell'interfaccia IDirectXFileSaveObject**](idirectxfilesaveobject.md) per creare oggetti dati e salvare modelli o dati.

Il valore predefinito per il formato di file è DXFILEFORMAT \_ BINARY. I valori del formato di file possono essere combinati in un OR logico per creare testo compresso o file binari compressi. Se un file viene specificato sia come file binario (0) che come testo (1), verrà salvato come file di testo perché il valore sarà indistinguibile dal valore del formato del file di testo (0 + 1 = 1). Se si indica che il formato del file deve essere testo e compresso, il file verrà prima scritto come testo e quindi compresso. Tuttavia, i file di testo compressi non sono efficienti come i file di testo binari, quindi nella maggior parte dei casi è necessario indicare file binari e compressi. Se si imposta un file da comprimere senza specificare un formato, verrà restituito un file binario compresso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> <dt>

[**IDirectXFileSaveObject**](idirectxfilesaveobject.md)
</dt> </dl>

 

 
