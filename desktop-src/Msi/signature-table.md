---
description: La tabella Signature contiene le informazioni che identificano in modo univoco una firma di file. Per altre informazioni sulle firme, vedere Firme digitali e Windows programma di installazione.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Tabella delle firme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5ddda5c501b24e12498f356c10a1aa2a3549426daca5e4cc3c19c1f62ed04cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118624648"
---
# <a name="signature-table"></a>Tabella delle firme

La tabella Signature contiene le informazioni che identificano in modo univoco una firma di file. Per altre informazioni sulle firme, vedere [Firme digitali e Windows programma di installazione.](digital-signatures-and-windows-installer.md)

La tabella Signature include le colonne seguenti.



| Colonna     | Tipo                               | Chiave | Nullable |
|------------|------------------------------------|-----|----------|
| Firma  | [Identificatore](identifier.md)       | S   | N        |
| FileName   | [Text](text.md)                   | N   | N        |
| Versione minima | [Text](text.md)                   | N   | S        |
| MaxVersion | [Text](text.md)                   | N   | S        |
| MinSize    | [DoubleInteger](doubleinteger.md) | N   | S        |
| MaxSize    | [DoubleInteger](doubleinteger.md) | N   | S        |
| MinDate    | [DoubleInteger](doubleinteger.md) | N   | S        |
| Maxdate    | [DoubleInteger](doubleinteger.md) | N   | S        |
| Linguaggi  | [Text](text.md)                   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Firma
</dt> <dd>

La colonna Firma è una firma di file univoca.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>Filename
</dt> <dd>

Nome del file.

</dd> <dt>

<span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>Versione minima
</dt> <dd>

Versione minima del file, con un confronto tra le lingue. Se questo campo viene specificato, il file deve avere una versione almeno uguale a MinVersion. Se il file ha una versione uguale al valore del campo MinVersion ma la lingua specificata nella colonna Languages è diversa, il file non soddisfa i criteri di filtro della firma.

> [!Note]  
> La lingua specificata nella colonna Lingue viene utilizzata nel confronto e non è possibile ignorare la lingua. Se si vuole che un file soddisfi il requisito del campo MinVersion indipendentemente dalla lingua, è necessario immettere un valore nel campo MinVersion minore di uno rispetto al valore effettivo. Ad esempio, se la versione minima per il filtro è 2.0.2600.1183, usare 2.0.2600.1182 per trovare il file senza corrispondenze con le informazioni sulla lingua.

 

</dd> <dt>

<span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion
</dt> <dd>

Versione massima del file. Se questo campo viene specificato, il file deve avere una versione al massimo uguale a MaxVersion.

</dd> <dt>

<span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize
</dt> <dd>

Dimensione minima del file. Se questo campo viene specificato, le dimensioni del file in esame devono essere almeno uguali a MinSize. Deve essere un numero non negativo.

</dd> <dt>

<span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>Maxsize
</dt> <dd>

Dimensione massima del file. Se questo campo viene specificato, le dimensioni del file in esame devono essere al massimo uguali a MaxSize. Deve essere un numero non negativo.

</dd> <dt>

<span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate
</dt> <dd>

Data e ora minime di modifica del file. Se questo campo viene specificato, il file in esame deve avere una data e un'ora di modifica almeno uguali a MinDate. Deve essere un numero non negativo. Il formato di questo campo è due valori a 16 bit di tipo **WORD.** Il valore **WORD di ordine** elevato specifica la data nel formato di data MS-DOS. Il valore **WORD di ordine** basso specifica l'ora nel formato ora MS-DOS. Il valore 0 per il valore dell'ora rappresenta la mezzanotte. Vedere la sezione relativa alle osservazioni.

</dd> <dt>

<span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>Maxdate
</dt> <dd>

