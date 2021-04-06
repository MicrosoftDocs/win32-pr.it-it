---
description: La tabella dei collegamenti include le informazioni necessarie all'applicazione per creare collegamenti nel computer dell'utente.
ms.assetid: 86b5b51e-e5f4-4f42-84f9-1faa29ea7a84
title: Tabella di collegamento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56482f1d2d5521bede54c781c91d2de2bc39e79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882926"
---
# <a name="shortcut-table"></a>Tabella di collegamento

La tabella dei collegamenti include le informazioni necessarie all'applicazione per creare collegamenti nel computer dell'utente.

La tabella dei collegamenti contiene le colonne seguenti.



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
| DescriptionResourceDLL | [Formattato](formatted.md)   | N   | S        |
| DescriptionResourceId  | [Integer](integer.md)       | N   | S        |



 

## <a name="columns"></a>Colonne

<dl> <dt>

<span id="Shortcut"></span><span id="shortcut"></span><span id="SHORTCUT"></span>Collegamento
</dt> <dd>

Valore della chiave per questa tabella.

</dd> <dt>

<span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella di directory](directory-table.md). Questa colonna specifica la directory in cui viene creato il file di collegamento.

</dd> <dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>Nome
</dt> <dd>

Nome localizzabile del collegamento da creare.

</dd> <dt>

<span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Componente\_
</dt> <dd>

Chiave esterna nella prima colonna della [tabella dei componenti](component-table.md). Il programma di installazione utilizza lo stato di installazione del componente specificato in questa colonna per determinare se il collegamento è stato creato o eliminato. Questo componente deve avere un percorso di chiave valido per il collegamento da installare. Se la colonna di destinazione contiene il nome di una funzionalità, il file avviato dal collegamento è il file di chiave del componente elencato in questa colonna.

</dd> <dt>

<span id="Target"></span><span id="target"></span><span id="TARGET"></span>Destinazione
</dt> <dd>

Destinazione del collegamento.

Per un collegamento annunciato, questa colonna deve essere una chiave esterna nella prima colonna della [tabella delle funzionalità](feature-table.md). Il programma di installazione valuta la voce nel campo di destinazione come [identificatore](identifier.md) e la voce deve essere una chiave esterna valida nella [tabella delle funzionalità](feature-table.md). Il file avviato dal collegamento in questo caso è il file di chiave del componente elencato nella \_ colonna componente. Quando il collegamento viene attivato, il programma di installazione verifica che tutti i componenti della funzionalità siano installati prima di avviare il file.

Per un collegamento non annunciato, il programma di installazione valuta questo campo come stringa [formattata](formatted.md) . Il campo deve contenere un identificatore di proprietà racchiuso tra parentesi quadre ( \[ \] ), espanso nel file o in una cartella a cui punta il tasto di scelta rapida. Per ulteriori informazioni, vedere l' [azione CreateShortcuts](createshortcuts-action.md).

</dd> <dt>

<span id="Arguments"></span><span id="arguments"></span><span id="ARGUMENTS"></span>Argomenti
</dt> <dd>

Argomenti della riga di comando per il collegamento.

Si noti che la risoluzione delle proprietà nel campo arguments è limitata. Una proprietà formattata come \[ *Proprietà* \] in questo campo può essere risolta solo se la proprietà dispone già del valore previsto quando il componente proprietario del collegamento è installato. Ad esempio, per risolvere il valore corretto per l'argomento " \[ \#MyDoc.doc\] ", lo stesso processo deve installare il file MyDoc.doc e il componente proprietario del collegamento.

</dd> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Descrizione
</dt> <dd>

Descrizione localizzabile del collegamento.

</dd> <dt>

<span id="Hotkey"></span><span id="hotkey"></span><span id="HOTKEY"></span>Hotkey
</dt> <dd>

Tasto di scelta rapida per il collegamento. Il byte di ordine inferiore contiene il codice della chiave virtuale per la chiave e il byte di ordine superiore contiene i flag di modifica. Deve essere un numero non negativo. Per gli autori dei pacchetti di installazione è in genere consigliabile non impostare questa opzione, perché l'impostazione di questa opzione consente di aggiungere tasti di scelta rapida duplicati al desktop di un utente. Inoltre, la pratica di assegnare tasti di scelta rapida ai collegamenti può risultare problematica per gli utenti che utilizzano tasti di scelta rapida per l' [accessibilità](accessibility.md).

</dd> <dt>

<span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icona\_
</dt> <dd>

Chiave esterna per la colonna uno della [tabella delle icone](icon-table.md).

</dd> <dt>

<span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex
</dt> <dd>

Indice dell'icona per il collegamento. Deve essere un numero non negativo.

</dd> <dt>

<span id="ShowCmd"></span><span id="showcmd"></span><span id="SHOWCMD"></span>ShowCmd
</dt> <dd>

Comando show per la finestra dell'applicazione.

È possibile utilizzare i valori seguenti. I valori sono definiti per la funzione API Windows ShowWindow.



| Valore | Significato             |
|-------|---------------------|
| 1     | \_SHOWNORMAL SW      |
| 3     | \_SHOWMAXIMIZED SW   |
| 7     | \_SHOWMINNOACTIVE SW |



 

</dd> <dt>

