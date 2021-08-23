---
description: La tabella Collegamento contiene le informazioni necessarie all'applicazione per creare collegamenti nel computer dell'utente.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Tabella dei collegamenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e47a5c5843b4ad1986d968329c9df9b6d9df5e291cd4adf06bccfcfa37adb66a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119628421"
---
# <a name="shortcut-table"></a>Tabella dei collegamenti

La tabella Collegamento contiene le informazioni necessarie all'applicazione per creare collegamenti nel computer dell'utente.

La tabella Collegamento include le colonne seguenti.



| Colonna                 | Tipo                         | Chiave | Nullable |
|------------------------|------------------------------|-----|----------|
| Tasto di scelta rapida               | [Identificatore](identifier.md) | S   | N        |
| Directory\_            | [Identificatore](identifier.md) | N   | N        |
| Nome                   | [Filename](filename.md)     | N   | N        |
| Componente\_            | [Identificatore](identifier.md) | N   | N        |
| Destinazione                 | [Scelte rapide](shortcut.md)     | N   | N        |
| Argomenti              | [Formattato](formatted.md)   | N   | S        |
| Descrizione            | [Text](text.md)             | N   | S        |
| Tasto di scelta rapida                 | [Integer](integer.md)       | N   | S        |
| Icona\_                 | [Identificatore](identifier.md) | N   | S        |
| IconIndex              | [Integer](integer.md)       | N   | S        |
| ShowCmd                | [Integer](integer.md)       | N   | S        |
| WkDir                  | [Identificatore](identifier.md) | N   | S        |
| DisplayResourceDLL     | [Formattato](formatted.md)   | N   | S        |
| DisplayResourceId      | [Integer](integer.md)       | N   | S        |
| DescrizioneResourceDLL | [Formattato](formatted.md)   | N   | S        |
| DescriptionResourceId  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Scelta rapida
</dt> <dd>

Valore della chiave per questa tabella.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella Directory](directory-table.md). Questa colonna specifica la directory in cui viene creato il file di collegamento.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Nome localizzabile del collegamento da creare.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella Component](component-table.md). Il programma di installazione usa lo stato di installazione del componente specificato in questa colonna per determinare se il collegamento viene creato o eliminato. Questo componente deve avere un percorso di chiave valido per l'installazione del collegamento. Se la colonna Destinazione contiene il nome di una funzionalità, il file avviato dal collegamento è il file di chiave del componente elencato in questa colonna.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>bersaglio
</dt> <dd>

Destinazione del collegamento.

Per un collegamento annunciato, questa colonna deve essere una chiave esterna nella prima colonna della [tabella Funzionalità](feature-table.md). Il programma di installazione valuta la [](identifier.md) voce nel campo Destinazione come identificatore e la voce deve essere una chiave esterna valida nella [tabella delle funzionalità](feature-table.md). Il file avviato dal collegamento in questo caso è il file di chiave del componente elencato nella colonna \_ Componente. Quando il collegamento viene attivato, il programma di installazione verifica che tutti i componenti nella funzionalità siano installati prima di avviare questo file.

Per un collegamento non annunciato, il programma di installazione valuta questo campo come [stringa formattata.](formatted.md) Il campo deve contenere un identificatore di proprietà racchiuso tra parentesi quadre ( ), espanso nel file o in una cartella a cui punta \[ \] il collegamento. Per altre informazioni, vedere [l'azione CreateShortcuts](createshortcuts-action.md).

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argomenti
</dt> <dd>

Argomenti della riga di comando per il collegamento.

Si noti che la risoluzione delle proprietà nel campo Argomenti è limitata. Una proprietà formattata come Proprietà in questo campo può essere risolta solo se la proprietà ha già il valore previsto quando viene installato il componente proprietario \[  \] del collegamento. Ad esempio, per risolvere il valore corretto per l'argomento "MyDoc.doc", lo stesso processo deve installare il file MyDoc.doc e il componente proprietario del \[ \# \] collegamento.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione localizzabile del collegamento.

</dd> <dt>

<span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey
</dt> <dd>

Tasto di scelta rapida per il collegamento. Il byte di ordine basso contiene il codice della chiave virtuale per la chiave e il byte di ordine più alto contiene i flag di modifica. Deve essere un numero non negativo. Gli autori dei pacchetti di installazione sono in genere consigliati di non impostare questa opzione, perché l'impostazione di questa opzione può aggiungere tasti di scelta rapida duplicati al desktop di un utente. Inoltre, la pratica di assegnare tasti di scelta rapida ai tasti di scelta rapida può essere problematica per gli utenti che usano i tasti di scelta rapida per [l'accessibilità.](accessibility.md)

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icona\_
</dt> <dd>

Chiave esterna alla colonna uno della [tabella Icon](icon-table.md).

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Indice dell'icona per il collegamento. Deve essere un numero non negativo.

</dd> <dt>

<span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd
</dt> <dd>

Comando Show per la finestra dell'applicazione.

È possibile usare i valori seguenti. I valori sono definiti per la funzione Windows API ShowWindow.



