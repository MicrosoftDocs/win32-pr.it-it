---
description: WMI definisce un set di proprietà di sistema associate a tutte le classi e istanze delle classi, oltre alle proprietà specifiche della classe.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: Proprietà di sistema CIM per oggetti MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313193"
---
# <a name="cim-system-properties-for-mib-objects"></a>Proprietà di sistema CIM per oggetti MIB

WMI definisce un set di proprietà di sistema associate a tutte le classi e istanze delle classi, oltre alle proprietà specifiche della classe.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Il provider SNMP utilizza le proprietà di sistema CIM seguenti quando si esegue il mapping delle definizioni di oggetti MIB alle definizioni di classi CIM. Per il provider SNMP per la risoluzione completa di un oggetto gruppo, è necessario che siano presenti proprietà obbligatorie. La mancata definizione di una proprietà obbligatoria restituisce un errore.



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
<td><strong>stringa</strong> di Obbligatorio<br/> Per le istanze, la classe a cui appartiene l'oggetto. Per le classi, questo è il nome della classe.<br/></td>
</tr>
<tr class="even">
<td><strong>__DYNASTY</strong></td>
<td><strong>stringa</strong> di Opzionale<br/> Nome della classe che rappresenta la classe di base finale per l'oggetto corrente (non la classe padre immediata).<br/></td>
</tr>
<tr class="odd">
<td><strong>__GENUS</strong></td>
<td><strong>UInt32</strong> Obbligatorio<br/> Tipo di oggetto. I valori possibili sono:<br/> <dl> 1 = classe<br />
2 = istanza<br />
</dl></td>
</tr>
<tr class="even">
<td><strong>__NAMESPACE</strong></td>
<td><strong>stringa</strong> di Obbligatorio<br/> Spazio dei nomi in cui si trova l'oggetto.<br/></td>
</tr>
<tr class="odd">
<td><strong>__PATH</strong></td>
<td><strong>stringa</strong> di Obbligatorio<br/> Percorso assoluto dell'oggetto.<br/></td>
</tr>
<tr class="even">
<td><strong>__PROPERTYCOUNT</strong></td>
<td><strong>UInt32</strong> Obbligatorio<br/> Numero di proprietà non di sistema definite per l'oggetto.<br/></td>
</tr>
<tr class="odd">
<td><strong>__RELPATH</strong></td>
<td><strong>stringa</strong> di Obbligatorio<br/> Percorso relativo dell'oggetto.<br/></td>
</tr>
<tr class="even">
<td><strong>__SERVER</strong></td>
<td><strong>stringa</strong> di Obbligatorio<br/> Server che fornisce l'oggetto.<br/></td>
</tr>
<tr class="odd">
<td><strong>__SUPERCLASS</strong></td>
<td><strong>stringa</strong> di Opzionale<br/> Classe padre immediata dell'oggetto.<br/></td>
</tr>
</tbody>
</table>



 

 

 