Data massima di creazione del file. Se questo campo viene specificato, il file in esame deve avere una data di creazione al massimo uguale a MaxDate. Deve essere un numero non negativo. Il formato di questo campo è due valori a 16 bit di tipo **WORD.** Il valore **WORD di ordine** elevato specifica la data nel formato di data MS-DOS. Il valore **WORD di ordine** basso specifica l'ora nel formato ora MS-DOS. Il valore 0 per il valore dell'ora rappresenta la mezzanotte. Vedere la sezione relativa alle osservazioni.

</dd> <dt>

<span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Lingue
</dt> <dd>

Lingue supportate dal file.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene usata con la [tabella AppSearch](appsearch-table.md).

La firma viene cercata usando la tabella [RegLocator](reglocator-table.md), la tabella [IniLocator](inilocator-table.md), la tabella [CompLocator](complocator-table.md)e la [tabella DrLocator](drlocator-table.md). Le colonne di questa tabella in genere non sono localizzate. Se un autore decide di cercare i prodotti in più lingue, nella tabella può essere inclusa una voce separata per ogni lingua.

La tabella Signature segue in genere le regole Windows [di controllo delle versioni dei file del programma di installazione](file-versioning-rules.md). Le lingue specificate nella colonna Languages della tabella Signature non vengono valutate a meno che le versioni del file non siano equivalenti. La colonna Lingue garantisce che un file sia di una determinata lingua se è della versione richiesta. Non è disponibile alcun metodo per ignorare la colonna Languages. Un valore NULL immesso nella colonna Languages viene considerato come un file senza una lingua e non corrisponde alla firma di un file con una lingua visualizzata nella tabella Signature. Nell'esempio seguente viene cercata una versione specifica di MSI.DLL.

[Tabella DrLocator](drlocator-table.md)

| Firma\_ | Padre | Percorso                  | Profondità |
|-------------|--------|-----------------------|-------|
| MsiDll      | {null} | c: \\ windows \\ system32 | 0     |



 

[Tabella AppSearch](appsearch-table.md)



| Proprietà | Firma\_ |
|----------|-------------|
| MSIDLL   | MsiDll      |



 

Tabella delle firme



| Firma | FileName | MinVersion    | MaxVersion | MinSize | MaxSize | MinDate | Maxdate | Linguaggi |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| MsiDll    | msi.dll  | 2.0.2600.1106 | {null}     | {null}  | {null}  | {null}  | {null}  | 0         |



 

In questo caso, e Windows XP SP1, l'azione [AppSearch](appsearch-action.md) imposta MSIDLL su c: \\ windows system32msi.dll perché MSI.DLL è un file indipendente dalla \\ \\ lingua. Se il valore della colonna Languages viene modificato da 0 a 1033, l'azione AppSearch non riesce a trovare il msi.dll corrispondente e la proprietà MSIDLL non è definita.

Non è possibile usare la tabella Signature per eseguire query solo sui linguaggi. Per cercare versioni linguistiche diverse di un file, è necessario avere una voce separata nella tabella Firma per ogni versione linguistica. Se nella colonna Lingue sono disponibili più lingue, la ricerca è un file che supporta tutte queste lingue.

Il formato delle colonne MinDate e MaxDate è di due valori a 16 bit di tipo **WORD.**

Data **WORD**



| BITS | Content                                             |
|------|-----------------------------------------------------|
| 0–4  | Giorno del mese (1-31)                             |
| 5-8  | Mese (1 = gennaio, 2 = febbraio e così via)        |
| 9-15 | Offset anno dal 1980 (aggiungere 1980 per ottenere l'anno effettivo) |



 

Time **WORD**



| BITS  | Content                     |
|-------|-----------------------------|
| 0–4   | Secondi divisi per 2        |
| 5-10  | Minuti (0-59)              |
| 11-15 | Hour(0-23 on 24 hour clock) |



 

La formula per calcolare i valori dei campi MinDate e MaxDate è:

( (Anno - 1980) \* 512 + Mese \* 32 + Giorno ) \* 65536 + Ore \* 2048 + Minuti \* 32 + Secondi/2

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



