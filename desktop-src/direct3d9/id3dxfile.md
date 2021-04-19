---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFile per creare istanze delle interfacce ID3DXFileEnumObject e ID3DXFileSaveObject e per registrare i modelli.
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: Interfaccia ID3DXFile (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106322989"
---
# <a name="id3dxfile-interface"></a>Interfaccia ID3DXFile

Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFile per creare istanze delle interfacce [**ID3DXFileEnumObject**](id3dxfileenumobject.md) e [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) e per registrare i modelli.

## <a name="members"></a>Membri

L'interfaccia **ID3DXFile** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFile** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXFile** dispone di questi metodi.



| Metodo                                                            | Descrizione                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [**CreateEnumObject**](id3dxfile--createenumobject.md)           | Crea un oggetto enumeratore in grado di leggere un file con estensione x.<br/>                                                      |
| [**CreateSaveObject**](id3dxfile--createsaveobject.md)           | Crea un oggetto Save che verrà utilizzato per salvare i dati in un file con estensione x.<br/>                                          |
| [**RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) | Registra i modelli personalizzati, dato un oggetto di enumerazione [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .<br/> |
| [**RegisterTemplates**](id3dxfile--registertemplates.md)         | Registra i modelli personalizzati.<br/>                                                                                 |



 

## <a name="remarks"></a>Commenti

Un oggetto ID3DXFile contiene anche un archivio di modelli locale. Questa risorsa di archiviazione locale può essere aggiunta solo a con i metodi [**ID3DXFile:: RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) e [**ID3DXFile:: RegisterTemplates**](id3dxfile--registertemplates.md) .

Gli oggetti [**ID3DXFileEnumObject**](id3dxfileenumobject.md) e [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) creati con [**ID3DXFile:: CreateEnumObject**](id3dxfile--createenumobject.md) e [**ID3DXFile:: CreateSaveObject**](id3dxfile--createsaveobject.md) usano anche l'archivio dei modelli dell'oggetto ID3DXFile padre.

L'interfaccia ID3DXFile viene ottenuta chiamando la funzione [**D3DXFileCreate**](d3dxfilecreate.md) .

L'identificatore univoco globale (GUID) per l'interfaccia ID3DXFile è IID \_ ID3DXFile.

Il tipo LPD3DXFILE è definito come puntatore all'interfaccia ID3DXFile.


```
typedef interface ID3DXFile *LPD3DXFILE;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX9Xof. h</dt> </dl> |
| Libreria<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce di file D3DX X](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
