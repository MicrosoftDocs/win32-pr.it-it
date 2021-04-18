---
description: La tabella Environment viene utilizzata per impostare i valori delle variabili di ambiente.
ms.assetid: f7106ed6-706f-4e57-989f-030066bcecd3
title: Tabella ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7a4db2e33c01685bdc40475f659e1b03b69b6c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106310526"
---
# <a name="environment-table"></a>Tabella ambiente

La tabella Environment viene utilizzata per impostare i valori delle variabili di ambiente.

La tabella Environment contiene le colonne seguenti.



| Colonna      | Tipo                         | Chiave | Nullable |
|-------------|------------------------------|-----|----------|
| Ambiente | [Identificatore](identifier.md) | S   | N        |
| Nome        | [Text](text.md)             | N   | N        |
| Valore       | [Formattato](formatted.md)   | N   | S        |
| Componente\_ | [Identificatore](identifier.md) | N   | N        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Environment"></span><span id="environment"></span><span id="ENVIRONMENT"></span>Ambiente
</dt> <dd>

Si tratta della chiave primaria della tabella ed è un token non localizzato.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Questa colonna è il nome localizzabile della variabile di ambiente. I valori di chiave vengono scritti o rimossi a seconda di quali caratteri nella tabella seguente sono preceduti dal prefisso del nome. Non vi sono effetti nell'ordinamento dei simboli usati in un prefisso.



| Prefisso                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =                              | Creare la variabile di ambiente se non esiste, quindi impostarla durante l'installazione. Se la variabile di ambiente esiste, impostarla durante l'installazione.                                                                                                                                                                                                                                                                                                                                   |
| \+                             | Creare la variabile di ambiente se non esiste, quindi impostarla durante l'installazione. Questa operazione non ha alcun effetto sul valore della variabile di ambiente, se esiste già.                                                                                                                                                                                                                                                                                                                         |
| \-                             | Rimuovere la variabile di ambiente quando il componente viene rimosso. Questo simbolo può essere combinato con qualsiasi prefisso.                                                                                                                                                                                                                                                                                                                                                                                      |
| !                              | Rimuovere la variabile di ambiente durante un'installazione. Il programma di installazione rimuove una variabile di ambiente solo durante un'installazione se il nome e il valore della variabile corrispondono alle voci nei campi nome e valore della tabella dell'ambiente. Se si desidera rimuovere una variabile di ambiente, indipendentemente dal relativo valore, utilizzare la sintassi '!' e lasciare vuoto il campo valore.                                                                                                                    |
| \*                             | Questo prefisso viene usato con Windows 2000 per indicare che il nome fa riferimento a una variabile di ambiente di sistema. Se non è presente alcun asterisco, il programma di installazione scrive la variabile nell'ambiente dell'utente. Questo simbolo può essere combinato con qualsiasi prefisso. Un pacchetto usato per l'installazione nel [contesto di installazione](installation-context.md) per computer deve scrivere le variabili di ambiente nell'ambiente del computer includendo \* nella colonna nome. Per altre informazioni, vedere la sezione Osservazioni. |
| =-                             | La variabile di ambiente viene impostata durante l'installazione e viene rimossa durante la disinstallazione. Si tratta del comportamento usuale.                                                                                                                                                                                                                                                                                                                                                                                                 |
| !-                             | Rimuove una variabile di ambiente durante un'installazione o una disinstallazione.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| =+ !+<br/> !=<br/> | Non si tratta di prefissi validi                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

Se il campo del valore nella tabella include un \[ ~ \] , i caratteri di prefisso si applicano solo alla parte specificata della stringa. L'uso di \[ ~ \] è descritto di seguito nella sezione colonna valore.

