---
description: Net.exe può essere utilizzato per arrestare e avviare il protocollo IPv6.
ms.assetid: faa555d9-eb20-4b7a-94eb-b67a48ee630e
title: Net.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5074696b71ce000ef330f2c88fceef0f60b0222e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103879197"
---
# <a name="netexe"></a>Net.exe

Net.exe può essere utilizzato per arrestare e avviare il protocollo IPv6. Il riavvio di IPv6 reinizializza il protocollo come se il computer venisse riavviato, il che potrebbe modificare i numeri di interfaccia. Net.exe dispone di molti sottocomandi. I comandi seguenti sono rilevanti per IPv6:

<dl> <dt>

<span id="net_stop_tcpip6"></span><span id="NET_STOP_TCPIP6"></span>**NET STOP tcpip6**
</dt> <dd>

Arresta il protocollo IPv6 e lo Scarica dalla memoria. Questo comando non riesce se sono presenti socket IPv6 aperti.

</dd> <dt>

<span id="net_start_tcpip6"></span><span id="NET_START_TCPIP6"></span>**NET Start tcpip6**
</dt> <dd>

Avvia il protocollo IPv6 se è stato arrestato. Se nella directory% SystemRoot% system32 drivers è presente un nuovo file di driver Tcpip6.sys \\ \\ , viene caricato il file del driver.

</dd> </dl>

 

 



