---
description: La tabella Signature include le informazioni che identificano in modo univoco una firma del file. Per altre informazioni sulle firme, vedere firme digitali e Windows Installer.
ms.assetid: 4780356f-e02a-45d9-883c-4f84867dbdea
title: Tabella di firma
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: efb75155c4c7b8ddf4a82706bc38f09d0af75260
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314196"
---
# <a name="signature-table"></a>Tabella di firma

La tabella Signature include le informazioni che identificano in modo univoco una firma del file. Per altre informazioni sulle firme [, vedere firme digitali e Windows Installer](digital-signatures-and-windows-installer.md).

La tabella Signature contiene le colonne seguenti.



| Colonna     | Tipo                               | Chiave | Nullable |
|------------|------------------------------------|-----|----------|
| Firma  | [Identificatore](identifier.md)       | S   | N        |
| FileName   | [Text](text.md)                   | N   | N        |
| MinVersion | [Text](text.md)                   | N   | S        |
| MaxVersion | [Text](text.md)                   | N   | S        |
| MinSize    | [DoubleInteger](doubleinteger.md) | N   | S        |
| MaxSize    | [DoubleInteger](doubleinteger.md) | N   | S        |
| MinDate    | [DoubleInteger](doubleinteger.md) | N   | S        |
| MaxDate    | [DoubleInteger](doubleinteger.md) | N   | S        |
| Linguaggi  | [Text](text.md)                   | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Firma
</dt> <dd>

La colonna Signature è una firma di file univoca.

</dd> <dt>

<span id="FileName"></span><span id="filename"></span><span id="FILENAME"></span>FileName
</dt> <dd>

Nome del file.

</dd> <dt>

<span id="MinVersion"></span><span id="minversion"></span><span id="MINVERSION"></span>MinVersion
</dt> <dd>

Versione minima del file, con un confronto di lingua. Se questo campo è specificato, la versione del file deve essere almeno uguale a MinVersion. Se il file ha una versione uguale al valore del campo MinVersion ma la lingua specificata nella colonna Languages è diversa, il file non soddisfa i criteri di filtro della firma.

> [!Note]  
> Il linguaggio specificato nella colonna lingue viene utilizzato nel confronto e non è possibile ignorare la lingua. Se si vuole che un file soddisfi il requisito di campo MinVersion indipendentemente dalla lingua, è necessario immettere un valore nel campo MinVersion, che corrisponde a uno minore del valore effettivo. Se, ad esempio, la versione minima del filtro è 2.0.2600.1183, utilizzare 2.0.2600.1182 per trovare il file senza corrispondenti alle informazioni sulla lingua.

 

</dd> <dt>

<span id="MaxVersion"></span><span id="maxversion"></span><span id="MAXVERSION"></span>MaxVersion
</dt> <dd>

Versione massima del file. Se questo campo è specificato, il file deve avere una versione maggiore o uguale a MaxVersion.

</dd> <dt>

<span id="MinSize"></span><span id="minsize"></span><span id="MINSIZE"></span>MinSize
</dt> <dd>

Dimensioni minime del file. Se questo campo è specificato, il file in ispezione deve avere una dimensione almeno uguale a MinSize. Deve essere un numero non negativo.

</dd> <dt>

<span id="MaxSize"></span><span id="maxsize"></span><span id="MAXSIZE"></span>MaxSize
</dt> <dd>

Dimensione massima del file. Se viene specificato questo campo, il file in ispezione deve avere una dimensione maggiore o uguale a MaxSize. Deve essere un numero non negativo.

</dd> <dt>

<span id="MinDate"></span><span id="mindate"></span><span id="MINDATE"></span>MinDate
</dt> <dd>

Data e ora di modifica minime del file. Se questo campo è specificato, il file in ispezione deve avere una data e un'ora di modifica almeno uguali a MinDe. Deve essere un numero non negativo. Il formato di questo campo è costituito da due valori a 16 bit compressi di tipo **Word**. Il valore **Word** di ordine superiore specifica la data nel formato di data MS-DOS. Il valore di **Word** di ordine inferiore specifica l'ora nel formato di ora di MS-DOS. Il valore 0 per il valore time rappresenta la mezzanotte. Vedere la sezione relativa alle osservazioni.

</dd> <dt>

<span id="MaxDate"></span><span id="maxdate"></span><span id="MAXDATE"></span>MaxDate
</dt> <dd>

