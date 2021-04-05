---
description: 'Altre informazioni su: metodo API. RetrieveColumn'
title: API. RetrieveColumn, metodo
TOCTitle: 'RetrieveColumn method '
ms:assetid: Overload:Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.retrievecolumn(v=EXCHG.10)
ms:contentKeyID: 55100835
ms.date: 07/30/2014
ms.topic: article
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.RetrieveColumn
dev_langs:
- CSharp
- JScript
- VB
- other
ms.openlocfilehash: 3bcb5effcfc59e155007fbd9e1733d95db058970
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103758978"
---
# <a name="apiretrievecolumn-method"></a>API. RetrieveColumn, metodo

Includi membri protetti  
Includi membri ereditati  

## <a name="overload-list"></a>Elenco di overload

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nome</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334041(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID)</a></td>
<td>Recupera un valore di colonna singola dal record corrente. Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn334060(v=exchg.10).md">RetrieveColumn (JET_SESID, JET_TABLEID, JET_COLUMNID, RetrieveColumnGrbit, JET_RETINFO)</a></td>
<td>Recupera un valore di colonna singola dal record corrente. Il record è il record associato alla voce di indice in corrispondenza della posizione corrente del cursore. In alternativa, questa funzione può recuperare una colonna da un record creato nel buffer di copia del cursore. Questa funzione può anche recuperare i dati di colonna da una voce di indice che fa riferimento al record corrente. Oltre a recuperare il valore della colonna effettivo, è possibile utilizzare JetRetrieveColumn anche per recuperare le dimensioni di una colonna, prima di recuperare i dati della colonna in modo che i buffer dell'applicazione possano essere ridimensionati in modo appropriato.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe API](./api-class.md)

[Membri API](./api-members.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