La variabile di ambiente viene rimossa se il campo del valore della tabella è vuoto. Pertanto, con uno spazio vuoto nel campo del valore, un prefisso = Elimina la variabile di ambiente durante l'installazione e un prefisso Elimina tutti i valori correnti durante la disinstallazione.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Questa colonna contiene il valore localizzabile che deve essere impostato come stringa formattata. Vedere [formattato](formatted.md). Se questo campo viene lasciato vuoto, la variabile viene rimossa. Se il campo è vuoto e la stringa nel campo nome è preceduta dal simbolo-, la variabile viene rimossa solo quando il componente viene rimosso.

Per aggiungere un valore alla fine di una variabile esistente, anteporre il carattere null \[ ~ \] e il carattere separatore alla stringa in questo campo. Se, ad esempio, il punto e virgola è il separatore scelto: \[ ~ \] ;*Valore*.

Per anteporre un valore all'inizio di una variabile esistente, aggiungere la stringa in questo campo per il carattere separatore e il carattere null \[ ~ \] . Se, ad esempio, il punto e virgola è il separatore scelto: *valore*; \[ ~ \] .

Se non \[ ~ \] è presente alcun oggetto nel campo, la stringa rappresenta l'intero valore da impostare o eliminare.

Ogni riga può contenere un solo valore. Ad esempio, il *valore* della voce. *Valore* \[ ~ ; \] è maggiore di un valore e non deve essere utilizzato perché causa risultati imprevedibili. *Valore* della voce. \[ ~ \] è solo un valore.

Se il nome è preceduto da +, \[ ~ \] non deve essere utilizzato nella colonna valore. Questo perché il significato di "+" e " \[ ~ \] " sono chiaramente esclusivi l'uno dall'altro.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna per la prima colonna della tabella dei [componenti](component-table.md). Questa colonna fa riferimento al componente che controlla l'installazione dei valori dell'ambiente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per impostare le variabili di ambiente nel programma di installazione, è necessario che l' [azione WriteEnvironmentStrings](writeenvironmentstrings-action.md) e l' [azione RemoveEnvironmentStrings](removeenvironmentstrings-action.md) siano elencate nella [tabella InstallExecuteSequence](installexecutesequence-table.md).

Si noti che le variabili di ambiente non cambiano per l'installazione in corso quando viene eseguita l'azione [WriteEnvironmentStrings](writeenvironmentstrings-action.md) o [RemoveEnvironmentStrings](removeenvironmentstrings-action.md) . In Windows 2000 queste informazioni vengono archiviate nel registro di sistema e un messaggio informa il sistema di modifiche al termine dell'installazione. Un nuovo processo o un altro processo che verifica la presenza di questi messaggi usa le nuove variabili di ambiente.

Quando si modifica la variabile di ambiente Path con la tabella Environment, non tentare di immettere l'intero nuovo percorso in modo esplicito nel campo del valore. In alternativa, estendere il percorso esistente anteponendo o aggiungendo un valore e un delimitatore (;) a \[ ~ \] . Se \[ ~ \] non è presente nel campo del valore, le informazioni sul percorso esistenti andranno perse e l'installazione del file con estensione msi potrebbe impedire l'avvio del computer. La variabile Path viene generalmente impostata utilizzando la sintassi: \[ ~ \] ; Valore.

Quando si eseguono installazioni per computer da un server terminal, il programma di installazione scrive le variabili di ambiente per utente in **HKU \\ . \\Ambiente predefinito**. Poiché Servizi terminal non replica questa sezione del registro di sistema, l'installazione non imposta le variabili di ambiente per singolo utente. Un pacchetto usato per le installazioni per computer deve scrivere le variabili di ambiente nell'ambiente del computer includendo \* nella colonna nome. Se il pacchetto può essere installato per utente o per computer, creare due componenti: (1) un componente per utente con le voci della tabella dell'ambiente create per le impostazioni utente e (2) un componente per computer con la tabella dell'ambiente creata per le impostazioni del computer. Condizionare l'installazione di questo componente usando la proprietà [**Privileged**](privileged.md) .

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE65](ice65.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
</dl>

 

 




