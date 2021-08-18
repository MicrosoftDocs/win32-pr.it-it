---
description: 'Altre informazioni su: Metodi DurableCommitCallback'
title: Metodi DurableCommitCallback (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: DurableCommitCallback methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback_methods(v=EXCHG.10)
ms:contentKeyID: 55104392
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 0e410c1970df4809f879348603602fc507e7c68598d9e2ec1cc372a971160f9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119623431"
---
# <a name="durablecommitcallback-methods"></a>Metodi DurableCommitCallback

Includere membri protetti  
Includi membri ereditati  

Il [tipo DurableCommitCallback](./durablecommitcallback-class.md) espone i membri seguenti.

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
<td>Genera un'eccezione se questo oggetto è stato eliminato. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose()</a></td>
<td>Eliminare questo oggetto, rilasciando la risorsa Esent sottostante. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></td>
<td>Chiamato da Dispose e dal finalizzatore. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335442(v=exchg.10).md">Fine</a></td>
<td>Termina la sessione di commit durevole.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">Finalizza</a></td>
<td>Finalizza un'istanza della classe EsentResource. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">GetType</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn335327(v=exchg.10).md">ReleaseResource</a></td>
<td>Libera la sessione di commit durevole. Esegue l'override <a href="dn350545(v=exchg.10).md">di EsentResource.ReleaseResource()</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></td>
<td>Chiamato da una sottoclasse quando viene allocata una risorsa. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource.</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></td>
<td>Chiamato da una sottoclasse quando viene liberata una risorsa. Ereditato da <a href="dn319890(v=exchg.10).md">EsentResource.</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn335445(v=exchg.10).md">ToString</a></td>
<td>Genera una rappresentazione di stringa della struttura . Esegue l'override <a href="/dotnet/api/system.object.tostring#System_Object_ToString">di Object.ToString().</a></td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe DurableCommitCallback](./durablecommitcallback-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
