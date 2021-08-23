---
description: Altre informazioni sull'enumerazione ColumndefGrbit
title: Enumerazione ColumndefGrbit
TOCTitle: ColumndefGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.ColumndefGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.columndefgrbit(v=EXCHG.10)
ms:contentKeyID: 39513005
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnNotNULL
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnAutoincrement
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUnversioned
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMaybeNull
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnTagged
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.None
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnMultiValued
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTDescending
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnEscrowUpdate
- Microsoft.Isam.Esent.Interop.ColumndefGrbit
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnVersion
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnFixed
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.ColumnUserDefinedDefault
- Microsoft.Isam.Esent.Interop.ColumndefGrbit.TTKey
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f2bd26a3dac291d78b101aa56f186d9b31f7a927b1eca3e29febc7773e3c0939
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119042459"
---
# <a name="columndefgrbit-enumeration"></a>Enumerazione ColumndefGrbit

Opzioni per la JET_COLUMNDEF struttura.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Sintassi

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration ColumndefGrbit
'Usage
Dim instance As ColumndefGrbit
```

``` csharp
[FlagsAttribute]
public enum ColumndefGrbit
```

## <a name="members"></a>Members

<table>
<thead>
<tr class="header">
<th></th>
<th>Nome del membro</th>
<th>Descrizione</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>nessuno</td>
<td>Opzioni predefinite.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnFixed</td>
<td>La colonna sarà fissa. Verrà sempre utilizzata la stessa quantità di spazio in una riga, indipendentemente dalla quantità di dati archiviati nella colonna. Non è possibile usare ColumnFixed con ColumnTagged. Questo bit non può essere usato con valori long ,ovvero JET_coltyp. LongText e JET_coltyp. LongBinary).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnTagged</td>
<td>La colonna verrà contrassegnata con tag. Le colonne con tag non eseranno spazio nel database se non contengono dati. Questo bit non può essere usato con ColumnFixed.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnNotNULL</td>
<td>La colonna non deve mai essere impostata su un valore NULL. In Windows XP questo può essere applicato solo a colonne fisse (bit, byte, integer e così via).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnVersion</td>
<td>La colonna è una colonna versione che specifica la versione della riga. Il valore di questa colonna inizia da zero e verrà incrementato automaticamente per ogni aggiornamento nella riga. Questa opzione può essere applicata solo a JET_coltyp. Colonne lunghe. Questa opzione non può essere usata con ColumnAutoincrement, ColumnEscrowUpdate o ColumnTagged.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnAutoincrement</td>
<td>La colonna verrà incrementata automaticamente. Il numero è un numero crescente ed è garantito come univoco all'interno di una tabella. I numeri, tuttavia, potrebbero non essere continui. Ad esempio, se vengono inserite cinque righe in una tabella, la colonna dell'incrementale automatico potrebbe contenere i valori &quot; &quot; { 1, 2, 6, 7, 8 }. Questo bit può essere usato solo su colonne di tipo JET_coltyp. Long o JET_coltyp. Valuta.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnMultiValued</td>
<td>La colonna può essere multivalore. A una colonna multivalore possono essere associati zero, uno o più valori. I vari valori in una colonna multivalore sono identificati da un numero denominato membro itagSequence, che appartiene a varie strutture, tra cui: JET_RETINFO, JET_SETINFO, JET_SETCOLUMN, JET_RETRIEVECOLUMN e JET_ENUMCOLUMNVALUE. Le colonne multivalore devono essere colonne con tag. non possono essere colonne a lunghezza fissa o a lunghezza variabile.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnEscrowUpdate</td>
<td>Specifica che una colonna è una colonna di aggiornamento del deposito. Una colonna di aggiornamento del deposito può essere aggiornata simultaneamente da sessioni diverse con JetEscrowUpdate e manterrà la coerenza transazionale. Anche una colonna di aggiornamento del deposito deve soddisfare le condizioni seguenti: è possibile creare una colonna di aggiornamento del deposito solo quando la tabella è vuota. Una colonna di aggiornamento del deposito deve essere di tipo JET_coltypLong. Una colonna di aggiornamento del deposito deve avere un valore predefinito. JET_bitColumnEscrowUpdate non può essere usato in combinazione con ColumnTagged, ColumnVersion o ColumnAutoincrement.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUnversioned</td>
<td>La colonna verrà creata in un oggetto senza informazioni sulla versione. Ciò significa che le altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo. Questo bit è utile solo con JetAddColumn. Non può essere utilizzato all'interno di una transazione.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnMaybeNull</td>
<td>Durante l'outer join, l'operazione di recupero colonna potrebbe non avere una corrispondenza dalla tabella interna.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUserDefinedDefault</td>
<td>Il valore predefinito per una colonna verrà fornito da una funzione di callback. Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag. Specificare JET_bitColumnUserDefinedDefault indica che pvDefault deve puntare a una struttura JET_USERDEFINEDDEFAULT e cbDefault deve essere impostato su sizeof( JET_USERDEFINEDDEFAULT ).</td>
</tr>
<tr class="even">
<td></td>
<td>TTKey</td>
<td>La colonna sarà una colonna chiave per la tabella temporanea. L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea. La prima definizione di colonna nella matrice con questa opzione impostata sarà la colonna chiave più significativa e così via. Se vengono richieste più colonne chiave di quelle supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</td>
</tr>
<tr class="odd">
<td></td>
<td>TTDescending</td>
<td>L'ordinamento della colonna chiave per la tabella temporanea deve essere decrescente anziché crescente. Se questa opzione viene specificata senza TTKey, questa opzione viene ignorata.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)

[ColumnCompressed](./windows7grbits.columncompressed-field.md)
