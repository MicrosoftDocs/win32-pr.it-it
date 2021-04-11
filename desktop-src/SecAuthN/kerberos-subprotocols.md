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
# <a name="kerberos-subprotocols"></a><span data-ttu-id="119b3-103">Sottoprotocolli Kerberos</span><span class="sxs-lookup"><span data-stu-id="119b3-103">Kerberos Subprotocols</span></span>

<span data-ttu-id="119b3-104">Il [*protocollo Kerberos*](../secgloss/k-gly.md) è costituito da tre sottoprotocolli.</span><span class="sxs-lookup"><span data-stu-id="119b3-104">The [*Kerberos protocol*](../secgloss/k-gly.md) is composed of three subprotocols.</span></span>



| <span data-ttu-id="119b3-105">Sottoprotocollo</span><span class="sxs-lookup"><span data-stu-id="119b3-105">Subprotocol</span></span>                                                                         | <span data-ttu-id="119b3-106">Significato</span><span class="sxs-lookup"><span data-stu-id="119b3-106">Meaning</span></span>                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="119b3-107">Scambio del servizio di autenticazione</span><span class="sxs-lookup"><span data-stu-id="119b3-107">Authentication Service Exchange</span></span>](authentication-service-exchange.md)<br/>   | <span data-ttu-id="119b3-108">In questo sottoprotocollo, il [*centro distribuzione chiavi*](../secgloss/k-gly.md) (KDC) fornisce al client una [*chiave della sessione*](../secgloss/s-gly.md) di accesso e un ticket di concessione ticket (TGT).</span><span class="sxs-lookup"><span data-stu-id="119b3-108">In this subprotocol, the [*Key Distribution Center*](../secgloss/k-gly.md) (KDC) gives the client a logon [*session key*](../secgloss/s-gly.md) and a ticket-granting ticket (TGT).</span></span><br/> |
| [<span data-ttu-id="119b3-109">Scambio del servizio di concessione ticket</span><span class="sxs-lookup"><span data-stu-id="119b3-109">Ticket-Granting Service Exchange</span></span>](ticket-granting-service-exchange.md)<br/> | <span data-ttu-id="119b3-110">In questo sottoprotocollo, il KDC distribuisce una chiave della sessione del servizio e un ticket per il servizio.</span><span class="sxs-lookup"><span data-stu-id="119b3-110">In this subprotocol, the KDC distributes a service session key and a ticket for the service.</span></span><br/>                                                                                                                                                                                                            |
| [<span data-ttu-id="119b3-111">Exchange client/server</span><span class="sxs-lookup"><span data-stu-id="119b3-111">Client/Server Exchange</span></span>](client-server-exchange.md)<br/>                     | <span data-ttu-id="119b3-112">In questo sottoprotocollo il client presenta il ticket per l'ammissione a un servizio.</span><span class="sxs-lookup"><span data-stu-id="119b3-112">In this subprotocol, the client presents the ticket for admission to a service.</span></span><br/>                                                                                                                                                                                                                         |



 

 

 
