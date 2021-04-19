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
# <a name="idirectxfilecreatesaveobject-method"></a>Metodo IDirectXFile:: CreateSaveObject

Crea un oggetto Save. Deprecato.

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

*szFileName* \[ in\]
</dt> <dd>

Tipo: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Puntatore al nome del file da utilizzare per il salvataggio dei dati.

</dd> <dt>

*dwFileFormat* \[ in\]
</dt> <dd>

Tipo: **[ **DXFILEFORMAT**](dxfile.md)**

Indica il formato da usare quando si salva il file DirectX. Questo valore può essere uno dei flag DXFILEFORMAT \_ xxx nelle [costanti DXFILE](dxfile.md). Per altre informazioni, vedere la sezione Osservazioni.

</dd> <dt>

*ppSaveObj* \[ out, retval\]
</dt> <dd>

Tipo: **[ **LPDIRECTXFILESAVEOBJECT**](idirectxfilesaveobject.md)\***

Indirizzo di un puntatore a un'interfaccia [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) , che rappresenta l'oggetto Salva creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se il metodo ha esito positivo, il valore restituito è DXFILE \_ OK. Se il metodo ha esito negativo, il valore restituito può essere uno dei seguenti: DXFILEERR \_ BADALLOC, DXFILEERR \_ BadFile, DXFILEERR \_ BADVALUE.

## <a name="remarks"></a>Commenti

Dopo aver utilizzato questo metodo, utilizzare i metodi dell'interfaccia [**IDirectXFileSaveObject**](idirectxfilesaveobject.md) per creare oggetti dati e salvare modelli o dati.

Il valore predefinito per il formato di file è DXFILEFORMAT \_ Binary. I valori del formato di file possono essere combinati in un OR logico per creare testo compresso o file binari compressi. Se un file viene specificato sia come binario (0) che come testo (1), verrà salvato come file di testo poiché il valore non sarà distinguibile dal valore del formato del file di testo (0 + 1 = 1). Se si indica che il formato del file deve essere testo e compresso, il file verrà prima scritto come testo e quindi compresso. Tuttavia, i file di testo compressi non sono efficienti come file di testo binario, quindi nella maggior parte dei casi sarà necessario indicare il formato binario e compresso. Se si imposta un file da comprimere senza specificare un formato, verrà generato un file binario compresso.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[IDirectXFile](idirectxfile.md)
</dt> <dt>

[**IDirectXFileSaveObject**](idirectxfilesaveobject.md)
</dt> </dl>

 

 
