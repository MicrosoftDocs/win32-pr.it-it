---
description: WMI definisce un set di proprietà di sistema associate a tutte le classi e istanze di classi oltre alle proprietà specifiche della classe.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: Proprietà di sistema CIM per oggetti MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8448cbfa086b44542a4fee065599ef3fc1167454a2633f92b9268e3c06766958
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118820076"
---
# <a name="cim-system-properties-for-mib-objects"></a>Proprietà di sistema CIM per oggetti MIB

WMI definisce un set di proprietà di sistema associate a tutte le classi e istanze di classi oltre alle proprietà specifiche della classe.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 

Il provider SNMP usa le proprietà di sistema CIM seguenti quando si esegue il mapping delle definizioni degli oggetti MIB alle definizioni di classe CIM. Le proprietà obbligatorie devono essere presenti perché il provider SNMP risolva completamente un oggetto gruppo. Se non si definisce una proprietà obbligatoria, viene restituito un errore.



<table>
<thead>
<tr class="header">
<th>Proprietà</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>__CLASS</strong></td>
<td><strong>string</strong> Obbligatorio<br/> Per le istanze di , classe a cui appartiene l'oggetto . Per le classi, questo è il nome della classe.<br/></td>
</tr>
<tr class="even">
<td><strong>__DYNASTY</strong></td>
<td><strong>string</strong> Opzionale<br/> Nome della classe che rappresenta la classe di base finale per l'oggetto corrente (non la relativa classe padre immediata).<br/></td>
</tr>
<tr class="odd">
<td><strong>__GENUS</strong></td>
<td><strong>uint32</strong> Obbligatorio<br/> Tipo di oggetto. I valori possibili sono:<br/> <dl> 1 = classe<br />
2 = istanza<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>__NAMESPACE</strong></td>
<td><strong>string</strong> Obbligatorio<br/> Spazio dei nomi in cui si trova l'oggetto.<br/></td>
</tr>
<tr class="odd">
<td><strong>__PATH</strong></td>
<td><strong>string</strong> Obbligatorio<br/> Percorso assoluto dell'oggetto.<br/></td>
</tr>
<tr class="even">
<td><strong>__PROPERTYCOUNT</strong></td>
<td><strong>uint32</strong> Obbligatorio<br/> Numero di proprietà non di sistema definite per l'oggetto.<br/></td>
</tr>
<tr class="odd">
<td><strong>__RELPATH</strong></td>
<td><strong>string</strong> Obbligatorio<br/> Percorso relativo dell'oggetto.<br/></td>
</tr>
<tr class="even">
<td><strong>__SERVER</strong></td>
<td><strong>string</strong> Obbligatorio<br/> Server che fornisce l'oggetto .<br/></td>
</tr>
<tr class="odd">
<td><strong>__SUPERCLASS</strong></td>
<td><strong>string</strong> Opzionale<br/> Classe padre immediata dell'oggetto.<br/></td>
</tr>
</tbody>
</table>



 

 

 




