---
title: IPv6-Aware e funzioni helper WPAD legacy
description: Differenze tra IPv6-Aware funzioni helper WPAD e funzioni helper WPAD legacy
ms.assetid: ea4b1c0d-ce02-477b-85c8-44e1beef90c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 511b7f04aa0a2abe04b99562c15aeb3a53bdaadf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316011"
---
# <a name="ipv6-aware-and-legacy-wpad-helper-functions"></a>IPv6-Aware e funzioni helper WPAD legacy

Le tabelle seguenti illustrano le differenze tra le nuove funzioni helper WPAD e le funzioni helper WPAD legacy. Le nuove funzioni sono contrassegnate da un asterisco.



<table>
<thead>
<tr class="header">
<th>Funzioni</th>
<th>Input</th>
<th>Output</th>
<th>Motivo della modifica</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>dnsResolve</td>
<td>Host</td>
<td>IPv4 address (Indirizzo IPv4)</td>
<td rowspan="2">La funzione ex restituirà un elenco di IPv6/IPv4. Necessario perché gli indirizzi IPv6 o IPv4 possono avere più indirizzi unicast per una singola interfaccia. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>dnsResolveEx*</td>
<td>Host</td>
<td>Elenco di indirizzi IPv6/IPv4</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Funzioni</th>
<th>Input</th>
<th>Output</th>
<th>Motivo della modifica</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>con risoluzione</td>
<td>Host IPv4</td>
<td>TRUE / FALSE</td>
<td rowspan="2">La funzione ex restituirà TRUE se un host può essere risolto in un indirizzo IPv6 o IPv4. La funzione legacy restituisce TRUE solo se l'host viene risolto in un indirizzo IPv4. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>isResolveableEx*</td>
<td>Host IPv6/IPv4</td>
<td>TRUE / FALSE</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Funzioni</th>
<th>Input</th>
<th>Output</th>
<th>Motivo della modifica</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>myIPAddress</td>
<td>Nessuno</td>
<td>IPv4 address (Indirizzo IPv4)</td>
<td rowspan="2">La funzione ex restituirà un elenco di IPv6/IPv4. Necessario perché gli indirizzi IPv6 o IPv4 possono avere più indirizzi unicast per una singola interfaccia $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>myIPAddressEx*</td>
<td>Nessuno</td>
<td>Elenco di indirizzi IPv6/IPv4</td>

</tr>
</tbody>
</table>



 



<table>
<thead>
<tr class="header">
<th>Funzioni</th>
<th>Input</th>
<th>Output</th>
<th>Motivo della modifica</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>isInNet</td>
<td>Host, modello di indirizzo IP separato da punti, maschera di indirizzi IP</td>
<td>TRUE / FALSE</td>
<td rowspan="2">Fornire una modalità indipendente dalla versione IP per individuare se un indirizzo IP si trova in una determinata subnet. Inoltre, la notazione della maschera in IPv4 è deprecata. $ {REMOVE} $<br />
</td>
</tr>
<tr class="even">
<td>isInNetEx*</td>
<td>Prefisso IP indirizzo IP</td>
<td>TRUE / FALSE</td>

</tr>
</tbody>
</table>



 



| Funzioni           | Input                       | Output                             | Motivo della modifica                                                                                                                           |
|---------------------|-----------------------------|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| sortIPAddressList\* | Elenco di indirizzi IPv6/IPv4 | Elenco ordinato di indirizzi IPv6/IPv4 | Non esiste alcuna funzione legacy di controparte poiché le funzioni legacy restituiscono solo un singolo indirizzo IPv4, pertanto non è necessario eseguire l'ordinamento. |



 



| Funzioni          | Input | Output                     | Motivo della modifica                                                                                                                                                                                                           |
|--------------------|-------|----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| getClientVersion\* | Nessuno  | Numero di versione del motore WPAD | Attualmente questa funzione restituisce la versione 1,0. Questa funzione è stata aggiunta per consentire agli amministratori IT di aggiornare WPAD in modo che funzionino con versioni diverse del motore WPAD senza causare interruzioni della distribuzione esistente. |



 

> [!Note]  
> Questa funzionalità richiede Windows Internet Explorer 7 o versione successiva.

 

 

 



