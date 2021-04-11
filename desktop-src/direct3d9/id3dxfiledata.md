---
description: Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileData per compilare o accedere alla gerarchia immediata dell'oggetto dati. Le restrizioni del modello determinano la gerarchia.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: Interfaccia ID3DXFileData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "104235100"
---
# <a name="id3dxfiledata-interface"></a>Interfaccia ID3DXFileData

Le applicazioni utilizzano i metodi dell'interfaccia ID3DXFileData per compilare o accedere alla gerarchia immediata dell'oggetto dati. Le restrizioni del modello determinano la gerarchia.

## <a name="members"></a>Membri

L'interfaccia **ID3DXFileData** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXFileData** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DXFileData** dispone di questi metodi.



| Metodo                                            | Descrizione                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**GetChild**](id3dxfiledata--getchild.md)       | Recupera un oggetto figlio in questo oggetto dati del file.<br/>                                                        |
| [**GetChildren**](id3dxfiledata--getchildren.md) | Recupera il numero di elementi figlio in questo oggetto dati del file.<br/>                                                |
| [**Getenum**](id3dxfiledata--getenum.md)         | Recupera l'oggetto di enumerazione in questo oggetto dati del file.<br/>                                                |
| [**GetId**](id3dxfiledata--getid.md)             | Recupera il GUID di questo oggetto dati file.<br/>                                                              |
| [**GetName**](id3dxfiledata--getname.md)         | Recupera il nome di questo oggetto dati file.<br/>                                                              |
| [**GetType**](id3dxfiledata--gettype.md)         | Recupera l'ID modello in questo oggetto dati file.<br/>                                                       |
| [**IsReference**](id3dxfiledata--isreference.md) | Indica se questo oggetto dati del file è un oggetto di riferimento che punta a un altro oggetto dati figlio.<br/>   |
| [**Lock**](id3dxfiledata--lock.md)               | Accede ai dati del file con estensione x.<br/>                                                                                |
| [**Sblocca**](id3dxfiledata--unlock.md)           | Termina la durata del puntatore *ppData* restituito da [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).<br/> |



 

## <a name="remarks"></a>Commenti

I tipi di dati consentiti dal modello vengono denominati membri facoltativi. I membri facoltativi non sono obbligatori, ma un oggetto potrebbe perdere informazioni importanti senza di esse. Questi membri facoltativi vengono salvati come elementi figlio dell'oggetto dati. Un elemento figlio può essere un altro oggetto dati o un riferimento a un oggetto dati precedente.

Il GUID per l'interfaccia ID3DXFileData è IID \_ ID3DXFileData.

Il tipo LPD3DXFILEDATA è definito come puntatore a questa interfaccia.


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
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

 

 
