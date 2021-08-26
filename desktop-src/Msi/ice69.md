---
description: ICE69 verifica che tutte le sottostringhe nel formato $componentkey all'interno di una stringa formattata non facciano riferimento \[ \] incrociato ai componenti.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 183a62989ff39387639af1a9e1feeeddc3e0567f28915ca3857ba6dd5f58f68c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043941"
---
# <a name="ice69"></a>ICE69

ICE69 verifica che tutte le sottostringhe nel formato $componentkey all'interno di una stringa formattata non facciano riferimento \[ \] incrociato ai componenti. [](formatted.md) Un riferimento tra componenti si verifica quando la proprietà $componentkey di una stringa formattata fa riferimento a un componente diverso dal componente archiviato nella colonna \[ \] Componente delle \_ tabelle.

I problemi relativi al riferimento tra componenti derivano dal modo in cui [vengono valutate le](formatted.md) stringhe formattate. Se il componente a cui si fa riferimento con la proprietà $componentkey è già installato e non viene modificato durante l'installazione corrente (ad esempio, viene reinstallato, spostato nell'origine e così via), l'espressione $componentkey restituisce Null, perché lo stato dell'azione del componente \[ \] in $componentkey è \[ \] \[ \] Null. Durante le operazioni di aggiornamento e ripristino possono verificarsi problemi simili.

## <a name="result"></a>Risultato

ICE69 restituisce un errore se una sottostringa $componentkey all'interno di una stringa formattata fa riferimento incrociato a un \[ \] componente in un'altra funzionalità. [](formatted.md) ICE69 restituisce un avviso se $componentkey sottostringa all'interno di una stringa formattata fa riferimento incrociato \[ a un componente nella stessa \] funzionalità. Per determinare questo mapping viene usata la tabella [FeatureComponents.](featurecomponents-table.md) Deve eseguire il mapping alla stessa funzionalità per l'avviso. Il riferimento ai componenti nelle funzionalità padre o ai componenti nelle funzionalità figlio è considerato un errore.

ICE69 segnala un errore se la \[ \# \] sottostringa [](formatted.md) [](file-table.md) FileKey all'interno di una stringa formattata fa riferimento a un file non specificato nella tabella File come appartenente allo stesso componente.

## <a name="example"></a>Esempio

Ice69 segnala quanto segue per gli esempi illustrati.

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

Per correggere l'errore, non fare riferimento incrociato ai componenti. Modificare il \[ $componentkey in modo che corrisponda al componente del \] collegamento.

[Tabella dei collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Componente\_ | Argomento     |
|-----------|-------------|--------------|
| Test      | Quicktest   | -v \[ $Test\] |
| Collegamento2 | Quicktest   | \[$Test 2\]   |



 

Le [tabelle Verb](verb-table.md) ed [Extension](extension-table.md) sono casi speciali in cui la tabella Verb fa riferimento a un'estensione appartenente a un componente. Un'estensione, tuttavia, può appartenere a più componenti perché la chiave primaria per la tabella di estensione è costituito da estensione e componente \_ colonne. Logicamente, è possibile avere la situazione seguente.

[Tabella verbi](verb-table.md) (parziale)



| Estensione | Verbo\_ | Argomento                |
|-----------|--------|-------------------------|
| Tst       | apre   | -v \[ $comp 1 \] \[ $comp 2\] |



 

[Tabella delle estensioni](extension-table.md) (parziale)



| Estensione | Componente\_ |
|-----------|-------------|
| Tst       | comp1       |
| Tst       | comp2       |



 

[Tabella FeatureComponents](featurecomponents-table.md)



| Funzionalità\_ | Componente\_ |
|-----------|-------------|
| Funzionalità1  | Quicktest   |
| Funzionalità1  | Test        |
| Funzionalità2  | Test2       |



 

In questo caso, è necessario assicurarsi che almeno una delle proprietà $componentkey \[ \] restituirà un valore non Null. Tuttavia, ogni proprietà $componentkey nella colonna Argument della tabella \[ \] Verbo ( \[ $comp 1 \] \[ e $comp 2 nell'esempio precedente) deve fare riferimento \] a un possibile componente incluso con l'estensione associata al verbo. Un riferimento come \[ $comp 3 \] genererebbe un avviso da ICE69.

La [tabella AppId](appid-table.md) presenta una situazione simile alla tabella Verbo. Usa la tabella [Class per il](class-table.md) riferimento al componente. In questo caso, la tabella AppId viene convalidata nello stesso modo della convalida Verb-Extension(ora AppId-Class).

La colonna Argument della tabella Class viene convalidata come [shortcut,](shortcut-table.md) [Registry](registry-table.md)e tabelle simili.

## <a name="table-used-during-execution-only-if-found"></a>Tabella utilizzata durante l'esecuzione (solo se trovata)

[IniFile](inifile-table.md)

[RemoveIniFile](removeinifile-table.md)

[Registro](registry-table.md)

[RemoveRegistry](removeregistry-table.md)

[ServiceControl](servicecontrol-table.md)

[ServiceInstall](serviceinstall-table.md)

[Scelte rapide](shortcut-table.md)

[Verbo](verb-table.md)

[Estensione](extension-table.md)

[Classe](class-table.md)

[Appid](appid-table.md)

[Environment](environment-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni di riferimento su ICE](ice-reference.md)
</dt> </dl>

 

 



