---
description: Pacchetti le informazioni sul tipo di oggetto, sulla versione e sulle dimensioni richieste in molte strutture NDIS 6,0.
ms.assetid: 0dfb6022-1d8d-4bd9-bde3-2ee6d683f223
title: Struttura NDIS_OBJECT_HEADER (Ntddndis. h)
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
ms.openlocfilehash: fe28a87eeb1457bace0b72a386bcb07667b24a64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311681"
---
# <a name="ndis_object_header-structure"></a>Struttura dell'intestazione dell' \_ oggetto NDIS \_

La struttura dell' **\_ \_ intestazione dell'oggetto NDIS** impacca le informazioni sul tipo di oggetto, sulla versione e sulle dimensioni necessarie in molte strutture NDIS 6,0.

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

Specifica il numero di revisione della struttura.

</dd> <dt>

**Dimensioni**
</dt> <dd>

Specifica la dimensione totale, in byte, della struttura NDIS che contiene l' **intestazione dell' \_ oggetto \_ NDIS**. Questa dimensione include le dimensioni del membro **dell' \_ \_ intestazione dell'oggetto NDIS** e di tutti gli altri membri della struttura.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                       |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Ntddndis. h (include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_Elenco BSSID \_ DOT11**](dot11-bssid-list.md)
</dt> </dl>

 

 




