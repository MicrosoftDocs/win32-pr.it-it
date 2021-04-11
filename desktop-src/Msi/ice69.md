---
description: ICE69 verifica che tutte le sottostringhe del form \[ $componentkey \] all'interno di una stringa formattata non rimandino i componenti.
ms.assetid: 6ab8f3b7-19e9-46f3-b09e-36bdb43d6f55
title: ICE69
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 95bd00efc6b141bfa872470adcc9e88a63a2c52d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233158"
---
# <a name="ice69"></a>ICE69

ICE69 verifica che tutte le sottostringhe del form \[ $componentkey \] all'interno di una stringa [formattata](formatted.md) non rimandino i componenti. Un riferimento tra componenti si verifica quando la \[ \] Proprietà $componentkey di una stringa formattata fa riferimento a un componente diverso dal componente archiviato nella \_ colonna componente delle tabelle.

I problemi relativi al riferimento tra componenti si verificano dal modo in cui vengono valutate le stringhe [formattate](formatted.md) . Se il componente a cui si fa riferimento con la \[ \] Proprietà $componentkey è già installato e non viene modificato durante l'installazione corrente (ad esempio, in fase di reinstallazione, spostato nell'origine e così via), l'espressione \[ $componentkey \] restituisce null, perché lo stato dell'azione del componente in \[ $componentkey \] è null. Problemi simili possono verificarsi durante le operazioni di aggiornamento e ripristino.

## <a name="result"></a>Risultato

ICE69 restituisce un errore se una \[ \] sottostringa $componentkey all'interno di una stringa [formattata](formatted.md) fa riferimento a un componente in un'altra funzionalità. ICE69 restituisce un avviso se una \[ \] sottostringa $componentkey all'interno di una stringa formattata fa riferimento a un componente nella stessa funzionalità. La tabella [FeatureComponents](featurecomponents-table.md) viene utilizzata per determinare questo mapping. Deve eseguire il mapping alla stessa funzionalità per l'avviso. Il riferimento ai componenti nelle funzionalità padre o ai componenti di riferimento nelle funzionalità figlio viene considerato un errore.

ICE69 segnala un errore se la \[ \# \] sottostringa FileKey all'interno di una stringa [formattata](formatted.md) fa riferimento a un file non specificato nella tabella [file](file-table.md) come appartenente allo stesso componente.

## <a name="example"></a>Esempio

ICE69 segnala gli esempi riportati di seguito.

``` syntax
WARNING: "Mismatched component reference. Entry 'Test' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test'. Components are in the same feature."
ERROR: "Mismatched component reference. Entry 'Shortcut2' of the Shortcut table belongs to component 'QuickTest'. However, the formatted string in column 'Argument' references component 'Test2'. Components are not in the same feature."
```

Per correggere l'errore, non fare riferimento a componenti incrociati. Modificare il \[ $componentkey \] in modo che corrisponda al componente del collegamento.

[Tabella collegamenti](shortcut-table.md) (parziale)



| Tasto di scelta rapida  | Componente\_ | Argomento     |
|-----------|-------------|--------------|
| Test      | QuickTest   | -v \[ $test\] |
| Shortcut2 | QuickTest   | \[$Test 2\]   |



 

Le tabelle dei [verbi](verb-table.md) e delle [estensioni](extension-table.md) sono casi speciali in quanto la tabella dei verbi fa riferimento a un'estensione che appartiene a un componente. Un'estensione, tuttavia, può appartenere a più componenti perché la chiave primaria per la tabella di estensione è costituita dalle colonne Extension e Component \_ . È possibile che si verifichino logicamente le situazioni seguenti.

[Tabella Verb](verb-table.md) (parziale)



| Estensione | Verbo\_ | Argomento                |
|-----------|--------|-------------------------|
| TST       | apre   | -v \[ $comp 1 \] \[ $comp 2\] |



 

[Tabella di estensione](extension-table.md) (parziale)



| Estensione | Componente\_ |
|-----------|-------------|
| TST       | Comp1       |
| TST       | Comp2       |



 

[Tabella FeatureComponents](featurecomponents-table.md)



| Funzionalità\_ | Componente\_ |
|-----------|-------------|
| Feature1  | QuickTest   |
| Feature1  | Test        |
| Funzionalità2  | Test2       |



 

In questo caso, è necessario assicurarsi che almeno una delle \[ \] Proprietà $componentkey restituisca un valore non null. Ogni \[ $componentkey \] proprietà nella colonna Argument della tabella Verb ( \[ $comp 1 \] e \[ $comp 2 \] nell'esempio precedente), tuttavia, deve fare riferimento a un componente possibile incluso con l'estensione associata al verbo. Un riferimento come \[ $COMP 3 \] genera un avviso da ICE69.

La [tabella AppID](appid-table.md) presenta una situazione simile alla tabella dei verbi. Usa la [tabella delle classi](class-table.md) per il riferimento al componente. In questo caso, la tabella AppId viene convalidata allo stesso modo della convalida Verb-Extension (ora AppId-Class).

La colonna Argument della tabella della classe viene convalidata come il [collegamento](shortcut-table.md), il [Registro di sistema](registry-table.md)e tabelle simili.

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

[AppId](appid-table.md)

[Environment](environment-table.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento ghiaccio](ice-reference.md)
</dt> </dl>

 

 



