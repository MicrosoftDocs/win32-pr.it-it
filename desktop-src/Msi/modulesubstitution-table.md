---
description: La tabella ModuleSubstitution specifica i campi configurabili di un database dei moduli e fornisce un modello per la configurazione di ogni campo.
ms.assetid: 8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400
title: Tabella ModuleSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a66fbbb0898a254b181d02eca78f33709f8c0e037de140a37893ea3887af6390
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118628589"
---
# <a name="modulesubstitution-table"></a>Tabella ModuleSubstitution

La tabella ModuleSubstitution specifica i campi configurabili di un database dei moduli e fornisce un modello per la configurazione di ogni campo. L'utente o lo strumento di unione può eseguire una query su questa tabella per determinare le operazioni di configurazione da eseguire. Questa tabella non viene unita nel database di destinazione.

Le tabelle seguenti non possono contenere campi configurabili e non devono essere elencate in questa tabella:

Tabella ModuleSubstitution

[Tabella ModuleConfiguration](moduleconfiguration-table.md)

[Tabella ModuleExclusion](moduleexclusion-table.md)

[Tabella ModuleSignature](modulesignature-table.md)

La tabella ModuleSubstitution include le colonne seguenti.



| Colonna | Tipo                         | Chiave | Nullable |
|--------|------------------------------|-----|----------|
| Tabella  | [Identificatore](identifier.md) | S   | N        |
| Riga    | [Text](text.md)             | S   | N        |
| Colonna | [Identificatore](identifier.md) | S   | N        |
| Valore  | [Text](text.md)             | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Table"></span><span id="table"></span><span id="TABLE"></span>tavolo
</dt> <dd>

Questa colonna specifica il nome della tabella da modificare nel database del modulo.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Riga
</dt> <dd>

Questo campo specifica le chiavi primarie della riga di destinazione nella tabella denominata nella colonna Tabella. Più chiavi primarie sono separate da punti e virgola. Le righe di destinazione vengono selezionate per la modifica prima di apportare modifiche alla tabella di destinazione. Se un record nella tabella ModuleSubstitution modifica il campo chiave primaria di una riga di destinazione, gli altri record nella tabella ModuleSubstitution vengono applicati in base ai dati della chiave primaria originale, non al risultato delle sostituzioni della chiave primaria. L'ordine di sostituzione delle righe non è definito.

I valori in questa colonna sono sempre in [formato speciale CMSM.](cmsm-special-format.md) È possibile aggiungere un punto e virgola letterale (';') o uguale ('=') anteficcando il carattere con una barra rovesciata. '\\'. Un valore Null per una chiave è indicato da un valore Null, da un punto e virgola iniziale, da due punti e virgola consecutivi o da un punto e virgola finale, a seconda che il valore Null sia o meno un valore di colonna della chiave sole, first, middle o final.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Colonna
</dt> <dd>

Questo campo specifica la colonna di destinazione nella riga denominata nella colonna Riga. Se più righe nella tabella ModuleSubstitution modificano colonne diverse della stessa riga di destinazione, tutte le sostituzioni di colonna vengono eseguite prima che la riga modificata venga inserita nel database. L'ordine di sostituzione della colonna non è definito.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Questa colonna contiene una stringa che fornisce un modello di formattazione per i dati sostituiti nel campo di destinazione specificato da Tabella, Riga e Colonna. Quando viene rilevata una stringa di sostituzione nel formato =ItemA, la stringa, inclusi i caratteri tra parentesi quadre, viene sostituita dal valore dell'elemento \[ \] configurabile "ItemA". L'elemento configurabile "ItemA" viene specificato nella colonna Nome della tabella [ModuleConfiguration](moduleconfiguration-table.md) e il relativo valore viene fornito dallo strumento di unione. Se lo strumento di unione rifiuta di fornire un valore per qualsiasi elemento in una stringa di sostituzione, viene sostituito il valore predefinito specificato nella colonna DefaultValue della tabella ModuleConfiguration. Se una stringa fa riferimento a un elemento non presente nella tabella ModuleConfiguration, l'unione non riesce.

