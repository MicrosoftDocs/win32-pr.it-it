---
description: Oggetto caricamento dati utilizzato dall'interfaccia ID3DX10ThreadPump per il caricamento asincrono dei dati.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Interfaccia ID3DX10DataLoader (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10DataLoader
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: b0e45d24d663f0ba9a8978bc251a4adf0c7868fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/15/2021
ms.locfileid: "103969368"
---
# <a name="id3dx10dataloader-interface"></a>Interfaccia ID3DX10DataLoader

Oggetto caricamento dati utilizzato dall' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per il caricamento asincrono dei dati.

## <a name="members"></a>Membri

L'interfaccia **ID3DX10DataLoader** eredita dall'interfaccia [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DX10DataLoader** dispone anche di questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

L'interfaccia **ID3DX10DataLoader** dispone di questi metodi.



| Metodo                                             | Descrizione                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Decomprimere**](id3dx10dataloader-decompress.md) | Utilizzato per decomprimere i dati codificati. Questa operazione viene in genere utilizzata per caricare le risorse da file System, ad esempio file ZIP. Quando si esegue il caricamento da una risorsa non compressa, la fase di decompressione non deve eseguire alcuna operazione.<br/> |
| [**Eliminare**](id3dx10dataloader-destroy.md)       | Usato da un' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per eliminare il caricatore dopo il completamento di un elemento di lavoro.<br/>                                                                                                   |
| [**Caricamento**](id3dx10dataloader-load.md)             | Usato da un' [**interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per caricare i dati da un disco.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Questo oggetto può essere ereditato e i relativi membri ridefiniti. Questa operazione consente di personalizzare l'API per il caricamento e la decompressione dei formati di file personalizzati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
