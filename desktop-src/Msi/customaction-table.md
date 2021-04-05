---
description: La tabella CustomAction fornisce i mezzi per integrare codice e dati personalizzati nell'installazione. L'origine del codice eseguito può essere un flusso contenuto all'interno del database, un file installato di recente o un file eseguibile esistente.
ms.assetid: 0f47abc1-4e06-4ddc-9ea1-9afb9f27d499
title: Tabella CustomAction
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75c8cbfa6500743e2a2ad89627447da1907f6f48
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752322"
---
# <a name="customaction-table"></a>Tabella CustomAction

La tabella CustomAction fornisce i mezzi per integrare codice e dati personalizzati nell'installazione. L'origine del codice eseguito può essere un flusso contenuto all'interno del database, un file installato di recente o un file eseguibile esistente.

La tabella CustomAction include le colonne seguenti.



| Colonna       | Tipo                               | Chiave | Nullable |
|--------------|------------------------------------|-----|----------|
| Azione       | [Identificatore](identifier.md)       | S   | N        |
| Tipo         | [Integer](integer.md)             | N   | N        |
| Source (Sorgente)       | [CustomSource](customsource.md)   | N   | S        |
| Destinazione       | [Formattato](formatted.md)         | N   | S        |
| ExtendedType | [DoubleInteger](doubleinteger.md) | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Action"></span><span id="action"></span><span id="ACTION"></span>Azione
</dt> <dd>

Nome dell'azione. L'azione viene in genere visualizzata in una tabella di sequenza, a meno che non venga chiamata da un'altra azione personalizzata. Se il nome corrisponde a qualsiasi azione incorporata, l'azione personalizzata non viene mai chiamata.

Chiave della tabella primaria.

</dd> <dt>

<span id="Type"></span><span id="type"></span><span id="TYPE"></span>Tipo
</dt> <dd>

Campo di bit di flag che specifica il tipo di base dell'azione personalizzata e delle opzioni. Vedere l' [elenco riepilogativo di tutti i tipi di azione personalizzati](summary-list-of-all-custom-action-types.md) per un elenco dei tipi di base. Vedere Opzioni di [elaborazione della restituzione](custom-action-return-processing-options.md)di azioni personalizzate, [Opzioni di pianificazione dell'esecuzione](custom-action-execution-scheduling-options.md)dell'azione personalizzata, opzione di [destinazione nascosta dell'azione](custom-action-hidden-target-option.md)personalizzata e opzioni di [esecuzione personalizzate In-Script](custom-action-in-script-execution-options.md)dell'azione.

</dd> <dt>

<span id="Source"></span><span id="source"></span><span id="SOURCE"></span>Origine
</dt> <dd>

Nome di proprietà o chiave esterna in un'altra tabella. Per una descrizione delle possibili origini azione personalizzate, vedere [origini azione personalizzate](custom-action-sources.md) e l' [elenco riepilogativo di tutti i tipi di azione personalizzata](summary-list-of-all-custom-action-types.md). Ad esempio, la colonna di origine può contenere una chiave esterna nella prima colonna di una delle tabelle seguenti contenente l'origine del codice dell'azione personalizzata.

[Tabella di directory](directory-table.md) per la chiamata di file eseguibili esistenti.

[Tabella file](file-table.md) per la chiamata di file eseguibili e dll appena installati.

[Tabella binaria](binary-table.md) per chiamare i file eseguibili, le dll e i dati archiviati nel database.

[Tabella di proprietà](property-table.md) per la chiamata di file eseguibili i cui percorsi sono contenuti in una proprietà.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Destinazione
</dt> <dd>

Parametro di esecuzione che dipende dal tipo di base dell'azione personalizzata. Per una descrizione degli elementi che devono essere immessi in questo campo per ogni tipo di azione personalizzata, vedere l' [elenco riepilogativo di tutti i tipi di azioni personalizzati](summary-list-of-all-custom-action-types.md) . Questo campo, ad esempio, può contenere quanto segue, a seconda dell'azione personalizzata.



| Destinazione                                    | Azione personalizzata                         |
|-------------------------------------------|---------------------------------------|
| Punto di ingresso (obbligatorio)                    | Chiamata di una DLL.                        |
| Nome eseguibile con argomenti (obbligatorio) | Chiamata di un eseguibile esistente.       |
| Argomenti della riga di comando (facoltativo)         | Chiamata di un eseguibile appena installato. |
| Nome file di destinazione (obbligatorio)               | Creazione di un file da dati personalizzati.     |
| Null                                      | Esecuzione del codice di script.                |



 

</dd> <dt>

<span id="ExtendedType"></span><span id="extendedtype"></span><span id="EXTENDEDTYPE"></span>ExtendedType
</dt> <dd>

Immettere il valore **msidbCustomActionTypePatchUninstall** in questo campo per specificare un'azione personalizzata con l' [opzione di disinstallazione patch azione personalizzata](custom-action-patch-uninstall-option.md).

**[Windows Installer 4,0 e versioni precedenti](not-supported-in-windows-installer-4-0.md):** Non supportato. Questa opzione è disponibile a partire da Windows Installer 4,5.

</dd> </dl>

Per ulteriori informazioni, vedere tutti gli argomenti in [azioni personalizzate](custom-actions.md).

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE12](ice12.md)  
[ICE27](ice27.md)  
[ICE46](ice46.md)  
[ICE63](ice63.md)  
[ICE68](ice68.md)  
[ICE72](ice72.md)  
[ICE75](ice75.md)  
[ICE77](ice77.md)  
[ICE80](ice80.md)  
[ICE88](ice88.md)  
[ICE93](ice93.md)  
</dl>

 

 



