---
description: Specifica il livello di protezione per il contenuto video.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS struttura (D3d9types.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 1d1b76a6fea0dd6b966bd72001efb187a7a3a14e75b4d41d631e5a1ea163fe94
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118974710"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a>Struttura DEI FLAG DI PROTEZIONE D3DAUTHENTICATEDCHANNEL \_ \_

Specifica il livello di protezione per il contenuto video.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS {
  union {
    struct {
      UINT ProtectionEnabled  :1;
      UINT OverlayOrFullscreenRequired  :1;
      UINT Reserved  :30;
    };
    UINT   Value;
  };
} D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS;
```



## <a name="members"></a>Members

<dl> <dt>

**ProtectionEnabled**
</dt> <dd>

Se 1, la protezione del contenuto video è abilitata.

</dd> <dt>

**OverlayOrFullscreenRequired**
</dt> <dd>

Se 1, l'applicazione richiede che il video sia visualizzato usando una sovrimpressione hardware o la modalità esclusiva a schermo intero.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato. Impostare tutti i bit su zero.

</dd> <dt>

**Valore**
</dt> <dd>

Utilizzare questo membro per accedere a tutti i bit nell'unione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7 \[ app desktop\]<br/>                                             |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>D3d9types.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture video Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




