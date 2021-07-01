---
title: Preparazione di IAgentCharacter
description: Preparazione di IAgentCharacter
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b383bf10330934379990693b75fe2908a432f8d5
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119876"
---
# <a name="iagentcharacterprepare"></a>IAgentCharacter::P repare

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

Recupera i dati di animazione per un carattere.

-   Restituisce S \_ OK per indicare che l'operazione è riuscita. Quando la funzione viene restituita, *pdwReqID* contiene l'ID della richiesta.

<dl> <dt>

<span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*
</dt> <dd>

Valore che indica il tipo di dati di animazione da caricare che deve essere uno dei seguenti:



| Valore                                                           | Descrizione                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| **const unsigned short** **PREPARE ANIMATION = \_ 0;**<br/> | Dati di animazione di un carattere.                              |
| **const unsigned short** **PREPARE STATE = \_ 1;**<br/>     | Dati sullo stato di un carattere.                                  |
| **const unsigned short** **PREPARE WAVE = \_ 2**<br/>       | File audio di un carattere (. WAV o . LWV) per l'output parlato. |



 

</dd> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

Nome dell'animazione o dello stato.

Il nome dell'animazione si basa su quello definito per il carattere quando è stato salvato usando l'editor di caratteri di Microsoft Agent.

Per gli stati, il valore può essere uno dei seguenti:



|                      | Descrizione                                     |
|----------------------|-------------------------------------------------|
| **"Gesturing"**      | Per recuperare tutte **le animazioni dello stato** di gesturing. |
| **"GesturingDown"**  | Per recuperare **le animazioni GesturingDown.**       |
| **"GesturingLeft"**  | Per recuperare **le animazioni GesturingLeft.**       |
| **"GesturingRight"** | Per recuperare **le animazioni GesturingRight.**      |
| **"GesturingUp"**    | Per recuperare **le animazioni GesturingUp.**         |
| **"Nascondi"**         | Per recuperare le animazioni di stato **Nascondi.**    |
| **"Ascolto"**        | Per recuperare le animazioni **di stato Hearing.**   |
| **"Idling"**         | Per recuperare tutte le **animazioni di stato di Idling.**    |
| **"IdlingLevel1"**   | Per recuperare tutte **le animazioni IdlingLevel1.**    |
| **"IdlingLevel2"**   | Per recuperare tutte **le animazioni IdlingLevel2.**    |
| **"IdlingLevel3"**   | Per recuperare tutte **le animazioni IdlingLevel3.**    |
| **"Ascolto"**      | Per recuperare le **animazioni dello stato** di ascolto. |
| **"Moving"**         | Per recuperare tutte le **animazioni di** stato in movimento.    |
| **"MovingDown"**     | Per recuperare tutte **le animazioni in** movimento.          |
| **"MovingLeft"**     | Per recuperare tutte **le animazioni MovingLeft.**      |
| **"MovingRight"**    | Per recuperare tutte **le animazioni MovingRight.**     |
| **"MovingUp"**       | Per recuperare tutte **le animazioni MovingUp.**        |
| **"Showing"**        | Per recuperare le **animazioni dello** stato di visualizzazione.   |
| **"Speaking"**       | Per recuperare le **animazioni dello stato Speaking.**  |



 

Per. File WAV, impostare *bszName* sull'URL o sulla specifica del file per . File WAV. Se la specifica non è completa, viene interpretata come relativa alla specifica usata nel [**metodo Load.**](https://www.bing.com/search?q=**Load**)

</dd> <dt>

<span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*
</dt> <dd>

Valore booleano che specifica se il server accoda la [**richiesta Prepare.**](/windows/desktop/lwef/iagentcharacter--prepare) **True** accoda la richiesta e fa in modo che tutte le richieste di animazione che la seguono attendano fino al caricamento dei dati di animazione specificati. **False** recupera i dati di animazione in modo asincrono.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID [**richiesta di**](/windows/desktop/lwef/iagentcharacter--prepare) preparazione.

</dd> </dl>

Se si carica un carattere usando il protocollo HTTP (un oggetto . ACF), è necessario usare il [**metodo Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per recuperare i dati dell'animazione prima di poter riprodurre l'animazione. Non è possibile usare questo metodo se il carattere è stato caricato usando il protocollo UNC (un oggetto . file ACS). Non è inoltre possibile recuperare i dati HTTP per un carattere usando **Prepare** se tale carattere è stato caricato usando il protocollo UNC (. File di caratteri ACS).

I dati di animazione o audio recuperati [**con il metodo Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) vengono archiviati nella cache del browser. Le chiamate successive controllano la cache e, se i dati dell'animazione sono già presenti, il controllo carica i dati direttamente dalla cache. Dopo il caricamento, l'animazione o i dati sonori possono essere riprodotti con i [**metodi Play**](/windows/desktop/lwef/iagentcharacter--play) [**o Speak.**](/windows/desktop/lwef/iagentcharacter--speak)

È possibile specificare più animazioni e stati separandoli con virgole. Tuttavia, non è possibile combinare tipi nella stessa [**istruzione Prepare.**](/windows/desktop/lwef/iagentcharacter--prepare)

 

