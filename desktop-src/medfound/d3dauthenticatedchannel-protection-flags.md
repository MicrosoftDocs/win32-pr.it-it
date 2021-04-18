---
description: Specifica il livello di protezione per il contenuto video.
ms.assetid: 681c6ad9-cf55-47e4-bbb9-e7fdc499a709
title: Struttura D3DAUTHENTICATEDCHANNEL_PROTECTION_FLAGS (D3d9types. h)
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
ms.openlocfilehash: 2d3111d01f178be3128dcb79f65d2155195c2e4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305450"
---
# <a name="d3dauthenticatedchannel_protection_flags-structure"></a>Struttura di flag di \_ protezione D3DAUTHENTICATEDCHANNEL \_

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

Se è 1, la protezione del contenuto video è abilitata.

</dd> <dt>

**OverlayOrFullscreenRequired**
</dt> <dd>

Se è 1, l'applicazione richiede che il video venga visualizzato utilizzando una sovrapposizione hardware o una modalità esclusiva a schermo intero.

</dd> <dt>

**Reserved**
</dt> <dd>

Riservato. Impostare tutti i bit su zero.

</dd> <dt>

**Valore**
</dt> <dd>

Utilizzare questo membro per accedere a tutti i bit nell'Unione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                             |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2008 R2 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>D3d9types. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture video Direct3D](direct3d-video-structures.md)
</dt> </dl>

 

 




