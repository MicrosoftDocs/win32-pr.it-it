---
description: Questa pagina descrive il comportamento delle opzioni socket multicast in base a vari stati delle impostazioni delle opzioni socket.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Comportamento dell'opzione socket multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3367487d12a6c54c8aaf5ce623c717ed229a001875c68a6b782dde0739a328ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118993661"
---
# <a name="multicast-socket-option-behavior"></a>Comportamento dell'opzione socket multicast

Questa pagina descrive il comportamento delle opzioni socket multicast in base a vari stati delle impostazioni delle opzioni socket.

Ad esempio, questa pagina descrive il comportamento quando l'opzione socket IP ADD SOURCE MEMBERSHIP è impostata su un socket per cui l'opzione IP ADD SOURCE MEMBERSHIP è già stata impostata con la coppia \_ \_ \_ \_ \_ gruppo/origine specificata nella stessa interfaccia di \_ rete. È consentito chiamare IP \_ ADD SOURCE MEMBERSHIP nello stesso gruppo in \_ \_ un'interfaccia di rete diversa.

Questa pagina consente di progettare correttamente e risolvere i Windows multicast Sockets. 

<table>
<thead>
<tr class="header">
<th>Opzione socket iniziale</th>
<th>Opzione socket successiva in conflitto</th>
<th>Errore restituito</th>
<th>Commenti</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="4">IP_ADD_MEMBERSHIP${REMOVE}$<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Non chiamare IP_ADD_MEMBERSHIP con lo stesso gruppo più volte sulla stessa interfaccia di rete.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Non chiamare IP_ADD_SOURCE_MEMBERSHIP con lo stesso gruppo chiamato in precedenza con IP_ADD_MEMBERSHIP sulla stessa interfaccia di rete.</td>

</tr>
<tr class="odd">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Usare IP_BLOCK_SOURCE invece.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Restituisce un errore durante il tentativo di sbloccare una coppia gruppo/origine che non è stata bloccata in precedenza nella stessa interfaccia di rete.</td>

</tr>
<tr class="odd">
<td>IP_DROP_MEMBERSHIP</td>
<td>Qualsiasi chiamata successiva sulla stessa coppia gruppo/gruppo/origine</td>
<td>WSAEINVAL</td>
<td>L'esecuzione di chiamate all'opzione socket su una coppia gruppo/gruppo/origine non attualmente presente nell'elenco di inclusione (a causa dell'eliminazione dell'appartenenza o di altro tipo) comporta un errore.</td>
</tr>
<tr class="even">
<td rowspan="3">IP_ADD_SOURCE_MEMBERSHIP${REMOVE}$<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Non chiamare IP_ADD_MEMBERSHIP con lo stesso gruppo chiamato in precedenza con IP_ADD_SOURCE_MEMBERSHIP sulla stessa interfaccia di rete.</td>
</tr>
<tr class="odd">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Non chiamare IP_ADD_SOURCE_MEMBERSHIP con la stessa coppia gruppo/origine chiamata in precedenza con IP_ADD_SOURCE_MEMBERSHIP sulla stessa interfaccia di rete.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Restituisce un errore durante il tentativo di sbloccare una coppia gruppo/origine che non è stata bloccata in precedenza nella stessa interfaccia di rete.</td>

</tr>
<tr class="odd">
<td rowspan="2">IP_DROP_SOURCE_MEMBERSHIP${REMOVE}$<br />
</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Restituisce un errore durante il tentativo di sbloccare una coppia gruppo/origine che non è stata bloccata in precedenza nella stessa interfaccia di rete.</td>
</tr>
<tr class="even">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Restituisce un errore durante il tentativo di eliminare una coppia gruppo/origine che non è presente nell'elenco di inclusione nella stessa interfaccia di rete.</td>

</tr>
<tr class="odd">
<td rowspan="3">IP_BLOCK_SOURCE${REMOVE}$<br />
</td>
<td>IP_BLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Restituisce un errore durante il tentativo di bloccare una coppia gruppo/origine già bloccata nella stessa interfaccia di rete.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Usare IP_UNBLOCK_SOURCE invece.</td>

</tr>
<tr class="odd">
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>Usare IP_UNBLOCK_SOURCE invece.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Restituisce un errore durante il tentativo di sbloccare una coppia gruppo/origine che non è presente nell'elenco bloccato nella stessa interfaccia di rete.</td>
</tr>
</tbody>
</table>



 

 

 



