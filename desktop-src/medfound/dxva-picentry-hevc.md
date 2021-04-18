---
description: Specifica un riferimento a una superficie non compressa.
ms.assetid: 01F9C9F9-8EB4-49D5-91F0-89B4C40DDDC8
title: Struttura DXVA_PicEntry_HEVC (DXVA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DXVA_PicEntry_HEVC
api_type:
- HeaderDef
api_location:
- dxva.h
ms.openlocfilehash: a2c4856452d0f8010e8f97126b4e660557ea40ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305392"
---
# <a name="dxva_picentry_hevc-structure"></a>\_Struttura DXVA PicEntry \_ HEVC

Specifica un riferimento a una superficie non compressa.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DXVA_PicEntry_HEVC {
  union {
    struct {
      UCHAR  Index7Bits  :7;
      UCHAR  AssociatedFlag   :1;
    };
    UCHAR  bPicEntry;
  };
} DXVA_PicEntry_HEVC, *PDXVA_PicEntry_HEVC;
```



## <a name="members"></a>Members

<dl> <dt>

**Index7Bits**
</dt> <dd>

Indice che identifica una superficie non compressa.

</dd> <dt>

**AssociatedFlag** 
</dt> <dd>

Flag a 1 bit facoltativo associato alla superficie. Il significato del flag dipende dal contesto. Ad esempio, è possibile specificare se il frame di riferimento è un riferimento a lungo termine o un riferimento a breve termine.

</dd> <dt>

**bPicEntry**
</dt> <dd>

Accede a 8 bit interi dell'Unione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1 \[ solo app desktop\]<br/>                                      |
| Server minimo supportato<br/> | Solo app desktop Windows Server 2012 R2 \[\]<br/>                           |
| Intestazione<br/>                   | <dl> <dt>DXVA. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Strutture di Media Foundation](media-foundation-structures.md)
</dt> </dl>

 

 




