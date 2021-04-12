---
description: La tabella ModuleSubstitution specifica i campi configurabili di un database del modulo e fornisce un modello per la configurazione di ogni campo.
ms.assetid: 8e94c31f-b3a7-4f3a-aec4-32b0e1dd5400
title: Tabella ModuleSubstitution
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2e27789f723af87e228bada91b79a16d7dc4d2d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104234041"
---
# <a name="modulesubstitution-table"></a>Tabella ModuleSubstitution

La tabella ModuleSubstitution specifica i campi configurabili di un database del modulo e fornisce un modello per la configurazione di ogni campo. Lo strumento utente o merge può eseguire una query su questa tabella per determinare quali operazioni di configurazione devono essere eseguite. Questa tabella non è unita nel database di destinazione.

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

In questa colonna viene specificato il nome della tabella da modificare nel database del modulo.

</dd> <dt>

<span id="Row"></span><span id="row"></span><span id="ROW"></span>Riga
</dt> <dd>

Questo campo specifica le chiavi primarie della riga di destinazione nella tabella denominata nella colonna della tabella. Più chiavi primarie sono separate da punti e virgola. Le righe di destinazione vengono selezionate per la modifica prima che vengano apportate modifiche alla tabella di destinazione. Se un record nella tabella ModuleSubstitution modifica il campo chiave primaria di una riga di destinazione, gli altri record nella tabella ModuleSubstitution vengono applicati in base ai dati della chiave primaria originale, non alle sostituzioni della chiave primaria. L'ordine di sostituzione della riga non è definito.

I valori in questa colonna sono sempre in [formato speciale CMSM](cmsm-special-format.md). È possibile aggiungere un punto e virgola (';') o un segno di uguale (' =') anteponendo il carattere con una barra rovesciata. '\\'. Un valore null per una chiave è identificato da un valore null, un punto e virgola iniziale, due punti e virgola consecutivi o un punto e virgola finale, a seconda che il valore null sia un valore di colonna chiave unico, primo, medio o finale.

</dd> <dt>

<span id="Column"></span><span id="column"></span><span id="COLUMN"></span>Colonna
</dt> <dd>

Questo campo specifica la colonna di destinazione nella riga denominata nella colonna riga. Se più righe della tabella ModuleSubstitution modificano colonne diverse della stessa riga di destinazione, tutte le sostituzioni di colonna vengono eseguite prima che la riga modificata venga inserita nel database. L'ordine di sostituzione della colonna non è definito.

</dd> <dt>

<span id="Value"></span><span id="value"></span><span id="VALUE"></span>Valore
</dt> <dd>

Questa colonna contiene una stringa che fornisce un modello di formattazione per i dati che vengono sostituiti nel campo di destinazione specificato da tabella, riga e colonna. Quando \[ viene rilevata una stringa di sostituzione con formato = ITEMA \] , la stringa, inclusi i caratteri tra parentesi quadre, viene sostituita dal valore di "ITEMA" configurabile. L'elemento configurabile "ITEMA" viene specificato nella colonna Name della [tabella ModuleConfiguration](moduleconfiguration-table.md) e il relativo valore viene fornito dallo strumento merge. Se lo strumento di merge rifiuta di fornire un valore per qualsiasi elemento in una stringa di sostituzione, il valore predefinito specificato nella colonna DefaultValue della tabella ModuleConfiguration viene sostituito. Se una stringa fa riferimento a un elemento non presente nella tabella ModuleConfiguration, l'Unione ha esito negativo.

