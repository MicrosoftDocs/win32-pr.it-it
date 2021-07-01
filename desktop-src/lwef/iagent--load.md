---
title: Caricamento IAgent
description: Caricamento IAgent
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80ce2835d60f3edce6f45d181927437ba6e58b18
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120934"
---
# <a name="iagentload"></a>IAgent::Load

\[Microsoft Agent è deprecato a livello di Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

Carica un carattere nella [**raccolta Characters.**](./iagent.md)

-   Restituisce S \_ OK per indicare che l'operazione è riuscita.

<dl> <dt>

<span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*
</dt> <dd>

Tipo di dati variant che deve essere uno dei seguenti:



| Valore           | Descrizione                                                                      |
|------------|-----------------------------------------------------------------------|
| *filespec* | Percorso locale del file di definizione del carattere specificato. |
| *URL*      | Indirizzo HTTP per il file di definizione del carattere.                 |



 

</dd> <dt>

<span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID del carattere.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID [**richiesta**](load-method.md) di caricamento.

</dd> </dl>

È possibile caricare caratteri dalla sottodirectory di Microsoft Agent specificando un percorso relativo(uno che non include due punti o una barra iniziale). Questo antefissi il percorso con la directory dei caratteri di Agent (che si trova nella directory localizzata %windows% \\ msagent). È anche possibile usare un indirizzo relativo per specificare la propria directory nella directory Chars di Agent.

Non è possibile caricare più volte lo stesso carattere (un carattere con lo stesso GUID) da una singola connessione. Analogamente, non è possibile caricare il carattere predefinito e altri caratteri contemporaneamente da una singola connessione, perché il carattere predefinito potrebbe essere lo stesso dell'altro carattere. Tuttavia, è possibile creare un'altra connessione (usando CoCreateInstance) e caricare lo stesso carattere.

Il provider di dati di Microsoft Agent supporta il caricamento di dati di tipo carattere archiviati come singolo file strutturato (. ACS) con dati di tipo carattere e dati di animazione insieme o come dati di tipo carattere separati (. ACF) e animazione (. ACA). In genere, usare il singolo strutturato . File ACS per caricare un carattere archiviato in un'unità disco locale o in una rete e accessibile tramite il protocollo di file convenzionale ,ad esempio i nomi di percorso UNC. Usare l'oggetto separato . ACF e . File ACA quando si desidera caricare i file di animazione singolarmente da un sito remoto a cui si accede tramite il protocollo HTTP.

Per. I file ACS, usando [**il metodo Load,**](load-method.md) forniscono l'accesso alle animazioni di un carattere. Dopo il caricamento, è possibile usare il [**metodo Play**](play-method.md) per animare il carattere. Per. File ACF, si usa anche il [**metodo Prepare per**](/windows/desktop/lwef/iagentcharacter--prepare) caricare i dati dell'animazione. Il **metodo Load** non supporta il download di . File ACS da un sito HTTP.

Il caricamento di un carattere non visualizza automaticamente il carattere. Usare prima [**il metodo Show**](show-method.md) per rendere visibile il carattere.

 

 