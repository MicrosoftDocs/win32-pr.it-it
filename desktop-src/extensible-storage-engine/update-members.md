---
description: 'Altre informazioni su: Aggiorna membri'
title: 'Membri di Update '
TOCTitle: Update members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Update
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.update_members(v=EXCHG.10)
ms:contentKeyID: 55104188
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 9c97398ca903445c2d883b471e0dd7978fe95656
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104566594"
---
# <a name="update-members"></a>Membri di Update 

Includi membri protetti  
Includi membri ereditati  

Classe che incapsula un aggiornamento in un JET_TABLEID.

Il tipo di [aggiornamento](./update-class.md) espone i membri seguenti.

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
<td><a href="dn351261(v=exchg.10).md">Aggiornamento</a></td>
<td>Inizializza una nuova istanza della classe Update. Viene avviato automaticamente un aggiornamento. Se non viene salvato in modo esplicito, l'aggiornamento verrà annullato.</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn351266(v=exchg.10).md">Annulla</a></td>
<td>Annullare l'aggiornamento.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></td>
<td>Genera un'eccezione se l'oggetto è stato eliminato. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose ()</a></td>
<td>Eliminare questo oggetto, rilasciando la risorsa ESENT sottostante. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose (valore booleano)</a></td>
<td>Chiamato da Dispose e dal finalizzatore. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource</a>.</td>
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
<td><a href="dn351268(v=exchg.10).md">ReleaseResource</a></td>
<td>Chiamato quando la transazione viene eliminata quando è attiva. Questa operazione deve eseguire il rollback della transazione. Esegue l'override di <a href="dn350545(v=exchg.10).md">EsentResource. ReleaseResource ()</a>.</td>
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
<td><a href="dn351270(v=exchg.10).md">Salva ()</a></td>
<td>Aggiornare il TableID.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn351199(v=exchg.10).md">Salva ([], Int32, Int32)</a></td>
<td>Aggiornare il TableID.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn351272(v=exchg.10).md">SaveAndGotoBookmark</a></td>
<td>Aggiornare TableID e posizionare TableID sul record che è stato modificato. Questa operazione può essere utile quando si inserisce un record perché per impostazione predefinita il TableID rimane nella posizione precedente.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn351192(v=exchg.10).md">ToString</a></td>
<td>Restituisce una <a href="/dotnet/api/system.string">stringa</a> che rappresenta l' <a href="dn351191(v=exchg.10).md">aggiornamento</a>corrente. Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe Update](./update-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
