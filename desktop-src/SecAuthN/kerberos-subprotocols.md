---
description: Il protocollo Kerberos è costituito da tre sottoprotocol.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Sottoprotocol Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5ea1ababaf1ec7fe4e80112d4c1f69dc8bfc242a40cea56675d08198188a130
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013361"
---
# <a name="kerberos-subprotocols"></a>Sottoprotocol Kerberos

Il [*protocollo Kerberos*](../secgloss/k-gly.md) è costituito da tre sottoprotocol.



| Subprotocol                                                                         | Significato                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Scambio del servizio di autenticazione](authentication-service-exchange.md)<br/>   | In questo sottoprotocollo, [*il Centro distribuzione chiavi*](../secgloss/k-gly.md) (KDC) fornisce [](../secgloss/s-gly.md) al client una chiave di sessione di accesso e un ticket di concessione ticket (TGT).<br/> |
| [Scambio del servizio di concessione ticket](ticket-granting-service-exchange.md)<br/> | In questo sottoprotocollo, il KDC distribuisce una chiave di sessione del servizio e un ticket per il servizio.<br/>                                                                                                                                                                                                            |
| [Client/Server Exchange](client-server-exchange.md)<br/>                     | In questo sottoprotocollo, il client presenta il ticket per l'ammissione a un servizio.<br/>                                                                                                                                                                                                                         |



 

 

 
