---
title: Definizione di un nuovo carattere
description: Definizione di un nuovo carattere
ms.assetid: 4102cb7d-2fec-45d2-882a-04704c7f5a48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2586312ac9d913a27d2df0be112cbcf92c47f4fa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103955590"
---
# <a name="defining-a-new-character"></a>Definizione di un nuovo carattere

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per definire un nuovo carattere, eseguire l'editor dei caratteri di Agent. Se è stato caricato un file di caratteri esistente, scegliere il **nuovo** comando dal menu **file** . Verrà visualizzato un sottomenu delle scelte. Se si crea un carattere per uso personale, scegliere **carattere personalizzato**. Se si desidera creare un carattere che può essere utilizzato come carattere predefinito dell'agente, scegliere **carattere predefinito**. Questa operazione consente di preconfigurare l'editor con tutti i nomi di animazione e le assegnazioni di stato di animazione necessari, nonché di impostare l'opzione **supporta set di animazioni standard** . Analogamente, se si sceglie il carattere Assistente di Office, l'editor viene preconfigurato con i nomi di animazione e l'assegnazione dello stato di animazione necessari per un carattere Assistente di Office. Questa azione seleziona l'icona del **carattere** nell'albero e visualizza le pagine delle proprietà sul lato destro della finestra. Le sezioni seguenti descrivono come impostare le proprietà del carattere e come creare animazioni per il carattere.

### <a name="setting-your-characters-general-information"></a>Impostazione delle informazioni generali del carattere

Per iniziare a definire un carattere, immettere il nome del carattere nella casella di testo **nome** (32 caratteri massimo). Poiché Microsoft Agent usa il nome per consentire agli utenti di accedere al carattere, specificare un nome descrittivo. Specificare un nome che può essere pronunciato usando l'ortografia convenzionale oppure disabilitare l'input vocale per il carattere. È anche possibile specificare una breve descrizione facoltativa (256 caratteri) per il carattere nella casella di testo Descrizione. Il server espone gli elementi immessi nella casella di testo descrizione per le applicazioni client.

È anche possibile archiviare i propri dati come parte del carattere usando il campo dati. È possibile usare questa funzionalità per includere informazioni speciali sul carattere o su altri dati. Una volta compilata con l'editor di caratteri, è possibile accedere a queste informazioni usando la proprietà dati di tipo "OutData" in fase di esecuzione quando viene caricato il carattere.

È possibile impostare il nome, la descrizione e le informazioni aggiuntive sui dati del carattere in base all'impostazione dell'ID lingua del carattere. Per impostare questi dati per un'altra lingua, selezionare lingua e immettere il testo. È inoltre necessario che le tabelle codici della lingua siano installate nel sistema in cui viene compilato il file di caratteri. Se le impostazioni della lingua appropriate non verranno incluse nel file di caratteri compilato. Non è necessario fornire informazioni in altre lingue. Se queste proprietà vengono sottoposte a query in fase di esecuzione tramite l'API dell'agente e non sono presenti impostazioni specifiche per tale lingua, vengono restituite le impostazioni di inglese (impostazione predefinita).

### <a name="setting-your-characters-output-options"></a>Impostazione delle opzioni di output del carattere

Se si imposta l'opzione supporta set di animazioni standard, l'editor di caratteri verificherà che siano state incluse tutte le animazioni necessarie e le assegnazioni di stato di animazione per un carattere predefinito quando si tenta di compilare il carattere. Se un elemento non è presente, in una finestra di messaggio vengono elencati gli elementi mancanti. Per informazioni dettagliate sul set di animazioni standard, vedere [**progettazione di caratteri per Microsoft Agent**](designing-characters-for-microsoft-agent.md).

Per l'output parlato del carattere, Microsoft Agent consente di scegliere una voce sintetizzata, sintesi vocale (TTS) o una voce che usa file audio registrati. Se si vuole usare una voce sintetizzata, selezionare l'opzione Usa sintesi vocale per l'output vocale. Verrà aggiunta una pagina voce per la selezione delle caratteristiche della voce. Scegliere la pagina voce e usare i controlli presenti nella pagina per selezionare una voce, una velocità e un passo di tutti i motori TTS compatibili installati. L'intervallo dei parametri vocali che è possibile selezionare dipende dai motori TTS. Se non è stato ancora installato un motore TTS, l'elenco di ID voce sarà vuoto. Prima di definire le impostazioni vocali del carattere nell'editor dei caratteri dell'agente, è necessario che sia installato un motore TTS.

Se si prevede di usare un motore TTS per l'output del carattere, è necessario installare anche tale motore nel sistema dell'utente. Se si seleziona una voce basata su un particolare motore TTS, ma nell'utente è installato un motore TTS diverso, il server tenterà di trovare una corrispondenza con la voce in base alle caratteristiche definite nell'editor dei caratteri dell'agente.

Se si prevede di usare i file audio registrati (. File WAV) per l'output parlato del carattere, non è necessario selezionare l'opzione Usa sintesi vocale per l'output vocale. Al contrario, sarà necessario registrare separatamente i file audio di output parlato e caricarli dal codice dell'applicazione.

L'opzione Use **Word Balloon** consente di determinare se si vuole supportare una parola Balloon per il carattere. Questa funzionalità può essere impostata anche in fase di esecuzione.

Quando l'opzione **Use Word Balloon** è selezionata, è possibile accedere alla pagina di **Word Balloon** . Le opzioni nella pagina di **Word Balloon** consentono di modificare le caratteristiche predefinite del fumetto di Word. L'impostazione **caratteri per riga** consente di definire la larghezza del fumetto in base al numero medio di caratteri per riga. È possibile impostare l'altezza predefinita in base a un numero fisso di righe che si desidera visualizzare in una sola volta o automaticamente dimensionate in base al testo fornito nel metodo [**Speak**](speak-method.md) . È anche possibile specificare se il fumetto viene nascosto automaticamente dopo il completamento di un metodo **Speak** e se il fumetto Visualizza o imposta automaticamente le parole per la velocità di output vocale del carattere.

La pagina del **fumetto di Word** consente inoltre di impostare il tipo di carattere predefinito per il fumetto di parola del carattere e i colori di visualizzazione del fumetto. Tuttavia, tenere presente che gli utenti possono eseguire l'override delle impostazioni del tipo di carattere del fumetto di Word usando la finestra delle proprietà di Microsoft Agent.

### <a name="setting-your-characters-identifier"></a>Impostazione dell'identificatore del carattere

Ogni carattere richiede un identificatore univoco (GUID). Il server utilizza l'identificatore per distinguere i caratteri. Quando si crea un nuovo carattere, l'editor crea automaticamente un nuovo identificatore per il carattere. È necessario modificare l'identificatore di un carattere solo se è stato copiato il file di definizione dei caratteri di un altro carattere o se si vuole intenzionalmente distinguere un carattere da una versione precedente. Per modificare l'identificatore di un carattere, fare clic sul pulsante nuovo GUID e l'editor genererà un nuovo identificatore.

 

 




