---
title: Determinazione delle classi associate a un'istanza dell'oggetto
description: Ogni oggetto in Active Directory Domain Services dispone di due attributi i cui valori identificano la gerarchia delle classi di oggetti di cui l'oggetto è un'istanza.
ms.assetid: bb46f165-8c6e-4af1-b387-e0e30a4c6226
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67bc3fe900170e4a856d996f7e373918f242df2e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104470931"
---
# <a name="determining-the-classes-associated-with-an-object-instance"></a>Determinazione delle classi associate a un'istanza dell'oggetto

Ogni oggetto in Active Directory Domain Services dispone di due attributi i cui valori identificano la gerarchia delle classi di oggetti di cui l'oggetto è un'istanza.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attributo</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>structuralObjectClass</strong></td>
<td>Identifica le classi strutturali e astratte di cui l'oggetto è un'istanza. Ad esempio, i valori per un oggetto utente possono essere:
<ul>
<li><strong>top</strong></li>
<li><strong>persona</strong></li>
<li><strong>organizationalPerson</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><strong>objectClass</strong></td>
<td>Identifica le classi incluse in <strong>StructuralObjectClass</strong>, oltre a tutte le classi ausiliarie collegate in modo dinamico. Se ad esempio una &quot; &quot; classe ausiliaria del veicolo è collegata a un oggetto utente, i valori possibili sono:
<ul>
<li><strong>top</strong></li>
<li><strong>veicolo</strong></li>
<li><strong>persona</strong></li>
<li><strong>organizationalPerson</strong></li>
<li><strong>user</strong></li>
</ul></td>
</tr>
</tbody>
</table>



 

Tenere presente che nessuno di questi attributi include classi ausiliarie collegate staticamente con le classi di oggetti di cui l'oggetto è un'istanza. Ad esempio, la classe ausiliaria **securityPrincipal** è collegata in modo statico alla classe **utente** perché è inclusa nei valori **systemAuxiliaryClass** dell'oggetto **classSchema** dell'utente. non è incluso negli attributi **objectClass** o **StructuralObjectClass** delle istanze della classe User.

 

 




