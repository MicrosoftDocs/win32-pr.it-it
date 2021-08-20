---
description: 'Altre informazioni su: JET_SPACEHINTS membri'
title: JET_SPACEHINTS membri
TOCTitle: JET_SPACEHINTS members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_SPACEHINTS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_spacehints_members(v=EXCHG.10)
ms:contentKeyID: 55103957
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 2022ad3c8139c814a3adda9ea1b88d8b9d54c2ef3db3999b8e0f11ae1509060e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118073517"
---
# <a name="jet_spacehints-members"></a>JET_SPACEHINTS membri

Includere membri protetti  
Includi membri ereditati  

Descrive una colonna in una tabella di un database ESENT.

Il [JET_SPACEHINTS](./jet-spacehints-class.md) espone i membri seguenti.

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
<td><a href="dn351065(v=exchg.10).md">JET_SPACEHINTS</a></td>
<td></td>
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
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351103(v=exchg.10).md">cbInitial</a></td>
<td>Ottiene o imposta la dimensione iniziale (in byte).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351105(v=exchg.10).md">cbMaxExtent</a></td>
<td>Ottiene o imposta il valore che imposta il limite massimo di ulGrowth. Questo valore è in byte.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351104(v=exchg.10).md">cbMinExtent</a></td>
<td>Ottiene o imposta il valore che esegue l'override di ulGrowth se troppo piccolo. Questo valore è in byte.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351068(v=exchg.10).md">grbit</a></td>
<td>Ottiene o imposta le opzioni degli hint di spazio.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351069(v=exchg.10).md">ulGrowth</a></td>
<td>Ottiene o imposta la percentuale di crescita dell'ultima crescita o dimensione iniziale (possibilmente arrotondata alla dimensione di allocazione JET nativa più vicina). I valori validi sono 0 e [100, 50000).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351070(v=exchg.10).md">ulInitialDensity</a></td>
<td>Ottiene o imposta la densità in corrispondenza del layout (aggiunta).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351071(v=exchg.10).md">ulMaintDensity</a></td>
<td>Ottiene o imposta la densità in base alla quale eseguire la manutenzione.</td>
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
<td><a href="dn351097(v=exchg.10).md">ContentEquals</a></td>
<td>Restituisce un valore che indica se questa istanza è uguale a un'altra istanza di .</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn351100(v=exchg.10).md">DeepClone</a></td>
<td>Restituisce una copia completa dell'oggetto .</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalizza</a></td>
<td>Ereditato <a href="/dotnet/api/system.object">dall'oggetto</a>.</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn351066(v=exchg.10).md">ToString</a></td>
<td>Generare una rappresentazione di stringa dell'istanza di . Esegue l'override <a href="/dotnet/api/system.object.tostring#System_Object_ToString">di Object.ToString().</a></td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[JET_SPACEHINTS classe](./jet-spacehints-class.md)

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
