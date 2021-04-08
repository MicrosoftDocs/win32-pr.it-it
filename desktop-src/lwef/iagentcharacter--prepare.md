---
title: IAgentCharacter preparare
description: IAgentCharacter preparare
ms.assetid: e016039f-a0b1-4ae9-bff6-7212b02c1ad8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3eebee8d2ea99c8782e9506e0e4a812cfb277487
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046710"
---
# <a name="iagentcharacterprepare"></a>IAgentCharacter::P ripare

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Prepare(
   long dwType,     // type of animation data to load
   BSTR bszName,    // name of the animation 
   long bQueue,     // queue the request
   long * pdwReqID  // address of request ID
);
```

Recupera i dati di animazione per un carattere.

-   Restituisce \_ OK per indicare che l'operazione è stata completata. Quando la funzione restituisce, *pdwReqID* contiene l'ID della richiesta.

<dl> <dt>

<span id="dwType"></span><span id="dwtype"></span><span id="DWTYPE"></span>*dwType*
</dt> <dd>

Valore che indica il tipo di dati di animazione da caricare che deve essere uno dei seguenti:



| Valore                                                           | Descrizione                                                |
|-----------------------------------------------------------------|------------------------------------------------------------|
| animazione di preparazione **breve const senza segno** **\_ = 0;**<br/> | Dati di animazione di un carattere.                              |
| stato di preparazione **short senza segno const** **\_ = 1;**<br/>     | Dati dello stato di un carattere.                                  |
| **const unsigned short** **preparate \_ Wave = 2**<br/>       | File audio di un carattere (. WAV o. LWV) per l'output parlato. |



 

</dd> <dt>

<span id="bszName"></span><span id="bszname"></span><span id="BSZNAME"></span>*bszName*
</dt> <dd>

Nome dell'animazione o dello stato.

Il nome dell'animazione è basato su quello definito per il carattere quando è stato salvato mediante l'editor dei caratteri di Microsoft Agent.

Per gli Stati, il valore può essere uno dei seguenti:



|                      |                                                 |
|----------------------|-------------------------------------------------|
| **Gesturing**      | Per recuperare tutte le animazioni dello stato **gestuale** . |
| **"GesturingDown"**  | Per recuperare le animazioni **GesturingDown** .       |
| **"GesturingLeft"**  | Per recuperare le animazioni **GesturingLeft** .       |
| **"GesturingRight"** | Per recuperare le animazioni **GesturingRight** .      |
| **"GesturingUp"**    | Per recuperare le animazioni **GesturingUp** .         |
| **Nascondere**         | Per recuperare le animazioni di stato **nascoste** .    |
| **Udienza**        | Per recuperare le animazioni dello stato di **udito** .   |
| **Inattivi**         | Per recuperare tutte le animazioni di stato **minimo** .    |
| **"IdlingLevel1"**   | Per recuperare tutte le animazioni **IdlingLevel1** .    |
| **"IdlingLevel2"**   | Per recuperare tutte le animazioni **IdlingLevel2** .    |
| **"IdlingLevel3"**   | Per recuperare tutte le animazioni **IdlingLevel3** .    |
| **In ascolto**      | Per recuperare le animazioni dello stato di **ascolto** . |
| **Movimento**         | Per recuperare tutte le animazioni dello stato di **trasferimento** .    |
| **"MovingDown"**     | Per recuperare tutte le animazioni in **evoluzione** .          |
| **"MovingLeft"**     | Per recuperare tutte le animazioni **MovingLeft** .      |
| **"MovingRight"**    | Per recuperare tutte le animazioni **MovingRight** .     |
| **"MovingUp"**       | Per recuperare tutte le animazioni **MovingUp** .        |
| **Che Mostra**        | Per **recuperare le animazioni di visualizzazione dello** stato.   |
| **Parlando**       | Per recuperare le animazioni dello stato di **pronuncia** .  |



 

Per. File WAV, impostare *bszName* sull'URL o sulla specifica del file per. File WAV. Se la specifica non è completa, viene interpretata come relativa alla specifica utilizzata nel metodo [**Load**](https://www.bing.com/search?q=**Load**) .

</dd> <dt>

<span id="bQueue"></span><span id="bqueue"></span><span id="BQUEUE"></span>*bQueue*
</dt> <dd>

Valore booleano che specifica se il server accoda la richiesta di [**preparazione**](/windows/desktop/lwef/iagentcharacter--prepare) . **True** Accoda la richiesta e causa l'attesa di qualsiasi richiesta di animazione che la segua finché non vengono caricati i dati di animazione specificati. **False** recupera i dati di animazione in modo asincrono.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID della richiesta di [**preparazione**](/windows/desktop/lwef/iagentcharacter--prepare) .

</dd> </dl>

Se si carica un carattere usando il protocollo HTTP (un. File ACF), è necessario usare il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per recuperare i dati di animazione prima di poter riprodurre l'animazione. Non è possibile usare questo metodo se il carattere è stato caricato usando il protocollo UNC (un. File ACS). Non è inoltre possibile recuperare i dati HTTP per un carattere utilizzando **prepara** se è stato caricato il carattere utilizzando il protocollo UNC (. File di caratteri ACS).

I dati di animazione o audio recuperati con il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) vengono archiviati nella cache del browser. Le chiamate successive verificheranno la cache e, se i dati di animazione sono già presenti, il controllo caricherà i dati direttamente dalla cache. Una volta caricati, i dati di animazione o audio possono essere riprodotti con i metodi [**Play**](/windows/desktop/lwef/iagentcharacter--play) o [**Speak**](/windows/desktop/lwef/iagentcharacter--speak) .

È possibile specificare più animazioni e Stati separandoli con virgole. Tuttavia, non è possibile combinare tipi nella stessa istruzione [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) .

 

