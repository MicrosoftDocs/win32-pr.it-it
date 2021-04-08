---
description: 'Altre informazioni su: membri di DurableCommitCallback'
title: Membri di DurableCommitCallback (Microsoft. ISAM. esent. Interop. Windows8)
TOCTitle: DurableCommitCallback members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback_members(v=EXCHG.10)
ms:contentKeyID: 55104391
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 47086ba03982e21703ca89c2da41121824121cb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058013"
---
# <a name="durablecommitcallback-members"></a>Membri di DurableCommitCallback

Includi membri protetti  
Includi membri ereditati  

Esegue il wrapping del callback che riguarda i commit durevoli.

Il tipo [DurableCommitCallback](./durablecommitcallback-class.md) espone i membri seguenti.

## <a name="constructors"></a>Costruttori

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335324(v=exchg.10).md">DurableCommitCallback</a></td>
<td>Inizializza una nuova istanza della classe <a href="dn335323(v=exchg.10).md">DurableCommitCallback</a> .</td>
</tr>
</tbody>
</table>


Inizio

## <a name="properties"></a>Proprietà

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
<td><img src="../images/dn292128.protproperty(exchg.10).gif" title="Proprietà protetta." alt="Protected property" /></td>
<td><a href="dn350578(v=exchg.10).md">HasResource</a></td>
<td>Ottiene un valore che indica se la risorsa sottostante è attualmente allocata. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="methods"></a>Metodi

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
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></td>
<td>Genera un'eccezione se l'oggetto è stato eliminato. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose ()</a></td>
<td>Eliminare questo oggetto, rilasciando la risorsa ESENT sottostante. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose (valore booleano)</a></td>
<td>Chiamato da Dispose e dal finalizzatore. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335442(v=exchg.10).md">Fine</a></td>
<td>Termina la sessione di commit durevole.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">Finalize</a></td>
<td>Finalizza un'istanza della classe EsentResource. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn335327(v=exchg.10).md">ReleaseResource</a></td>
<td>Libera la sessione di commit durevole. Esegue l'override di <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></td>
<td>Chiamato da una sottoclasse quando viene allocata una risorsa. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></td>
<td>Chiamato da una sottoclasse quando una risorsa viene liberata. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335445(v=exchg.10).md">ToString</a></td>
<td>Genera una rappresentazione in forma di stringa della struttura. Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe DurableCommitCallback](./durablecommitcallback-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop. Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