-   Questa colonna usa [il formato speciale CMSM](cmsm-special-format.md). È possibile aggiungere un punto e virgola letterale (';') o uguale ('=') alla tabella anteficcando il carattere con una barra rovesciata. '\\'.
-   Il campo Valore può contenere più stringhe di sostituzione. Ad esempio, la configurazione degli elementi "Food1" e "Food2" nella stringa : " =Food1 è buona, ma =Food2 è migliore perché =Food2 è più \[ \] \[ \] \[ \] ricca".
-   Le stringhe di sostituzione non devono essere annidate. Il modello " \[ =AB \[ =CDE \] \] " non è valido.
-   Se il campo Valore restituisce Null e il campo di destinazione non ammette valori Null, l'unione ha esito negativo e viene creato e aggiunto un oggetto errore di tipo msmErrorBadNullSubstitution all'elenco errori. Per informazioni dettagliate, vedere i tipi di errore descritti in [**Get \_ Type Function**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).
-   Se il campo Valore restituisce il GUID null: , il GUID Null viene sostituito dal nome della funzionalità prima che la riga venga unita {00000000-0000-0000-0000-000000000000} nel modulo. Per informazioni [dettagliate, vedere Referencing Features in Merge Modules](referencing-features-in-merge-modules.md).
-   Il modello nel campo Valore viene valutato prima di essere inserito nel campo di destinazione. La sostituzione in una riga viene eseguita prima di sostituire qualsiasi funzionalità.
-   Se la colonna Valore restituisce una stringa di soli caratteri interi (con un carattere facoltativo + o -), la stringa viene convertita in un numero intero prima di essere sostituita in un campo di destinazione del tipo di formato [Integer](integer-format-types.md). Se il modello restituisce una stringa che non è costituita solo da caratteri interi (e da un carattere facoltativo + o -), il risultato non può essere sostituito in un campo di destinazione integer. Il tentativo di inserire un valore non Integer in un campo integer causa l'esito negativo dell'unione e aggiunge un oggetto errore msmErrorBadSubstitutionType all'elenco errori.
-   Se la colonna di destinazione specificata nei [](text-format-types.md)campi Tabella e Colonna è un tipo di formato testo e la valutazione del campo Valore comporta un tipo di formato [Integer,](integer-format-types.md)nel campo di testo di destinazione viene inserita una rappresentazione decimale del numero.
-   Se il campo [](integer-format-types.md)di destinazione è un tipo di formato Integer e il campo Valore è costituito da un elenco non delimitato di elementi [in](bitfield-format-types.md)Formato campo bit , il valore nel campo di destinazione viene combinato usando l'operatore **AND** bit per bit con l'inverso dell'operatore **OR** bit per bit di tutti i valori della maschera degli elementi, quindi combinato usando l'operatore **OR** bit per bit con ognuno degli elementi integer o bitfield se mascherati dai valori della maschera corrispondenti. Essenzialmente, imposta in modo esplicito i bit dalle proprietà ai valori specificati, ma lascia tutti gli altri bit nella cella da soli.
-   Se il campo Valore restituisce un tipo di formato chiave [e](key-format-types.md)è una chiave in una tabella che usa più chiavi primarie, il nome dell'elemento può essere seguito da un punto e virgola e da un valore intero che indica l'indice in base 1 nel set di valori che insieme costituiscono una chiave primaria. Se non viene specificato alcun numero intero, viene usato il valore 1. Ad esempio, la [tabella Control](control-table.md) include due colonne chiave primaria, Dialog \_ e Control. Il valore di un elemento "Item1" che rappresenta una chiave nella tabella Control avrà il formato "DialogName; ControlName", dove DialogName è il valore nella tabella Dialog e \_ ControlName è il valore nella colonna Control. Per sostituire solo ControlName, è necessario usare la stringa di sostituzione \[ =Item1;2. \]

</dd> </dl>

## <a name="remarks"></a>Commenti

La tabella ModuleSubstition viene usata dai [moduli unione configurabili.](configurable-merge-modules.md) Mergemod.dll versione 2.0 o successiva è necessario creare un modulo unione configurabile.

Per garantire la compatibilità con le versioni di Mergemod.dll precedenti alla versione 2.0, le tabelle [ModuleConfiguration](moduleconfiguration-table.md) e ModuleSubstitution devono essere incluse nella tabella [ModuleIgnoreTable](moduleignoretable-table.md) di ogni modulo.

 

 
