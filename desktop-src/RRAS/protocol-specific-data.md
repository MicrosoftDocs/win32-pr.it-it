---
title: Struttura PROTOCOL_SPECIFIC_DATA (RTM. h)
description: La \_ \_ struttura dei dati specifica del protocollo contiene memoria riservata per i dati specifici di un determinato protocollo di routing.
ms.assetid: b6c3a342-4726-4f7b-9511-dbe1393faf98
keywords:
- RAS struttura PROTOCOL_SPECIFIC_DATA
- RAS puntatore alla struttura PPROTOCOL_SPECIFIC_DATA
topic_type:
- apiref
api_name:
- PROTOCOL_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3162aa377c051f6b329e993dfaca3bed17fae780
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103742191"
---
# <a name="protocol_specific_data-structure"></a>\_ \_ Struttura dei dati specifici del protocollo

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La **struttura \_ \_ dei dati specifica del protocollo** contiene memoria riservata per i dati specifici di un determinato protocollo di routing.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _PROTOCOL_SPECIFIC_DATA {
  DWORD PSD_Data[4];
} PROTOCOL_SPECIFIC_DATA, *PPROTOCOL_SPECIFIC_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**\_Dati PSD**
</dt> <dd>

Specifica una matrice di variabili **DWORD** . Questa memoria è riservata ai dati specifici dei protocolli di routing.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>RTM. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Riferimento di gestione tabelle di routing versione 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Strutture di gestione tabelle di routing versione 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**\_route IP \_ RTM**](rtm-ip-route.md)
</dt> <dt>

[**\_Route IPX \_ RTM**](rtm-ipx-route.md)
</dt> </dl>

 

 





