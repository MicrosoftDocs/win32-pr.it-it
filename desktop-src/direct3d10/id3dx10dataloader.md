---
description: Oggetto di caricamento dati usato dall'interfaccia ID3DX10ThreadPump per il caricamento asincrono dei dati.
ms.assetid: bda2414c-bbab-47ac-b23a-f58fb86e732d
title: Interfaccia ID3DX10DataLoader (D3DX10.h)
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
ms.openlocfilehash: 86da40dd581c10d9f567f6011cd3987710a9aa36e41f360dc4ffc2662f909c18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128360"
---
# <a name="id3dx10dataloader-interface"></a>Interfaccia ID3DX10DataLoader

Oggetto di caricamento dati usato [**dall'interfaccia ID3DX10ThreadPump per**](id3dx10threadpump.md) il caricamento asincrono dei dati.

## <a name="members"></a>Membri

**L'interfaccia ID3DX10DataLoader** eredita dall'interfaccia [**IUnknown.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **ID3DX10DataLoader** include anche questi tipi di membri:

-   [Metodi](#methods)

### <a name="methods"></a>Metodi

**L'interfaccia ID3DX10DataLoader** include questi metodi.



| Metodo                                             | Descrizione                                                                                                                                                                                                                        |
|:---------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Decomprimere**](id3dx10dataloader-decompress.md) | Usato per decomprimere i dati codificati. In genere viene usato per caricare le risorse dai file system, ad esempio i file ZIP. Durante il caricamento da una risorsa non compressa, la fase di decompressione non deve eseguire alcuna operazione.<br/> |
| [**Distruggere**](id3dx10dataloader-destroy.md)       | Usato da [**un'interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per eliminare il caricatore dopo il completamento di un elemento di lavoro.<br/>                                                                                                   |
| [**Caricamento**](id3dx10dataloader-load.md)             | Usato da [**un'interfaccia ID3DX10ThreadPump**](id3dx10threadpump.md) per caricare i dati da un disco.<br/>                                                                                                                            |



 

## <a name="remarks"></a>Commenti

Questo oggetto può essere ereditato e i relativi membri possono essere ridefinito. In questo modo sarà possibile personalizzare l'API per il caricamento e la decompressione di formati di file personalizzati.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|--------------------|---------------------------------------------------------------------------------------|
| Intestazione<br/>  | <dl> <dt>D3DX10.h</dt> </dl>   |
| Libreria<br/> | <dl> <dt>D3DX10.lib</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Interfacce D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
