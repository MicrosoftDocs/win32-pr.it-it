---
description: 'Altre informazioni su: Campi server2003Grbits'
title: Campi Server2003Grbits (Microsoft.Isam.Esent.Interop.Server2003)
TOCTitle: Server2003Grbits fields
ms:assetid: Fields.T:Microsoft.Isam.Esent.Interop.Server2003.Server2003Grbits
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003grbits_fields(v=EXCHG.10)
ms:contentKeyID: 55104210
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 77db94da9f3a5dbec982b31c0ea3d673ffb6228a58f81adf644ff498a2cf4f84
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118071673"
---
# <a name="server2003grbits-fields"></a>Campi server2003Grbits

Includere membri protetti  
Includere i membri ereditati  

Il [tipo Server2003Grbits](./server2003grbits-class.md) espone i membri seguenti.

## <a name="fields"></a>Campi

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
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351203(v=exchg.10).md">EnumerateIgnoreUserDefinedDefault</a></td>
<td>Se una determinata colonna non è presente nel record e ha un valore predefinito definito dall'utente, non verrà restituito alcun valore di colonna. Questa opzione impedisce la chiamata del callback che calcola il valore predefinito definito dall'utente per la colonna durante l'enumerazione dei valori per tale colonna.</td>
</tr>
<tr class="even">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351284(v=exchg.10).md">ForwardOnly</a></td>
<td>Questa opzione richiede che la tabella temporanea sia creata solo se il gestore tabelle temporaneo può usare l'implementazione ottimizzata per i risultati intermedi delle query. Se una caratteristica della tabella temporanea impedisce l'uso di questa ottimizzazione, l'operazione avrà esito negativo con JET_errCannotMaterializeForwardOnlySort. Un effetto collaterale di questa opzione è consentire alla tabella temporanea di contenere record con chiavi di indice duplicate. Per <a href="hh558517(v=exchg.10).md">altre informazioni,</a> vedere Univoco.</td>
</tr>
<tr class="odd">
<td><img src="../images/hh596466.pubfield(exchg.10).gif" title="Campo pubblico" alt="Public field" /><img src="../images/dn292146.static(exchg.10).gif" title="Membro statico" alt="Static member" /></td>
<td><a href="dn351209(v=exchg.10).md">WaitAllLevel0Commit</a></td>
<td>Tutte le transazioni di cui è stato eseguito il commit in precedenza da qualsiasi sessione che non sono ancora state scaricate nel file di log delle transazioni verranno scaricate immediatamente. Questa API attenderà che le transazioni siano state scaricate prima di tornare al chiamante. Questa opzione può essere usata anche se la sessione non è attualmente in una transazione. Questa opzione non può essere usata in combinazione con altre opzioni.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Server2003Grbits](./server2003grbits-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
