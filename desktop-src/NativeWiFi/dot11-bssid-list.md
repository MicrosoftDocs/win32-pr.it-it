---
description: Contiene un elenco di identificatori del set di servizi di base (BSS).
ms.assetid: 22907f94-1ae8-4938-a816-b406656256c0
title: Struttura DOT11_BSSID_LIST (Windot11. h)
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
ms.openlocfilehash: 345053a8d39ea37bea2fa2350dcc426420aed422
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313765"
---
# <a name="dot11_bssid_list-structure"></a>\_Struttura DOT11 BSSID \_ List

La struttura dell' **\_ \_ elenco BSSID di DOT11** contiene un elenco di identificatori del set di servizi di base (BSS).

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

Struttura [**di \_ \_ intestazione di un oggetto NDIS**](ndis-object-header.md) che contiene le informazioni sul tipo, la versione e le dimensioni di una struttura NDIS. Per la maggior parte delle strutture **DOT11 \_ BSSID \_ List** , impostare il membro del **tipo** su **tipo di \_ oggetto NDIS \_ \_ default**, impostare il membro **Revisione** su **DOT11 \_ BSSID \_ List \_ Revision \_ 1** e impostare il membro **size** su **sizeof (DOT11 \_ BSSID \_ List)**.

</dd> <dt>

**uNumOfEntries**
</dt> <dd>

Numero di voci nella struttura.

</dd> <dt>

**uTotalNumOfEntries**
</dt> <dd>

Il numero totale di voci supportate.

</dd> <dt>

**BSSIDs**
</dt> <dd>

Elenco di identificatori BSS. Un identificatore BSS viene archiviato come tipo [**di \_ \_ indirizzo Mac DOT11**](dot11-mac-address-type.md) .

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows XP con \[ solo app desktop SP3\]<br/>                                        |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                                       |
| Componente ridistribuibile<br/>          | API LAN wireless per Windows XP con SP2<br/>                                                        |
| Intestazione<br/>                   | <dl> <dt>Windot11. h (include Windot11. h)</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_parametri di connessione WLAN \_**](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> </dl>

 

 