<span id="WkDir"></span><span id="wkdir"></span><span id="WKDIR"></span>WkDir
</dt> <dd>

Nome della proprietà con il percorso della directory di lavoro per il collegamento. Il valore può usare il formato Windows per fare riferimento alle variabili di ambiente, ad esempio% USERPROFILE%. I riferimenti vengono risolti in un percorso effettivo quando il programma di installazione risolve la directory di lavoro per creare il collegamento.

</dd> </dl>

<dl> <dt>

<span id="DisplayResourceDLL"></span><span id="displayresourcedll"></span><span id="DISPLAYRESOURCEDLL"></span>DisplayResourceDLL
</dt> <dd>

Questo campo contiene un valore stringa [formattato](formatted.md) per il percorso completo del file eseguibile portatile indipendente dalla lingua (nel file) che contiene i dati di configurazione della risorsa (configurazione RC). La stringa formattata può utilizzare la \[ \# \] convenzione FileKey. Se questo campo contiene un valore, la colonna Name verrà ignorata. Se il campo è vuoto, il programma di installazione utilizzerà il valore nella colonna nome. Quando questo campo contiene un valore, anche il campo **DisplayResourceId** deve contenere un valore oppure l'installazione non riesce.

Questa colonna della tabella dei collegamenti viene utilizzata solo quando è in esecuzione in Windows Vista o Windows Server 2008 e viene altrimenti ignorata. Questa colonna è disponibile con versioni non precedenti a Windows Installer 4,0.

Per informazioni su come aggiungere collegamenti alla tabella dei collegamenti per l'uso con le risorse MUI, vedere [un esempio di collegamento MUI](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DisplayResourceId"></span><span id="displayresourceid"></span><span id="DISPLAYRESOURCEID"></span>DisplayResourceId
</dt> <dd>

Indice del nome visualizzato per il collegamento. Deve essere un numero non negativo. Quando questo campo contiene un valore, il campo **DisplayResourceDLL** è necessario per contenere anche un valore o l'installazione non riesce.

Questa colonna della tabella dei collegamenti viene utilizzata solo quando è in esecuzione in Windows Vista o Windows Server 2008 e viene altrimenti ignorata. Questa colonna è disponibile con versioni non precedenti a Windows Installer 4,0.

</dd> <dt>

<span id="DescriptionResourceDLL"></span><span id="descriptionresourcedll"></span><span id="DESCRIPTIONRESOURCEDLL"></span>DescriptionResourceDLL
</dt> <dd>

Questo campo contiene un valore stringa [formattato](formatted.md) per il percorso completo del file eseguibile portatile indipendente dalla lingua (nel file) che contiene i dati di configurazione della risorsa (configurazione RC). La stringa formattata può utilizzare la \[ \# \] convenzione FileKey. Se questo campo contiene un valore, la colonna Name verrà ignorata. Se il campo è vuoto, il programma di installazione utilizzerà il valore nella colonna Descrizione. Quando questo campo contiene un valore, anche il campo **DescriptionResourceId** deve contenere un valore oppure l'installazione non riesce.

Questa colonna della tabella dei collegamenti viene utilizzata solo quando è in esecuzione in Windows Vista o Windows Server 2008 e viene altrimenti ignorata. Questa colonna è disponibile con versioni non precedenti a Windows Installer 4,0.

Per informazioni su come aggiungere collegamenti alla tabella dei collegamenti per l'uso con le risorse MUI, vedere [un esempio di collegamento MUI](a-mui-shortcut-example.md).

</dd> <dt>

<span id="DescriptionResourceId"></span><span id="descriptionresourceid"></span><span id="DESCRIPTIONRESOURCEID"></span>DescriptionResourceId
</dt> <dd>

Indice del nome della descrizione per il collegamento. Deve essere un numero non negativo. Quando questo campo contiene un valore, il campo **DescriptionResourceDLL** è necessario per contenere anche un valore o l'installazione non riesce.

Questa colonna della tabella dei collegamenti viene utilizzata solo quando è in esecuzione in Windows Vista o Windows Server 2008 e viene altrimenti ignorata. Questa colonna è disponibile con versioni non precedenti a Windows Installer 4,0.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'abilitazione di una funzionalità consente di creare un collegamento annunciato solo se l'interfaccia IShellLink del sistema supporta la risoluzione del descrittore del programma di installazione. Questa operazione è supportata da Microsoft Windows 2000 e dai sistemi che eseguono Microsoft Internet Explorer 4,01. Se non è supportato, il programma di installazione crea un collegamento non annunciato durante l'installazione del componente della funzionalità, localmente o eseguito dall'origine.

Si noti che i collegamenti annunciati sempre puntano a una particolare applicazione, identificata da un [**ProductCode**](productcode.md)e non devono essere condivisi tra le applicazioni. I collegamenti annunciati funzionano solo per l'applicazione installata più di recente e vengono rimossi quando l'applicazione viene rimossa.

Questa tabella viene definita quando viene eseguita l' [azione CreateShortcuts](createshortcuts-action.md) e l' [azione RemoveShortcuts](removeshortcuts-action.md) .

Vedere anche la proprietà [**DISABLEADVTSHORTCUTS**](disableadvtshortcuts.md) .

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

 

 



