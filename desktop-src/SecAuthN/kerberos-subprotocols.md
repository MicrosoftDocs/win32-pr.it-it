---
description: Il protocollo Kerberos è costituito da tre sottoprotocolli.
ms.assetid: a32aebee-4c08-4838-9d81-c62091ce86e4
title: Sottoprotocolli Kerberos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 592c06c26013e065254458ad403cdff99fbb2edd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231845"
---
# <a name="kerberos-subprotocols"></a>Sottoprotocolli Kerberos

Il [*protocollo Kerberos*](../secgloss/k-gly.md) è costituito da tre sottoprotocolli.



| Sottoprotocollo                                                                         | Significato                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Scambio del servizio di autenticazione](authentication-service-exchange.md)<br/>   | In questo sottoprotocollo, il [*centro distribuzione chiavi*](../secgloss/k-gly.md) (KDC) fornisce al client una [*chiave della sessione*](../secgloss/s-gly.md) di accesso e un ticket di concessione ticket (TGT).<br/> |
| [Scambio del servizio di concessione ticket](ticket-granting-service-exchange.md)<br/> | In questo sottoprotocollo, il KDC distribuisce una chiave della sessione del servizio e un ticket per il servizio.<br/>                                                                                                                                                                                                            |
| [Exchange client/server](client-server-exchange.md)<br/>                     | In questo sottoprotocollo il client presenta il ticket per l'ammissione a un servizio.<br/>                                                                                                                                                                                                                         |



 

 

 