| Valore | Significato             |
|-------|---------------------|
| 1     | SW \_ SHOWNORMAL      |
| 3     | SW \_ SHOWMAXIMIZED   |
| 7     | SW \_ SHOWMINNOACTIVE |



 

</dd> <dt>

<span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir
</dt> <dd>

Nome della proprietà con il percorso della directory di lavoro per il collegamento. Il valore può usare il formato Windows per fare riferimento alle variabili di ambiente, ad esempio %USERPROFILE%. I riferimenti vengono risolti in un percorso effettivo quando il programma di installazione risolve la directory di lavoro per creare il collegamento.

</dd> </dl>

<dl> <dt>

<span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL
</dt> <dd>

Questo campo contiene un [valore](formatted.md) stringa formattato per il percorso completo del file eseguibile portabile indipendente dalla lingua (file LN) che contiene i dati di configurazione delle risorse (configurazione RC). La stringa formattata può usare la \[ \# convenzione \] filekey. Se questo campo contiene un valore, la colonna Nome viene ignorata. Se questo campo è vuoto, il programma di installazione usa il valore nella colonna Nome. Quando questo campo contiene un valore, anche il **campo DisplayResourceId** deve contenere un valore oppure l'installazione non riesce.

Questa colonna della tabella Collegamento viene usata solo quando viene eseguita in Windows Vista o Windows Server 2008 e in caso contrario viene ignorata. Questa colonna è disponibile con versioni non precedenti a Windows Installer 4.0.

Per informazioni su come aggiungere collegamenti alla tabella dei collegamenti da usare con le risorse MUI, vedere Esempio di collegamento [MUI](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId
</dt> <dd>

Indice del nome visualizzato per il collegamento. Deve essere un numero non negativo. Quando questo campo contiene un valore, il **campo DisplayResourceDLL** deve contenere anche un valore o l'installazione non riesce.

Questa colonna della tabella Collegamento viene usata solo quando viene eseguita in Windows Vista o Windows Server 2008 e in caso contrario viene ignorata. Questa colonna è disponibile con versioni non precedenti a Windows Installer 4.0.

</dd> <dt>

<span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescrizioneResourceDLL
</dt> <dd>

Questo campo contiene un [valore](formatted.md) stringa formattato per il percorso completo del file eseguibile portabile indipendente dalla lingua (file LN) che contiene i dati di configurazione delle risorse (configurazione RC). La stringa formattata può usare la \[ \# convenzione \] filekey. Se questo campo contiene un valore, la colonna Nome viene ignorata. Se questo campo è vuoto, il programma di installazione usa il valore nella colonna Descrizione. Quando questo campo contiene un valore, anche il **campo DescriptionResourceId** deve contenere un valore oppure l'installazione non riesce.

Questa colonna della tabella Collegamento viene usata solo quando viene eseguita in Windows Vista o Windows Server 2008 e in caso contrario viene ignorata. Questa colonna è disponibile con versioni non precedenti a Windows Installer 4.0.

Per informazioni su come aggiungere collegamenti alla tabella dei collegamenti da usare con le risorse MUI, vedere Esempio di collegamento [MUI](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId
</dt> <dd>

Indice del nome della descrizione per il collegamento. Deve essere un numero non negativo. Quando questo campo contiene un valore, il **campo DescriptionResourceDLL** deve contenere anche un valore o l'installazione non riesce.

Questa colonna della tabella Collegamento viene usata solo quando viene eseguita in Windows Vista o Windows Server 2008 e in caso contrario viene ignorata. Questa colonna è disponibile con versioni non precedenti a Windows Installer 4.0.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'abilitazione di una funzionalità crea un collegamento annunciato solo se l'interfaccia IShellLink del sistema supporta la risoluzione del descrittore del programma di installazione. Questa funzionalità è supportata da Microsoft Windows 2000 e dai sistemi che eseguono Microsoft Internet Explorer 4.01. Se non supportato, il programma di installazione crea un collegamento non annunciato al momento dell'installazione del componente della funzionalità, in locale o in esecuzione dall'origine.

Si noti che i collegamenti annunciati puntano sempre a una determinata applicazione, identificata da [**un ProductCode,**](productcode.md)e non devono essere condivisi tra le applicazioni. I collegamenti annunciati funzionano solo per l'applicazione installata più di recente e vengono rimossi quando l'applicazione viene rimossa.

Questa tabella viene indicata quando vengono eseguite [l'azione CreateShortcuts](createshortcuts-action.md) e [l'azione RemoveShortcuts.](removeshortcuts-action.md)

Vedere anche la [**proprietà DISABLEADVTSHORTCUTS.**](disableadvtshortcuts.md)

## <a name="validation"></a>Convalida

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE19](ice19.md)  
[ICE32](ice32.md)  
[ICE36](ice36.md)  
[ICE46](ice46.md)  
[ICE50](ice50.md)  
[ICE57](ice57.md)  
[ICE59](ice59.md)  
[ICE67](ice67.md)  
[ICE69](ice69.md)  
[ICE80](ice80.md)  
[ICE90](ice90.md)  
[ICE91](ice91.md)  
[ICE94](ice94.md)  
</dl>

 

 



