---
description: La tabella seguente descrive le \_ Opzioni del socket del tipo di traffico IP DSCP \_ \_ .
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
ms.openlocfilehash: 80cbe41e58cf36cd366015d83af380f5952630ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328375"
---
# <a name="ip_dscp_traffic_type"></a>\_tipo di \_ traffico \_ DSCP IP

La tabella seguente descrive le \_ Opzioni del socket del tipo di traffico IP DSCP \_ \_ .

<dl> <dt><span id="IP_DSCP_TRAFFIC_TYPE"></span><span id="ip_dscp_traffic_type"></span>**\_tipo di \_ traffico \_ DSCP IP**</dt> <dd> <dl> <dt> 

| Opzione              | Recupero | Set | Tipo optVal | Descrizione                                                                                                                                                                                                                                                                                                                                      |
|---------------------|-----|-----|-------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipo di traffico DSCP \_ | Sì | Sì | DWORD       | Impostando questo valore su valori definiti nel **\_ \_ tipo di traffico DSCP**, un'applicazione sarà in grado di richiedere i pacchetti di rete da considerare in base al tipo di servizio richiesto. Analogamente, le chiamate a [**getsockopt**](/windows/desktop/api/winsock/nf-winsock-getsockopt) possono essere usate per ottenere l'impostazione corrente per il tipo di traffico richiesto sul socket specificato |



 


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|--------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows 10<br/>                                                          |
| Fine del supporto server<br/> | Windows Server 2016<br/>                                                 |
| Intestazione<br/>                | <dl> <dt>N/D</dt> </dl> |



 

 




