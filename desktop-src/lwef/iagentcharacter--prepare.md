---
title: Preparazione IAgentCharacter
description: Preparazione IAgentCharacter
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de29c49960bbfd00a6e0d0e9ff1cb055a01cb930c414708fe9144ff0ff4b75af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119725329"
---
# <a name="iagentcharacterprepare"></a>IAgentCharacter::P repare

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

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

Valore che indica il tipo di dati dell'animazione da caricare che deve essere uno dei seguenti:



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
| **"Gesturing"**      | Per recuperare tutte **le animazioni di stato** di inserimento. |
| **"GesturingDown"**  | Per recuperare **animazioni GesturingDown.**       |
| **"GesturingLeft"**  | Per recuperare **le animazioni GesturingLeft.**       |
| **"GesturingRight"** | Per recuperare **le animazioni GesturingRight.**      |
| **"GesturingUp"**    | Per recuperare **animazioni GesturingUp.**         |
| **"Nascondi"**         | Per recuperare le animazioni di stato **Nascondi.**    |
| **"Ascolto"**        | Per recuperare le animazioni **dello stato** dell'udito.   |
| **"Idling"**         | Per recuperare tutte le animazioni con stato **Idling.**    |
| **"IdlingLevel1"**   | Per recuperare tutte **le animazioni IdlingLevel1.**    |
| **"IdlingLevel2"**   | Per recuperare tutte **le animazioni IdlingLevel2.**    |
| **"IdlingLevel3"**   | Per recuperare tutte **le animazioni IdlingLevel3.**    |
| **"Listening"**      | Per recuperare le **animazioni dello** stato di ascolto. |
| **"Moving"**         | Per recuperare tutte le **animazioni di** stato in movimento.    |
| **"MovingDown"**     | Per recuperare tutte le **animazioni** in movimento.          |
| **"MovingLeft"**     | Per recuperare tutte **le animazioni MovingLeft.**      |
| **"MovingRight"**    | Per recuperare tutte **le animazioni MovingRight.**     |
| **"MovingUp"**       | Per recuperare tutte **le animazioni MovingUp.**        |
| **"Showing"**        | Per recuperare le **animazioni dello** stato Showing.   |
| **"Speaking"**       | Per recuperare le **animazioni dello** stato Speaking.  |



 

Per. File WAV, impostare *bszName* sull'URL o sulla specifica del file per . File WAV. Se la specifica non è completa, viene interpretata come relativa alla specifica usata nel [**metodo Load.**](https://www.bing.com/search?q=**Load**)

</dd> <dt>

<span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*
</dt> <dd>

Valore booleano che specifica se il server accoda la [**richiesta prepare.**](/windows/desktop/lwef/iagentcharacter--prepare) **True** accoda la richiesta e fa in modo che qualsiasi richiesta di animazione che la segue attenda il caricamento dei dati di animazione specificati. **False** recupera i dati dell'animazione in modo asincrono.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID [**della**](/windows/desktop/lwef/iagentcharacter--prepare) richiesta di preparazione.

</dd> </dl>

Se si carica un carattere usando il protocollo HTTP (un oggetto . ACF), è necessario usare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per recuperare i dati dell'animazione prima di poter riprodurre l'animazione. Non è possibile usare questo metodo se il carattere è stato caricato usando il protocollo UNC (un . file ACS). Non è inoltre possibile recuperare i dati HTTP per un carattere usando **Prepare** se tale carattere è stato caricato usando il protocollo UNC (. file di caratteri ACS).

I dati di animazione o audio recuperati [**con il metodo Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) vengono archiviati nella cache del browser. Le chiamate successive controllano la cache e, se i dati dell'animazione sono già presenti, il controllo carica i dati direttamente dalla cache. Dopo il caricamento, i dati dell'animazione o del suono possono essere riprodotti con [**i metodi Play**](/windows/desktop/lwef/iagentcharacter--play) o [**Speak.**](/windows/desktop/lwef/iagentcharacter--speak)

È possibile specificare più animazioni e stati separandoli con virgole. Non è tuttavia possibile combinare tipi nella stessa [**istruzione Prepare.**](/windows/desktop/lwef/iagentcharacter--prepare)

 

