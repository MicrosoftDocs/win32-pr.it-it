---
title: Definizione di un nuovo carattere
description: Definizione di un nuovo carattere
ms.assetid: 4102cb7d-2fec-45d2-882a-04704c7f5a48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a1f3d9aee78893ebc4796781947be92366baa10b9ad1e123a73121df24646ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963101"
---
# <a name="defining-a-new-character"></a>Definizione di un nuovo carattere

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Per definire un nuovo carattere, eseguire Editor caratteri agente. Se è stato caricato un file di caratteri esistente, scegliere il **comando** Nuovo dal menu **File.** Verrà visualizzato un sottomenu di scelte. Se si crea un carattere per uso personale, scegliere **Carattere personalizzato.** Se si vuole creare un carattere che può essere usato come carattere predefinito di Agent, scegliere **Carattere predefinito**. Verrà pre-configurato l'editor con tutti i nomi di animazione necessari e le assegnazioni dello stato dell'animazione, nonché verrà impostata l'opzione **Supports Standard Animation Set (Supporto** set di animazioni standard). Analogamente, se si sceglie un Office assistente, l'editor è preconfigurato con i nomi di animazione e l'assegnazione dello stato dell'animazione necessari per un Office assistant. Questa azione seleziona **l'icona Carattere** nell'albero e visualizza le relative pagine delle proprietà sul lato destro della finestra. Le sezioni seguenti descrivono come impostare le proprietà del carattere e come creare animazioni per il carattere.

### <a name="setting-your-characters-general-information"></a>Impostazione delle informazioni generali del carattere

Per iniziare a definire un carattere, immettere il nome del carattere nella **casella di** testo Nome (massimo 32 caratteri). Poiché Microsoft Agent usa il nome per consentire agli utenti di accedere al carattere, specificare un nome descrittivo. Specificare un nome che possa essere pronunciato usando l'ortografia convenzionale oppure disabilitare l'input vocale per il carattere. È anche possibile specificare una breve descrizione facoltativa (256 caratteri) per il carattere nella casella di testo Descrizione. Il server espone le informazioni immesse nella casella di testo Descrizione alle applicazioni client.

È anche possibile archiviare i propri dati come parte del carattere usando il campo ExtraData. È possibile usare questa funzionalità per includere informazioni speciali sul carattere o su altri dati. Dopo la compilazione con l'editor di caratteri, è possibile accedere a queste informazioni usando la proprietà ExtraData in fase di esecuzione quando il carattere viene caricato.

È possibile impostare il nome, la descrizione e le informazioni aggiuntive sui dati del carattere in base all'impostazione dell'ID lingua del carattere. Per impostare questi dati per un'altra lingua, selezionare Lingua e immettere il testo. È inoltre necessario che le tabelle codici della lingua siano installate nel sistema in cui si compila il file di caratteri. Se non si specificano le impostazioni della lingua appropriate, non verranno incluse nel file di caratteri compilato. Non è necessario fornire informazioni in altre lingue. Se queste proprietà vengono query in fase di esecuzione usando l'API di Agent e non sono disponibili impostazioni specifiche per tale lingua, vengono restituite le impostazioni per la lingua inglese (predefinita).

### <a name="setting-your-characters-output-options"></a>Impostazione delle opzioni di output del carattere

Se si imposta l'opzione Supports Standard Animation Set (Supporta set di animazioni standard), l'editor di caratteri verifica di aver incluso tutte le animazioni e le assegnazioni di stato di animazione necessarie per un carattere predefinito quando si tenta di compilare il carattere. Se manca un elemento, in una finestra di messaggio verranno elencati gli elementi mancanti. Per informazioni dettagliate sul set di animazioni standard, vedere [**Progettazione di caratteri per Microsoft Agent.**](designing-characters-for-microsoft-agent.md)

Per l'output parlato del tuo carattere, Microsoft Agent offre la possibilità di scegliere tra una voce sintetizzata e sintesi vocale (TTS) o una voce che usa file audio registrati. Se si vuole usare una voce sintetizzata, selezionare l'opzione Use Synthesized Speech For Voice Output (Usa sintesi vocale per output vocale). Verrà aggiunta una pagina Voce per la selezione delle caratteristiche della voce. Scegliere la pagina Voce e usare i controlli nella pagina per selezionare una voce, una velocità e un passo di tutti i motori TTS compatibili installati. L'intervallo dei parametri vocali che è possibile selezionare dipende dai motori TTS. Se non è ancora stato installato un motore TTS, l'elenco di ID voce sarà vuoto. È necessario che sia installato un motore TTS prima di definire le impostazioni vocali del carattere nell'editor di caratteri dell'agente.

Se si prevede di usare un motore TTS per l'output del carattere, è necessario installare anche tale motore nel sistema dell'utente. Se si seleziona una voce basata su un motore TTS specifico, ma l'utente ha un motore TTS diverso installato, il server tenta di trovare una corrispondenza con la voce in base alle caratteristiche definite nell'Editor caratteri dell'agente.

Se si prevede di usare file audio registrati (. FILE WAV) per l'output parlato del carattere, non è necessario selezionare l'opzione Use Synthesized Speech For Voice Output (Usa sintesi vocale per output vocale). Sarà invece necessario registrare separatamente i file audio di output parlato e caricarli dal codice dell'applicazione.

**L'opzione Usa fumetto** parola consente di determinare se si vuole supportare un fumetto per il carattere. Questa funzionalità può essere impostata anche in fase di esecuzione.

Quando **l'opzione Usa fumetto** parola è selezionata, è possibile accedere alla **pagina Fumetto** parola. Le opzioni nella pagina **Fumetto** parola consentono di modificare le caratteristiche predefinite del fumetto. **L'impostazione Caratteri per** riga consente di definire la larghezza del fumetto in base al numero medio di caratteri per riga. È possibile impostare l'altezza predefinita in base a un numero fisso di righe da visualizzare contemporaneamente o ridimensionata automaticamente in base al testo specificato nel [**metodo Speak.**](speak-method.md) È anche possibile specificare se il fumetto viene nascosto automaticamente dopo il completamento di un metodo **Speak** e se il balloon visualizza automaticamente le parole o "accelera" l'impostazione della velocità di output vocale del carattere.

La **pagina Fumetto** parola consente anche di impostare il tipo di carattere predefinito per il fumetto delle parole del carattere e i colori di visualizzazione del fumetto. Tenere tuttavia presente che gli utenti possono eseguire l'override delle impostazioni del tipo di carattere del fumetto usando la finestra delle proprietà di Microsoft Agent.

### <a name="setting-your-characters-identifier"></a>Impostazione dell'identificatore del carattere

Ogni carattere richiede un identificatore univoco (GUID). Il server usa l'identificatore per distinguere i caratteri. Quando si crea un nuovo carattere, l'editor crea automaticamente un nuovo identificatore per il carattere. È necessario modificare l'identificatore di un carattere solo se è stato copiato il file di definizione dei caratteri di un altro carattere o se si vuole distinguere intenzionalmente un carattere da una versione precedente. Per modificare l'identificatore di un carattere, fare clic sul pulsante Nuovo GUID per fare in modo che l'editor generi un nuovo identificatore.

 

 