-   In questa colonna viene utilizzato il [formato speciale CMSM](cmsm-special-format.md). È possibile aggiungere alla tabella un punto e virgola letterale (';') o un segno di uguale (' =') anteponendo il carattere con una barra rovesciata. '\\'.
-   Il campo del valore può contenere più stringhe di sostituzione. Ad esempio, la configurazione degli elementi "Food1" e "food2" nella stringa: " \[ = Food1 \] è corretta, ma \[ = food2 \] è migliore perché \[ = food2 \] è più nutriente".
-   Le stringhe di sostituzione non devono essere nidificate. Il modello " \[ = AB \[ = CDE \] \] " non è valido.
-   Se il campo del valore restituisce null e il campo di destinazione non ammette valori null, l'Unione ha esito negativo e viene creato un oggetto Error di tipo msmErrorBadNullSubstitution che viene aggiunto all'elenco errori. Per informazioni dettagliate, vedere i tipi di errore descritti in [**ottenere la \_ funzione di tipo**](/windows/win32/api/mergemod/nf-mergemod-imsmerror-get_type).
-   Se il campo del valore restituisce il GUID null: {00000000-0000-0000-0000-000000000000} , il GUID null viene sostituito dal nome della funzionalità prima che la riga venga unita al modulo. Per informazioni dettagliate, vedere [riferimento alle funzionalità nei moduli unione](referencing-features-in-merge-modules.md).
-   Il modello nel campo del valore viene valutato prima di essere inserito nel campo di destinazione. La sostituzione in una riga viene eseguita prima di sostituire tutte le funzionalità.
-   Se la colonna valore restituisce una stringa costituita solo da caratteri Integer (con un segno + o-) facoltativo, la stringa viene convertita in un numero intero prima di essere sostituita in un campo di destinazione del [tipo di formato integer](integer-format-types.md). Se il modello restituisce una stringa che non è costituita solo da caratteri Integer (e da un valore facoltativo + o-), il risultato non può essere sostituito in un campo di destinazione di tipo Integer. Se si tenta di inserire un valore diverso da integer in un campo Integer, l'Unione avrà esito negativo e verrà aggiunto un oggetto errore msmErrorBadSubstitutionType all'elenco errori.
-   Se la colonna di destinazione specificata nei campi tabella e colonna è un [tipo di formato testo](text-format-types.md)e la valutazione del campo valore genera un [tipo di formato integer](integer-format-types.md), viene inserita una rappresentazione decimale del numero nel campo di testo di destinazione.
-   Se il campo di destinazione è [un tipo di formato integer](integer-format-types.md), il campo del valore è costituito da un elenco non delimitato di elementi nel [formato bit](bitfield-format-types.md), il valore nel campo di destinazione viene combinato usando l'operatore **and** bit per bit con l'inverso dell' **operatore OR bit per bit di** tutti i valori di maschera dagli elementi, quindi combinati con l'operatore **OR bit per** bit con ognuno degli elementi Integer o bit quando vengono mascherati dai valori della maschera corrispondenti In sostanza, imposta in modo esplicito i bit dalle proprietà sui valori forniti, ma lascia solo tutti gli altri bit nella cella.
-   Se il campo del valore restituisce un [tipo di formato chiave](key-format-types.md)e è una chiave in una tabella che utilizza più chiavi primarie, il nome dell'elemento può essere seguito da un punto e virgola e da un valore intero che indica l'indice in base 1 nel set di valori che insieme costituiscono una chiave primaria. Se non viene specificato alcun Integer, viene usato il valore 1. La [tabella dei controlli](control-table.md) , ad esempio, include due colonne chiave primaria, finestra di dialogo \_ e controllo. Il valore di un elemento "Item1" che rappresenta una chiave nella tabella dei controlli avrà il formato "Dialogname; ControlName ", dove Dialogname è il valore nella tabella della finestra \_ di dialogo e ControlName è il valore nella colonna del controllo. Per sostituire solo ControlName, è necessario usare la stringa di sostituzione \[ = Item1; 2 \] .

</dd> </dl>

## <a name="remarks"></a>Commenti

La tabella ModuleSubstition viene utilizzata dai [moduli merge configurabili](configurable-merge-modules.md). Per creare un modulo merge configurabile è necessario Mergemod.dll versione 2,0 o successiva.

Per garantire la compatibilità con le versioni di Mergemod.dll precedenti alla versione 2,0, è necessario includere nella [tabella ModuleIgnoreTable](moduleignoretable-table.md) di ogni modulo le tabelle [ModuleConfiguration](moduleconfiguration-table.md) e ModuleSubstitution.

 

 
