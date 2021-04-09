---
description: Questa pagina descrive il comportamento delle opzioni dei socket multicast basate su diversi Stati delle impostazioni delle opzioni del socket.
ms.assetid: a411e831-7b28-4ab5-a09a-650db99a7cd5
title: Comportamento dell'opzione socket multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fd10094750bea59b844ad1fcdac70be0c7f9646
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049482"
---
# <a name="multicast-socket-option-behavior"></a>Comportamento dell'opzione socket multicast

Questa pagina descrive il comportamento delle opzioni dei socket multicast basate su diversi Stati delle impostazioni delle opzioni del socket.

Ad esempio, in questa pagina viene descritto il comportamento quando \_ l' \_ opzione IP Aggiungi origine \_ socket è impostata su un socket per il quale \_ è \_ già stata impostata l'opzione di appartenenza all'origine IP Aggiungi \_ con la coppia gruppo/origine specificata nella stessa interfaccia di rete. È consentito chiamare l'appartenenza all' \_ origine IP Aggiungi nello \_ \_ stesso gruppo in un'interfaccia di rete diversa.

Questa pagina supporta la progettazione e la risoluzione dei problemi delle applicazioni multicast Windows Sockets. 

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
<td rowspan="4">IP_ADD_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Non chiamare IP_ADD_MEMBERSHIP con lo stesso gruppo più di una volta nella stessa interfaccia di rete.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Non chiamare IP_ADD_SOURCE_MEMBERSHIP con lo stesso gruppo precedentemente chiamato con IP_ADD_MEMBERSHIP nella stessa interfaccia di rete.</td>

</tr>
<tr class="odd">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>In alternativa, usare IP_BLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Restituisce un errore quando si tenta di sbloccare una coppia gruppo/origine che non è stata precedentemente bloccata nella stessa interfaccia di rete.</td>

</tr>
<tr class="odd">
<td>IP_DROP_MEMBERSHIP</td>
<td>Qualsiasi chiamata successiva sulla stessa coppia gruppo/gruppo/origine</td>
<td>WSAEINVAL</td>
<td>L'esecuzione di chiamate di opzioni socket su una coppia gruppo o gruppo/origine non attualmente presente nell'elenco di inclusione (a causa della rimozione dell'appartenenza o in caso contrario) genera un errore.</td>
</tr>
<tr class="even">
<td rowspan="3">IP_ADD_SOURCE_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Non chiamare IP_ADD_MEMBERSHIP con lo stesso gruppo precedentemente chiamato con IP_ADD_SOURCE_MEMBERSHIP nella stessa interfaccia di rete.</td>
</tr>
<tr class="odd">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Non chiamare IP_ADD_SOURCE_MEMBERSHIP con la stessa coppia gruppo/origine chiamata in precedenza con IP_ADD_SOURCE_MEMBERSHIP nella stessa interfaccia di rete.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Restituisce un errore quando si tenta di sbloccare una coppia gruppo/origine che non è stata precedentemente bloccata nella stessa interfaccia di rete.</td>

</tr>
<tr class="odd">
<td rowspan="2">IP_DROP_SOURCE_MEMBERSHIP $ {REMOVE} $<br />
</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEINVAL</td>
<td>Restituisce un errore quando si tenta di sbloccare una coppia gruppo/origine che non è stata precedentemente bloccata nella stessa interfaccia di rete.</td>
</tr>
<tr class="even">
<td>IP_DROP_SOURCE_MEMBERSHIP</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Restituisce un errore quando si tenta di eliminare una coppia gruppo/origine che non è presente nell'elenco di inclusione nella stessa interfaccia di rete.</td>

</tr>
<tr class="odd">
<td rowspan="3">IP_BLOCK_SOURCE $ {REMOVE} $<br />
</td>
<td>IP_BLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Restituisce un errore quando si tenta di bloccare una coppia gruppo/origine che è già bloccata nella stessa interfaccia di rete.</td>
</tr>
<tr class="even">
<td>IP_ADD_SOURCE_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>In alternativa, usare IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="odd">
<td>IP_ADD_MEMBERSHIP</td>
<td>WSAEINVAL</td>
<td>In alternativa, usare IP_UNBLOCK_SOURCE.</td>

</tr>
<tr class="even">
<td>IP_UNBLOCK_SOURCE</td>
<td>IP_UNBLOCK_SOURCE</td>
<td>WSAEADDRNOTAVAIL</td>
<td>Restituisce un errore quando si tenta di sbloccare una coppia gruppo/origine che non è presente nell'elenco bloccato nella stessa interfaccia di rete.</td>
</tr>
</tbody>
</table>



 

 

 



