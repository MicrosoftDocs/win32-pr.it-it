---
title: Struttura IPX_SPECIFIC_DATA (RTM. h)
description: La \_ struttura di dati specifici di IPX \_ contiene dati specifici di IPX.
ms.assetid: 4d97092d-692c-4dc7-af7f-260dc76c6c08
keywords:
- RAS struttura IPX_SPECIFIC_DATA
- RAS puntatore alla struttura PIPX_SPECIFIC_DATA
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
ms.openlocfilehash: 56badfb6149e416c71b447aca93564b5eb5aba7a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103963729"
---
# <a name="ipx_specific_data-structure"></a>\_Struttura di dati specifici di IPX \_

\[Questa API è stata sostituita dall'API di [Gestione tabelle di routing versione 2](about-routing-table-manager-version-2.md) e non sarà disponibile oltre Windows Server 2003. Le applicazioni devono usare l'API di Routing Table Manager versione 2.\]

La struttura di **\_ \_ dati specifici di IPX** contiene dati specifici di IPX.

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

**\_Flag FSD**
</dt> <dd>

Specifica i flag che descrivono la route. Attualmente, questo membro è pari a zero o al valore del flag seguente.



| Valore                                                                                                                                                                                                      | Significato                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="IPX_GLOBAL_CLIENT_WAN_ROUTE"></span><span id="ipx_global_client_wan_route"></span><dl> <dt>**\_ \_ \_ Route WAN client globale \_ IPX**</dt> </dl> | Specifica che questa route è destinata alla rete globale allocata per tutti i client WAN.<br/> |



 

</dd> <dt>

**\_TickCount FSD**
</dt> <dd>

Specifica il numero di cicli necessari per raggiungere la rete di destinazione. I protocolli di routing diversi da RIP devono convertire le metriche in cicli.

</dd> <dt>

**\_HopCount FSD**
</dt> <dd>

Specifica il numero di hop associato alla route.

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

[**\_Route IPX \_ RTM**](rtm-ipx-route.md)
</dt> </dl>

 

 





