---
description: Crea un'istanza di un oggetto ID3DXFile.
ms.assetid: c086cb66-b1dc-4180-b966-e9a3b1f36f22
title: Funzione D3DXFileCreate (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXFileCreate
api_type:
- LibDef
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 36fd57d15257323e86c0068709c3c73662eb0658
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104132342"
---
# <a name="d3dxfilecreate-function"></a>D3DXFileCreate (funzione)

Crea un'istanza di un oggetto [**ID3DXFile**](id3dxfile.md) .

## <a name="syntax"></a>Sintassi


```C++
HRESULT STDAPICALLTYPE D3DXFileCreate(
   ID3DXFile **lplpDirectXFile
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*lplpDirectXFile* 
</dt> <dd>

Tipo: **[ **ID3DXFile**](id3dxfile.md)\*\***

Indirizzo di un puntatore a un'interfaccia [**ID3DXFile**](id3dxfile.md) , che rappresenta l'oggetto file con estensione x creato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Se la funzione ha esito positivo, il valore restituito è \_ OK. Se la funzione ha esito negativo, il valore restituito può essere uno dei seguenti: E \_ pointer, e \_ OutOfMemory.

## <a name="remarks"></a>Commenti

Dopo aver utilizzato questa funzione, utilizzare [**RegisterTemplates**](id3dxfile--registertemplates.md) o [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) per registrare i modelli, [**CreateEnumObject**](id3dxfile--createenumobject.md) per creare un oggetto enumeratore o [**CreateSaveObject**](id3dxfile--createsaveobject.md) per creare un oggetto Save.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Funzioni file D3DX X](dx9-graphics-reference-d3dx-x-file-functions.md)
</dt> <dt>

[**CreateEnumObject**](id3dxfile--createenumobject.md)
</dt> <dt>

[**CreateSaveObject**](id3dxfile--createsaveobject.md)
</dt> <dt>

[**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md)
</dt> <dt>

[**RegisterTemplates**](id3dxfile--registertemplates.md)
</dt> </dl>

 

 




