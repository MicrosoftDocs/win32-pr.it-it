---
description: Il WMI Query Language (WQL) è un subset del American National Standards Institute Structured Query Language (ANSI SQL)&\# 8212; con modifiche semantiche secondarie. Nella tabella seguente sono elencate le parole chiave WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL per WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c9a1a3b0db3f383bd8ba44aeb1e433b5aab02b4e9b4773ea221e1a0254ae037
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117738820"
---
# <a name="wql-sql-for-wmi"></a>WQL (SQL per WMI)

Il WMI Query Language (WQL) è un subset del American National Standards Institute Structured Query Language (ANSI SQL) con modifiche semantiche secondarie. Nella tabella seguente sono elencate le parole chiave WQL.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Parola chiave WQL</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AND<br/></td>
<td>Combina due espressioni booleane e restituisce <strong>TRUE quando</strong> entrambe le espressioni sono <strong>TRUE.</strong><br/></td>
</tr>
<tr class="even">
<td><a href="associators-of-statement.md">ASSOCIATORI DI</a></td>
<td>Recupera tutte le istanze associate a un'istanza di origine.<br/> Usare questa istruzione con query di schema e query di dati.<br/></td>
</tr>
<tr class="odd">
<td><a href="--class-identifier.md">__CLASS</a></td>
<td>Fa riferimento alla classe dell'oggetto in una query.<br/></td>
</tr>
<tr class="even">
<td>FROM<br/></td>
<td>Specifica la classe che contiene le proprietà elencate in un'istruzione SELECT. Windows Strumentazione gestione (WMI) supporta le query di dati da una sola classe alla volta.<br/></td>
</tr>
<tr class="odd">
<td><a href="group-clause.md">Clausola GROUP</a></td>
<td>Fa in modo che WMI generi una notifica per rappresentare un gruppo di eventi.<br/> Usare questa clausola con query di eventi.<br/></td>
</tr>
<tr class="even">
<td><a href="having-clause.md">HAVING</a></td>
<td>Filtra gli eventi ricevuti durante l'intervallo di raggruppamento specificato nella <a href="within-clause.md">clausola WITHIN.</a><br/></td>
</tr>
<tr class="odd">
<td><a href="wql-operators.md">IS</a></td>
<td>Operatore di confronto usato con NOT e <strong>NULL.</strong> La sintassi per questa istruzione è la seguente:<br/> IS [NOT] <strong>NULL</strong><br/> (dove NOT è facoltativo)<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">ISA</a></td>
<td>Operatore che applica una query alle sottoclassi di una classe specificata. Per altre informazioni, vedere <a href="isa-operator-for-event-queries.md">Operatore ISA per query di</a>eventi, <a href="isa-operator-for-data-queries.md">Operatore ISA</a>per query di dati e <a href="isa-operator-for-schema-queries.md">Operatore ISA per query di schema.</a><br/></td>
</tr>
<tr class="odd">
<td>KEYSONLY<br/></td>
<td>Utilizzato nelle query <a href="references-of-statement.md">REFERENCES OF</a> e <a href="associators-of-statement.md">ASSOCIATORS OF</a> per garantire che le istanze risultanti siano popolate solo con le chiavi delle istanze, riducendo così l'overhead della chiamata.<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">LIKE</a></td>
<td>Operatore che determina se una determinata stringa di caratteri corrisponde a un criterio specificato.<br/></td>
</tr>
<tr class="odd">
<td>NOT<br/></td>
<td>Operatore di confronto che utilizza in una query WQL SELECT, ad esempio:<br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>Indica che a un oggetto non è assegnato un valore in modo esplicito. <strong>NULL</strong> non equivale a zero (0) o vuoto.<br/></td>
</tr>
<tr class="odd">
<td>OR<br/></td>
<td>Combina due condizioni.<br/> Quando in un'istruzione viene usato più di un operatore logico, gli operatori OR vengono valutati dopo gli operatori AND.<br/></td>
</tr>
<tr class="even">
<td><a href="references-of-statement.md">RIFERIMENTI DI</a></td>
<td>Recupera tutte le istanze di associazione che fanno riferimento a un'istanza di origine specifica. Usare questa istruzione con query di schema e dati. <a href="references-of-statement.md">L'istruzione REFERENCES OF</a> è simile all'istruzione <a href="associators-of-statement.md">ASSOCIATORS OF.</a> Tuttavia, non recupera le istanze dell'endpoint. recupera le istanze di associazione.<br/></td>
</tr>
<tr class="odd">
<td>SELECT<br/></td>
<td>Specifica le proprietà utilizzate in una query.<br/> Per altre informazioni, vedere <a href="select-statement-for-data-queries.md">Istruzione SELECT per query di dati,</a>Istruzione SELECT per query <a href="select-statement-for-event-queries.md">di</a>eventi o Istruzione SELECT per query <a href="select-statement-for-schema-queries.md">di schema.</a><br/></td>
</tr>
<tr class="even">
<td><strong>TRUE</strong></td>
<td>Operatore booleano che restituisce -1 (meno uno).<br/></td>
</tr>
<tr class="odd">
<td><a href="where-clause.md">WHERE</a></td>
<td>Restringe l'ambito di una query di dati, eventi o schema.<br/></td>
</tr>
<tr class="even">
<td><a href="within-clause.md">WITHIN</a></td>
<td>Specifica un intervallo di polling o di raggruppamento.<br/> Usare questa clausola con query di eventi.<br/></td>
</tr>
<tr class="odd">
<td>FALSE<br/></td>
<td>Operatore booleano che restituisce 0 (zero).</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> L'uso di una parola chiave WQL come nome di oggetto può comportare una query che non può essere analizzata anche quando la query viene compilata senza errori.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operatori WQL](wql-operators.md)
</dt> <dt>

[Formati di data supportati da WQL](wql-supported-date-formats.md)
</dt> <dt>

[Formati di ora supportati da WQL](wql-supported-time-formats.md)
</dt> </dl>

 

 




