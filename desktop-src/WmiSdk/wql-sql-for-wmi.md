---
description: Il WMI Query Language (WQL) è un subset del Structured Query Language di American National Standards Institute (ANSI SQL) &\# 8212; con modifiche semantiche secondarie. Nella tabella seguente sono elencate le parole chiave WQL.
ms.assetid: 72a7ec04-9af3-41ae-9189-6e1d46803fa9
ms.tgt_platform: multiple
title: WQL (SQL per WMI)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 87498b6e8e37ab900e21eedf2c15d5cdba9f9bd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104226932"
---
# <a name="wql-sql-for-wmi"></a>WQL (SQL per WMI)

Il WMI Query Language (WQL) è un subset del Structured Query Language di American National Standards Institute (ANSI SQL) con modifiche di semantica secondarie. Nella tabella seguente sono elencate le parole chiave WQL.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>WQL (parola chiave)</th>
<th>Significato</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>AND<br/></td>
<td>Combina due espressioni booleane e restituisce <strong>true</strong> quando entrambe le espressioni sono <strong>true</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="associators-of-statement.md">ASSOCIATORI DI</a></td>
<td>Recupera tutte le istanze di associate a un'istanza di di origine.<br/> Usare questa istruzione con query di schema e query di dati.<br/></td>
</tr>
<tr class="odd">
<td><a href="--class-identifier.md">__CLASS</a></td>
<td>Fa riferimento alla classe dell'oggetto in una query.<br/></td>
</tr>
<tr class="even">
<td>FROM<br/></td>
<td>Specifica la classe che contiene le proprietà elencate in un'istruzione SELECT. Strumentazione gestione Windows (WMI) supporta le query di dati da una sola classe alla volta.<br/></td>
</tr>
<tr class="odd">
<td><a href="group-clause.md">Clausola GROUP</a></td>
<td>Causa la generazione di una notifica da parte di WMI per rappresentare un gruppo di eventi.<br/> Usare questa clausola con le query di eventi.<br/></td>
</tr>
<tr class="even">
<td><a href="having-clause.md">HAVING</a></td>
<td>Filtra gli eventi ricevuti durante l'intervallo di raggruppamento specificato nella <a href="within-clause.md">clausola all'interno</a>di.<br/></td>
</tr>
<tr class="odd">
<td><a href="wql-operators.md">IS</a></td>
<td>Operatore di confronto utilizzato con NOT e <strong>null</strong>. La sintassi per questa istruzione è la seguente:<br/> IS [NOT] <strong>null</strong><br/> (dove NOT è facoltativo)<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">ISA</a></td>
<td>Operatore che applica una query alle sottoclassi di una classe specificata. Per ulteriori informazioni, vedere <a href="isa-operator-for-event-queries.md">operatore ISA per query di evento</a>, <a href="isa-operator-for-data-queries.md">operatore ISA per query di dati</a>e <a href="isa-operator-for-schema-queries.md">operatore ISA per le query di schema</a>.<br/></td>
</tr>
<tr class="odd">
<td>KEYSONLY<br/></td>
<td>Utilizzato nei <a href="references-of-statement.md">riferimenti di</a> e <a href="associators-of-statement.md">associatori di</a> query per garantire che le istanze risultanti vengano popolate solo con le chiavi delle istanze di, riducendo l'overhead della chiamata.<br/></td>
</tr>
<tr class="even">
<td><a href="wql-operators.md">LIKE</a></td>
<td>Operatore che determina se una determinata stringa di caratteri corrisponde a un criterio specificato.<br/></td>
</tr>
<tr class="odd">
<td>NOT<br/></td>
<td>Operatore di confronto che utilizza in una query di selezione WQL, ad esempio:<br/>
<pre data-space="preserve"><code>SELECT * FROM meta_class WHERE NOT __class < &quot;Win32&quot; AND NOT __this ISA &quot;Win32_Account&quot;</code></pre></td>
</tr>
<tr class="even">
<td><strong>NULL</strong></td>
<td>Indica che un oggetto non dispone di un valore assegnato in modo esplicito. <strong>Null</strong> non è equivalente a zero (0) o vuoto.<br/></td>
</tr>
<tr class="odd">
<td>OR<br/></td>
<td>Combina due condizioni.<br/> Quando in un'istruzione viene usato più di un operatore logico, gli operatori OR vengono valutati dopo gli operatori e.<br/></td>
</tr>
<tr class="even">
<td><a href="references-of-statement.md">RIFERIMENTI DI</a></td>
<td>Recupera tutte le istanze di associazione che fanno riferimento a un'istanza di origine specifica. Usare questa istruzione con le query di schema e dati. I <a href="references-of-statement.md">riferimenti</a> <a href="associators-of-statement.md">all'istruzione sono simili a quelli dell'</a> istruzione. Tuttavia, non recupera le istanze dell'endpoint. Recupera le istanze dell'associazione.<br/></td>
</tr>
<tr class="odd">
<td>SELECT<br/></td>
<td>Specifica le proprietà utilizzate in una query.<br/> Per ulteriori informazioni, vedere istruzione <a href="select-statement-for-data-queries.md">Select per le query di dati</a>, <a href="select-statement-for-event-queries.md">istruzione SELECT per le query di evento</a>o <a href="select-statement-for-schema-queries.md">istruzione SELECT per le query dello schema</a>.<br/></td>
</tr>
<tr class="even">
<td><strong>TRUE</strong></td>
<td>Operatore booleano che restituisce-1 (meno uno).<br/></td>
</tr>
<tr class="odd">
<td><a href="where-clause.md">WHERE</a></td>
<td>Restringe l'ambito di una query di dati, eventi o schemi.<br/></td>
</tr>
<tr class="even">
<td><a href="within-clause.md">WITHIN</a></td>
<td>Specifica un intervallo di polling o di raggruppamento.<br/> Usare questa clausola con le query di eventi.<br/></td>
</tr>
<tr class="odd">
<td>FALSE<br/></td>
<td>Operatore booleano che restituisce 0 (zero).</td>
</tr>
</tbody>
</table>



 

> [!Note]  
> L'utilizzo di una parola chiave WQL come nome di oggetto può generare una query che non può essere analizzata anche quando la query viene compilata senza errori.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Operatori WQL](wql-operators.md)
</dt> <dt>

[Formati di data supportati da WQL](wql-supported-date-formats.md)
</dt> <dt>

[Formati di ora supportati da WQL](wql-supported-time-formats.md)
</dt> </dl>

 

 