Data massima di creazione del file. Se questo campo è specificato, il file in ispezione deve avere una data di creazione maggiore o uguale a MaxDate. Deve essere un numero non negativo. Il formato di questo campo è costituito da due valori a 16 bit compressi di tipo **Word**. Il valore **Word** di ordine superiore specifica la data nel formato di data MS-DOS. Il valore di **Word** di ordine inferiore specifica l'ora nel formato di ora di MS-DOS. Il valore 0 per il valore time rappresenta la mezzanotte. Vedere la sezione relativa alle osservazioni.

</dd> <dt>

<span id="Languages"></span><span id="languages"></span><span id="LANGUAGES"></span>Lingue
</dt> <dd>

Lingue supportate dal file.

</dd> </dl>

## <a name="remarks"></a>Commenti

Questa tabella viene utilizzata con la [tabella AppSearch](appsearch-table.md).

Viene eseguita la ricerca della firma utilizzando la tabella [RegLocator](reglocator-table.md), la tabella [IniLocator](inilocator-table.md), la [tabella CompLocator](complocator-table.md)e la [tabella DrLocator](drlocator-table.md). Generalmente, le colonne della tabella non sono localizzate. Se un autore decide di cercare i prodotti in più lingue, è possibile che nella tabella sia inclusa una voce separata per ogni lingua.

La tabella Signature segue in genere le [regole di controllo delle versioni dei File](file-versioning-rules.md)Windows Installer. Le lingue specificate nella colonna lingue della tabella di firma non vengono valutate a meno che le versioni dei file non siano equivalenti. La colonna lingue garantisce che un file sia di una determinata lingua se è della versione richiesta. Non è disponibile alcun metodo per ignorare la colonna lingue. Un valore NULL immesso nella colonna lingue viene considerato come un file senza una lingua e non corrisponde alla firma del file con una lingua visualizzata nella tabella della firma. Nell'esempio seguente viene eseguita la ricerca di una particolare versione di MSI.DLL.

[Tabella DrLocator](drlocator-table.md)

| Firma\_ | Padre | Percorso                  | Profondità |
|-------------|--------|-----------------------|-------|
| MsiDll      | null | c: \\ Windows \\ system32 | 0     |



 

[Tabella AppSearch](appsearch-table.md)



| Proprietà | Firma\_ |
|----------|-------------|
| MSIDLL   | MsiDll      |



 

Tabella di firma



| Firma | FileName | MinVersion    | MaxVersion | MinSize | MaxSize | MinDate | MaxDate | Linguaggi |
|-----------|----------|---------------|------------|---------|---------|---------|---------|-----------|
| MsiDll    | msi.dll  | 2.0.2600.1106 | null     | null  | null  | null  | null  | 0         |



 

In questo caso, e in Windows XP SP1, l' [azione AppSearch](appsearch-action.md) imposta MSIDLL su c: \\ Windows \\ system32 \\msi.dll perché MSI.DLL è un file indipendente dalla lingua. Se il valore della colonna languages viene modificato da 0 a 1033, l'azione AppSearch non riesce a trovare il msi.dll corrispondente e la proprietà MSIDLL non è definita.

Non è possibile usare la tabella Signature per eseguire query solo su linguaggi. Per cercare versioni in lingue diverse di un file, è necessario disporre di una voce separata nella tabella della firma per ogni versione della lingua. Se nella colonna lingue sono disponibili più lingue, la ricerca è relativa a un file che supporta tutte le lingue.

Il formato delle colonne MinDe e MaxDate è costituito da due valori a 16 bit compressi di tipo **Word**.

**Parola** data



| BITS | Content                                             |
|------|-----------------------------------------------------|
| 0 – 4  | Giorno del mese (1-31)                             |
| 5-8  | Month (1 = gennaio, 2 = febbraio e così via)        |
| 9-15 | Offset anno da 1980 (aggiungere 1980 per ottenere l'anno effettivo) |



 

**Parola** temporale



| BITS  | Content                     |
|-------|-----------------------------|
| 0 – 4   | Secondi divisi per 2        |
| 5-10  | Minuti (0-59)              |
| 11-15 | Ora (da 0 a 23 in formato 24 ore) |



 

La formula per il calcolo dei valori dei campi MinDe e MaxDate è:

((Anno-1980) \* 512 + mese \* 32 + giorno) \* 65536 + ore \* 2048 + minuti \* 32 + secondi/2

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
</dl>

 

 



