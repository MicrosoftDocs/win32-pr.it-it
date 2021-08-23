---
description: Contiene un elenco di identificatori BSS (Basic Service Set).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: DOT11_BSSID_LIST struttura (Windot11.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSSID_LIST
api_type:
- HeaderDef
api_location:
- windot11.h
ms.openlocfilehash: 8abcd2e711d5598c59bb8d4b7aed0f291364f94d04ec17a5fc80de2fd32939eb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119801391"
---
# <a name="dot11_bssid_list-structure"></a>Struttura DOT11 \_ BSSID \_ LIST

La **struttura DOT11 \_ BSSID \_ LIST** contiene un elenco di identificatori BSS (Basic Service Set).

## <a name="syntax"></a>Sintassi


```C++
typedef struct _DOT11_BSSID_LIST {
  NDIS_OBJECT_HEADER Header;
  ULONG              uNumOfEntries;
  ULONG              uTotalNumOfEntries;
  DOT11_MAC_ADDRESS  BSSIDs[1];
} DOT11_BSSID_LIST, *PDOT11_BSSID_LIST;
```



## <a name="members"></a>Members

<dl> <dt>

**Intestazione**
</dt> <dd>

Struttura [**NDIS \_ OBJECT \_ HEADER**](ndis-object-header.md) che contiene le informazioni su tipo, versione e dimensioni di una struttura NDIS. Per la maggior parte delle strutture **\_ DOT11 BSSID \_ LIST,** impostare il membro **Type** su **NDIS \_ OBJECT \_ TYPE \_ DEFAULT,** impostare il membro **Revision** su **DOT11 \_ BSSID \_ LIST REVISION \_ \_ 1** e il membro **Size** su **sizeof(DOT11 \_ BSSID \_ LIST).**

</dd> <dt>

**uNumOfEntries**
</dt> <dd>

Numero di voci nella struttura .

</dd> <dt>

**uTotalNumOfEntries**
</dt> <dd>

Numero totale di voci supportate.

</dd> <dt>

**SSID**
</dt> <dd>

Elenco di identificatori BSS. Un identificatore BSS viene archiviato come [**tipo DI \_ \_ INDIRIZZO MAC DOT11.**](dot11-mac-address-type.md)

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP solo con app desktop SP3 \[\]<br/>                                        |
| Server minimo supportato<br/> | Windows Solo app desktop di Server 2008 \[\]<br/>                                                       |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Windot11.h (includere Windot11.h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**PARAMETRI DI CONNESSIONE \_ \_ WLAN**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




