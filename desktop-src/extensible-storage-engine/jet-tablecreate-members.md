---
description: 'Altre informazioni su: membri JET_TABLECREATE'
title: Membri JET_TABLECREATE
TOCTitle: JET_TABLECREATE members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.JET_TABLECREATE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_tablecreate_members(v=EXCHG.10)
ms:contentKeyID: 55103926
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 7f08d8fe464aec1ccf1eff51598ff8ef506d8707
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104559282"
---
# <a name="jet_tablecreate-members"></a>Membri JET_TABLECREATE

Includi membri protetti  
Includi membri ereditati  

Contiene le informazioni necessarie per creare una tabella in un database ESE. Contiene le informazioni necessarie per creare una tabella in un database ESE.

Il tipo di [JET_TABLECREATE](./jet-tablecreate-class.md) espone i membri seguenti.

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
<td><a href="dn351074(v=exchg.10).md">JET_TABLECREATE</a></td>
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
<td><a href="dn351077(v=exchg.10).md">cbSeparateLV</a></td>
<td>Ottiene o imposta la dimensione euristica per separare un valore LV intrinseco dal record primario.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351078(v=exchg.10).md">cbtyp</a></td>
<td>Ottiene o imposta un tipo della funzione di callback.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351080(v=exchg.10).md">cColumns</a></td>
<td>Ottiene o imposta il numero di colonne da creare.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351079(v=exchg.10).md">Creata</a></td>
<td>Ottiene o imposta il numero di oggetti creati (colonne + tabella + indici + callback).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351081(v=exchg.10).md">cIndexes</a></td>
<td>Ottiene o imposta il numero di indici da creare.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351082(v=exchg.10).md">grbit</a></td>
<td>Ottiene o imposta le opzioni della tabella.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351087(v=exchg.10).md">pLVSpacehints</a></td>
<td>Ottiene o imposta gli hint per l'allocazione, la manutenzione e l'utilizzo dello spazio per l'albero BT separato, di tipo <a href="dn351095(v=exchg.10).md">JET_SPACEHINTS</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351083(v=exchg.10).md">pSeqSpacehints</a></td>
<td>Ottiene o imposta gli hint per l'allocazione, la manutenzione e l'utilizzo dello spazio per l'indice sequenziale predefinito.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351086(v=exchg.10).md">rgcolumncreate</a></td>
<td>Ottiene o imposta una matrice di informazioni sulla creazione di colonne, di tipo <a href="dn335028(v=exchg.10).md">JET_COLUMNCREATE</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351089(v=exchg.10).md">rgindexcreate</a></td>
<td>Ottiene o imposta una matrice di indici da creare, di tipo <a href="dn335112(v=exchg.10).md">JET_INDEXCREATE</a>.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351090(v=exchg.10).md">szCallback</a></td>
<td>Ottiene o imposta una funzione di callback da utilizzare per la tabella. Si tratta del modulo &quot; module! functionname &quot; e presuppone il codice non gestito. Per un'alternativa, vedere <strong>JetRegisterCallback (JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)</strong> .</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351092(v=exchg.10).md">szTableName</a></td>
<td>Ottiene o imposta il nome della tabella da creare.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351093(v=exchg.10).md">szTemplateTableName</a></td>
<td>Ottiene o imposta il nome della tabella da cui ereditare DDL di base.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351099(v=exchg.10).md">TableID</a></td>
<td>Ottiene o imposta l'oggetto tabledid restituito.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351101(v=exchg.10).md">ulDensity</a></td>
<td>Ottiene o imposta la densità della tabella.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Proprietà pubblica" alt="Public property" /></td>
<td><a href="dn351102(v=exchg.10).md">ulPages</a></td>
<td>Ottiene o imposta le pagine iniziali da allocare per la tabella.</td>
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
<td><a href="dn351122(v=exchg.10).md">ContentEquals</a></td>
<td>Restituisce un valore che indica se questa istanza è uguale a un'altra istanza.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn351123(v=exchg.10).md">DeepClone</a></td>
<td>Restituisce una copia completa dell'oggetto.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">È uguale a</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Metodo protetto" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.finalize#System_Object_Finalize">Finalize</a></td>
<td>Ereditato da <a href="/dotnet/api/system.object">Object</a>.</td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Metodo pubblico" alt="Public method" /></td>
<td><a href="dn351076(v=exchg.10).md">ToString</a></td>
<td>Generare una rappresentazione di stringa dell'istanza. Esegue l'override di <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object. ToString ()</a>.</td>
</tr>
</tbody>
</table>


Inizio

## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Classe JET_TABLECREATE](./jet-tablecreate-class.md)

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
