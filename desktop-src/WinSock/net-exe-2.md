---
description: Net.exe possibile usare per arrestare e avviare il protocollo IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29ab08a69590d6cf53a42096bf12d2e8657c571fd27b637feca4c51c61354225
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117741078"
---
# <a name="netexe"></a>Net.exe

Net.exe possibile usare per arrestare e avviare il protocollo IPv6. Il riavvio di IPv6 reinizializza il protocollo come se il computer fosse in esecuzione, con la possibile modifica dei numeri di interfaccia. Net.exe contiene molti sottocomandi. I comandi seguenti sono rilevanti per IPv6:

<dl> <dt>

<span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**net stop tcpip6**
</dt> <dd>

Arresta il protocollo IPv6 e lo scarica dalla memoria. Questo comando ha esito negativo se sono aperti socket IPv6.

</dd> <dt>

<span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**net start tcpip6**
</dt> <dd>

Avvia il protocollo IPv6 se è stato arrestato. Se nella directory %systemroot% System32 Drivers è presente un nuovo file del driver di Tcpip6.sys, tale file viene \\ \\ caricato.

</dd> </dl>

 

 



