---
description: Nella tabella seguente vengono descritte le opzioni del \_ socket IP DSCP \_ TRAFFIC \_ TYPE.
ms.assetid: 0042B53F-B84E-453A-8E18-87052280DAD5
title: IP_DSCP_TRAFFIC_TYPE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IP_DSCP_TRAFFIC_TYPE
api_type:
- HeaderDef
api_location:
- N/A
ms.openlocfilehash: 87915dc214b0ba306b4f38dbd833b27199277564fa8c2815b9147e0d82253589
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097851"
---
# <a name="ip_dscp_traffic_type"></a>TIPO \_ DI TRAFFICO \_ DSCP \_ IP

Nella tabella seguente vengono descritte le opzioni del \_ socket IP DSCP \_ TRAFFIC \_ TYPE.

<dl> <dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**TIPO \_ DI TRAFFICO \_ DSCP \_ IP**</dt> <dd> <dl> <dt> 

| Opzione              | Recupero | Impostazione | Tipo optval | Descrizione                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TIPO DI \_ TRAFFICO DSCP \_ | Sì | Sì | DWORD       | Impostando questo valore su valori definiti in **DSCP \_ TRAFFIC \_ TYPE,** un'applicazione sarà in grado di chiedere ai pacchetti di rete di essere trattati in base al tipo di servizio richiesto. Analogamente, le chiamate a [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) possono essere usate per ottenere l'impostazione corrente per il tipo di traffico richiesto nel socket specificato |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|--------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows 10<br/>                                                          |
| Fine del supporto server<br/> | Windows Server 2016<br/>                                                 |
| Intestazione<br/>                | <dl> <dt>N/D</dt> </dl> |



 

 




