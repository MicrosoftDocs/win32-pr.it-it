---
description: 'Altre informazioni su: Enumerazione ColumndefGrbit'
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
ms.openlocfilehash: d2c94dcf7d454c5f0ea11fcee0bd46655099dfd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308575"
---
# <a name="columndefgrbit-enumeration"></a>Enumerazione ColumndefGrbit

Opzioni per la struttura JET_COLUMNDEF.

Questa enumerazione ha un attributo [FlagsAttribute](/dotnet/api/system.flagsattribute) che consente una combinazione bit per bit dei valori del relativo membro.

**Spazio dei nomi:**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly:**  Microsoft. ISAM. esent. Interop (in Microsoft.Isam.Esent.Interop.dll)

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
<td>La colonna verrà corretta. Utilizzerà sempre la stessa quantità di spazio in una riga, indipendentemente dalla quantità di dati archiviati nella colonna. Non è possibile usare ColumnFixed con ColumnTagged. Non è possibile usare questo bit con valori Long (ovvero JET_coltyp. LongText e JET_coltyp. LongBinary).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnTagged</td>
<td>La colonna verrà contrassegnata con tag. Se non contengono dati, le colonne con tag non utilizzano alcuno spazio nel database. Non è possibile usare questo bit con ColumnFixed.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnNotNULL</td>
<td>La colonna non deve mai essere impostata su un valore NULL. In Windows XP questa operazione può essere applicata solo a colonne fisse (bit, byte, Integer e così via).</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnVersion</td>
<td>La colonna è una colonna della versione che specifica la versione della riga. Il valore di questa colonna inizia da zero e verrà incrementato automaticamente per ogni aggiornamento nella riga. Questa opzione può essere applicata solo a JET_coltyp. Colonne lunghe. Questa opzione non può essere usata con ColumnAutoincrement, ColumnEscrowUpdate o ColumnTagged.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnAutoincrement</td>
<td>La colonna verrà incrementata automaticamente. Il numero è un numero crescente ed è garantito che sia univoco all'interno di una tabella. I numeri, tuttavia, potrebbero non essere continui. Se, ad esempio, vengono inserite cinque righe in una tabella, la &quot; colonna AutoIncrement &quot; potrebbe contenere i valori {1, 2, 6, 7, 8}. Questo bit può essere utilizzato solo su colonne di tipo JET_coltyp. Long o JET_coltyp. Valuta.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnMultiValued</td>
<td>La colonna può essere multivalore. Una colonna multivalore può avere zero, uno o più valori associati. I vari valori in una colonna multivalore sono identificati da un numero denominato membro itagSequence, che appartiene a diverse strutture, tra cui: JET_RETINFO, JET_SETINFO, JET_SETCOLUMN, JET_RETRIEVECOLUMN e JET_ENUMCOLUMNVALUE. Le colonne multivalore devono essere contrassegnate come colonne; ovvero non possono essere colonne a lunghezza fissa o a lunghezza variabile.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnEscrowUpdate</td>
<td>Specifica che una colonna è una colonna di aggiornamento del deposito. Una colonna di aggiornamento del deposito può essere aggiornata simultaneamente da diverse sessioni con JetEscrowUpdate e manterrà la coerenza transazionale. Una colonna di aggiornamento del deposito deve soddisfare anche le condizioni seguenti: una colonna di aggiornamento del deposito può essere creata solo quando la tabella è vuota. Una colonna di aggiornamento del deposito vincolata deve essere di tipo JET_coltypLong. Una colonna di aggiornamento del deposito deve avere un valore predefinito. Non è possibile usare JET_bitColumnEscrowUpdate insieme a ColumnTagged, ColumnVersion o ColumnAutoincrement.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUnversioned</td>
<td>La colonna verrà creata in un oggetto senza informazioni sulla versione. Ciò significa che le altre transazioni che tentano di aggiungere una colonna con lo stesso nome avranno esito negativo. Questo bit è utile solo con JetAddColumn. Non può essere utilizzato all'interno di una transazione.</td>
</tr>
<tr class="even">
<td></td>
<td>ColumnMaybeNull</td>
<td>Quando si esegue una outer join, è possibile che l'operazione di recupero colonna non corrisponda a quella della tabella interna.</td>
</tr>
<tr class="odd">
<td></td>
<td>ColumnUserDefinedDefault</td>
<td>Il valore predefinito per una colonna verrà fornito da una funzione di callback. Una colonna con un valore predefinito definito dall'utente deve essere una colonna con tag. Specificando JET_bitColumnUserDefinedDefault significa che pvDefault deve puntare a una struttura di JET_USERDEFINEDDEFAULT e cbDefault deve essere impostato su sizeof (JET_USERDEFINEDDEFAULT).</td>
</tr>
<tr class="even">
<td></td>
<td>TTKey</td>
<td>La colonna sarà una colonna chiave per la tabella temporanea. L'ordine delle definizioni di colonna con questa opzione specificata nella matrice di input determinerà la precedenza di ogni colonna chiave per la tabella temporanea. La prima definizione di colonna nella matrice con questo set di opzioni sarà la colonna chiave più significativa e così via. Se sono richieste più colonne chiave che possono essere supportate dal motore di database, questa opzione viene ignorata per le colonne chiave non supportate.</td>
</tr>
<tr class="odd">
<td></td>
<td>TTDescending</td>
<td>Il tipo di ordinamento della colonna chiave per la tabella temporanea deve essere decrescente anziché crescente. Se questa opzione viene specificata senza TTKey, questa opzione viene ignorata.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Vedi anche

#### <a name="reference"></a>Riferimento

[Spazio dei nomi Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

[ColumnCompressed](./windows7grbits.columncompressed-field.md)
