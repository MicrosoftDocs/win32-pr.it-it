---
description: Consente di creare un pacchetto delle informazioni sul tipo di oggetto, sulla versione e sulle dimensioni necessarie in molte strutture NDIS 6.0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: NDIS_OBJECT_HEADER struttura (Ntddndis.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NDIS_OBJECT_HEADER
api_type:
- HeaderDef
api_location:
- ntddndis.h
ms.openlocfilehash: f9f4a4ef2a833081cde0c3c7ca4d395e59743944291a95d7680c241191988b35
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065051"
---
# <a name="ndis_object_header-structure"></a>Struttura NDIS \_ OBJECT \_ HEADER

La **struttura NDIS \_ OBJECT \_ HEADER** contiene le informazioni sul tipo di oggetto, sulla versione e sulle dimensioni necessarie in molte strutture NDIS 6.0.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _NDIS_OBJECT_HEADER {
  UCHAR  Type;
  UCHAR  Revision;
  USHORT Size;
} NDIS_OBJECT_HEADER, *PNDIS_OBJECT_HEADER;
```



## <a name="members"></a>Members

<dl> <dt>

**Tipo**
</dt> <dd>

Specifica il tipo di oggetto NDIS descritto da una struttura.

</dd> <dt>

**Revisione**
</dt> <dd>

Specifica il numero di revisione di questa struttura.

</dd> <dt>

**Dimensioni**
</dt> <dd>

Specifica le dimensioni totali, in byte, della struttura NDIS che contiene **l'intestazione NDIS \_ OBJECT \_**. Queste dimensioni includono le dimensioni del membro **NDIS \_ OBJECT \_ HEADER** e di tutti gli altri membri della struttura.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                                       |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Ntddndis.h (includere Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**DOT11 \_ BSSID \_ LIST**](dot11-bssid-list.md)
</dt> </dl>

 

 




