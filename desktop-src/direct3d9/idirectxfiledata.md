---
description: Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileData per compilare o accedere alla gerarchia immediata dell'oggetto dati.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Interfaccia IDirectXFileData (DXFile. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 30d2fb26e3752e302726edce51354369f3b067eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "106323229"
---
# <a name="idirectxfiledata-interface"></a>Interfaccia IDirectXFileData

Le applicazioni utilizzano i metodi dell'interfaccia IDirectXFileData per compilare o accedere alla gerarchia immediata dell'oggetto dati. Le restrizioni del modello determinano la gerarchia. I tipi di dati consentiti dal modello vengono denominati membri facoltativi. I membri facoltativi non sono obbligatori, ma un oggetto potrebbe perdere informazioni importanti senza di esse. Questi membri facoltativi vengono salvati come elementi figlio dell'oggetto dati. Gli elementi figlio possono essere un altro oggetto dati, un riferimento a un oggetto dati precedente o un oggetto binario. Deprecato.

## <a name="members"></a>Membri

L'interfaccia **IDirectXFileData** eredita da [**IDirectXFileObject**](idirectxfileobject.md). **IDirectXFileData** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **IDirectXFileData** dispone di questi metodi.



| Metodo                                                         | Descrizione                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [**AddBinaryObject**](idirectxfiledata--addbinaryobject.md)   | Crea un oggetto binario e lo aggiunge come oggetto figlio. Deprecato.<br/>                                             |
| [**AddDataObject**](idirectxfiledata--adddataobject.md)       | Aggiunge un oggetto dati come oggetto figlio. Deprecato.<br/>                                                              |
| [**AddDataReference**](idirectxfiledata--adddatareference.md) | Crea e aggiunge un oggetto riferimento ai dati come oggetto figlio. Deprecato.<br/>                                        |
| [**GetData**](idirectxfiledata--getdata.md)                   | Recupera i dati per uno dei membri dell'oggetto o i dati per tutti i membri. Deprecato.<br/>                    |
| [**GetNextObject**](idirectxfiledata--getnextobject.md)       | Recupera il successivo oggetto dati figlio, oggetto riferimento ai dati o oggetto binario nel file DirectX. Deprecato.<br/> |
| [**GetType**](idirectxfiledata--gettype.md)                   | Recupera il GUID del modello dell'oggetto. Deprecato.<br/>                                                       |



 

## <a name="remarks"></a>Commenti

Il GUID per l'interfaccia IDirectXFileData è IID \_ IDirectXFileData.

Il tipo LPDIRECTXFILEDATA è definito come puntatore a questa interfaccia.


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>DXFile. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3dxof. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IDirectXFileObject**](idirectxfileobject.md)
</dt> <dt>

[Interfacce di file X](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




