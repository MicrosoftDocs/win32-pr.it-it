---
description: La tabella Environment viene usata per impostare i valori delle variabili di ambiente.
ms.assetid: f7106ed6-706f-4e57-989f-030066bcecd3
title: Tabella dell'ambiente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de1fe52e8222bfde3e451b6ccc543511822e0d511a2ce1ce2b6bee8bc4fd117f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129601"
---
# <a name="environment-table"></a>Tabella dell'ambiente

La tabella Environment viene usata per impostare i valori delle variabili di ambiente.

La tabella Ambiente include le colonne seguenti.



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

Questa colonna è il nome localizzabile della variabile di ambiente. I valori della chiave vengono scritti o rimossi a seconda dei caratteri nella tabella seguente preceduti dal nome. L'ordinamento dei simboli usati in un prefisso non ha alcun effetto.



| Prefisso                         | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| =                              | Creare la variabile di ambiente se non esiste e quindi impostarla durante l'installazione. Se la variabile di ambiente esiste, impostarla durante l'installazione.                                                                                                                                                                                                                                                                                                                                   |
| \+                             | Creare la variabile di ambiente se non esiste, quindi impostarla durante l'installazione. Questa operazione non ha alcun effetto sul valore della variabile di ambiente se esiste già.                                                                                                                                                                                                                                                                                                                         |
| \-                             | Rimuovere la variabile di ambiente quando il componente viene rimosso. Questo simbolo può essere combinato con qualsiasi prefisso.                                                                                                                                                                                                                                                                                                                                                                                      |
| !                              | Rimuovere la variabile di ambiente durante un'installazione. Il programma di installazione rimuove una variabile di ambiente solo durante un'installazione se il nome e il valore della variabile corrispondono alle voci nei campi Nome e Valore della tabella Ambiente. Se si vuole rimuovere una variabile di ambiente, indipendentemente dal relativo valore, usare la sintassi '!' e lasciare vuoto il campo Valore.                                                                                                                    |
| \*                             | Questo prefisso viene usato con Windows 2000 per indicare che il nome fa riferimento a una variabile di ambiente di sistema. Se non è presente alcun asterisco, il programma di installazione scrive la variabile nell'ambiente dell'utente. Questo simbolo può essere combinato con qualsiasi prefisso. Un pacchetto usato per l'installazione [](installation-context.md) nel contesto di installazione per computer deve scrivere variabili di ambiente nell'ambiente del computer includendo \* nella colonna Nome . Per altre informazioni, vedere la sezione Osservazioni. |
| =-                             | La variabile di ambiente viene impostata durante l'installazione e rimossa durante la disinstallazione. Questo è il comportamento consueto.                                                                                                                                                                                                                                                                                                                                                                                                 |
| !-                             | Rimuove una variabile di ambiente durante un'installazione o una disinstallazione.                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| =+ !+<br/> !=<br/> | Questi non sono prefissi validi                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



 

Se il campo Valore nella tabella include , i caratteri di prefisso si applicano solo \[ ~ \] alla parte specificata della stringa. L'uso \[ ~ \] di è descritto di seguito nella sezione Colonna Valore .

La variabile di ambiente viene rimossa se il campo Valore della tabella è vuoto. Pertanto, con un valore vuoto nel campo Valore, un prefisso = elimina la variabile di ambiente durante l'installazione e un prefisso - elimina tutti i valori correnti durante la disinstallazione.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Questa colonna contiene il valore localizzabile che deve essere impostato come stringa formattata. Vedere [Formattato.](formatted.md) Se questo campo viene lasciato vuoto, la variabile viene rimossa. Se il campo è vuoto e la stringa nel campo Nome è preceduta dal simbolo - , la variabile viene rimossa solo quando il componente viene rimosso.

Per aggiungere un valore alla fine di una variabile esistente, antessare alla stringa in questo campo il carattere Null \[ ~ \] e il carattere separatore. Ad esempio, se il punto e virgola è il separatore scelto: \[ ~ \] ;*Valore*.

Per aggiungere un prefisso a un valore all'inizio di una variabile esistente, aggiungere la stringa in questo campo dal carattere separatore e dal carattere Null \[ ~ \] . Ad esempio, se il punto e virgola è il separatore scelto: *Valore*; \[ ~ \] .

Se nel \[ ~ \] campo non è presente alcun valore, la stringa rappresenta l'intero valore da impostare o eliminare.

Ogni riga può contenere un solo valore. Ad esempio, la voce *Valore*; *Valore*; \[ ~ \] è più di un valore e non deve essere usato perché causa risultati imprevedibili. Valore della *voce*; \[ ~ \] è solo un valore.

Se il prefisso Name è +, non \[ ~ \] deve essere usato nella colonna Valore. Ciò è dovuto al fatto che il significato di "+" e " " è chiaramente \[ ~ \] esclusivo l'uno dell'altro.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna alla prima colonna della [tabella Component](component-table.md). Questa colonna fa riferimento al componente che controlla l'installazione dei valori dell'ambiente.

</dd> </dl>

## <a name="remarks"></a>Commenti

Per impostare le variabili di ambiente da parte del programma di installazione, è necessario che l'azione [WriteEnvironmentStrings](writeenvironmentstrings-action.md) e [l'azione RemoveEnvironmentStrings](removeenvironmentstrings-action.md) siano elencate nella [tabella InstallExecuteSequence](installexecutesequence-table.md).

Si noti che le variabili di ambiente non cambiano per l'installazione in corso quando viene eseguita l'azione [WriteEnvironmentStrings](writeenvironmentstrings-action.md) o [RemoveEnvironmentStrings.](removeenvironmentstrings-action.md) In Windows 2000 queste informazioni vengono archiviate nel Registro di sistema e un messaggio invia una notifica al sistema delle modifiche al termine dell'installazione. Un nuovo processo o un altro processo che controlla questi messaggi usa le nuove variabili di ambiente.

Quando si modifica la variabile di ambiente path con la tabella Environment, non tentare di immettere in modo esplicito l'intero nuovo percorso nel campo Valore. Estendere invece il percorso esistente antecendo o aggiungendo un valore e un delimitatore (;) a \[ ~ \] . Se non è presente nel campo Valore, le informazioni sul percorso esistente andranno perse e l'installazione del file .msi potrebbe impedire l'avvio \[ ~ \] del computer. La variabile path viene generalmente impostata usando la sintassi \[ ~ \] : ; Valore.

Quando si eseguono installazioni per computer da un server terminal, il programma di installazione scrive variabili di ambiente per utente in **HKU \\ . Ambiente \\ predefinito**. Poiché Servizi terminal non replica questa sezione del Registro di sistema, l'installazione non imposta le variabili di ambiente per utente. Un pacchetto usato per le installazioni per computer deve scrivere variabili di ambiente nell'ambiente del computer includendo \* nella colonna Nome . Se il pacchetto può essere installato per utente o per computer, creare due componenti: (1) un componente per utente con le voci della tabella Ambiente create per le impostazioni utente e (2) un componente per computer con la tabella Ambiente creata per le impostazioni del computer. Condizionare l'installazione di questo componente usando [**la proprietà Privileged.**](privileged.md)

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

 

 




