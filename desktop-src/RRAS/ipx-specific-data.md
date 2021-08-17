---
title: IPX_SPECIFIC_DATA (Rtm.h)
description: La struttura DEI DATI SPECIFICI DI IPX \_ contiene dati specifici di \_ IPX.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- IPX_SPECIFIC_DATA struttura RAS
- PIPX_SPECIFIC_DATA del puntatore della struttura RAS
topic_type:
- apiref
api_name:
- IPX_SPECIFIC_DATA
api_location:
- Rtm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0367e02dd8b0a46304538a2e5830e101eb9573e6548383fbae617a856df83621
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117790749"
---
# <a name="ipx_specific_data-structure"></a>Struttura DEI \_ DATI SPECIFICI \_ DI IPX

\[Questa API è stata sostituita dall'API di Gestione tabelle di routing versione [2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API gestione tabelle di routing versione 2.\]

La **struttura DEI DATI SPECIFICI \_ \_ DI IPX** contiene dati specifici di IPX.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _IPX_SPECIFIC_DATA {
  DWORD  FSD_Flags;
  USHORT FSD_TickCount;
  USHORT FSD_HopCount;
} IPX_SPECIFIC_DATA, *PIPX_SPECIFIC_DATA;
```



## <a name="members"></a>Members

<dl> <dt>

**Flag \_ FSD**
</dt> <dd>

Specifica i flag che descrivono la route. Attualmente, questo membro è zero o il valore del flag seguente.



| Valore                                                                                                                                                                                                      | Significato                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <dt>**ROUTE \_ WAN \_ CLIENT GLOBALE \_ \_ IPX**</dt> </dl> | Specifica che questa route è per la rete globale allocata per tutti i client WAN.<br/> |



 

</dd> <dt>

**FSD \_ TickCount**
</dt> <dd>

Specifica il numero di tick necessari per raggiungere la rete di destinazione. I protocolli di routing diversi da RIP devono convertire le metriche in tick.

</dd> <dt>

**FSD \_ HopCount**
</dt> <dd>

Specifica il conteggio hop associato alla route.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                        |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                             |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                   |
| Intestazione<br/>                   | <dl> <dt>Rtm.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Informazioni di riferimento su Gestione tabelle di routing versione 1](routing-table-manager-version-1-reference.md)
</dt> <dt>

[Strutture di Gestione tabelle di routing versione 1](routing-table-manager-version-1-structures.md)
</dt> <dt>

[**RTM \_ IPX \_ ROUTE**](rtm-ipx-route.md)
</dt> </dl>

 

 





