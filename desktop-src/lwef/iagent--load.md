---
title: Carico IAgent
description: Carico IAgent
ms.assetid: 8f25e6b6-a117-4b37-969a-d8f80c7be224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4e30a25abb631714384f8349a9d260deade0d6d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103963061"
---
# <a name="iagentload"></a>IAgent:: Load

\[Microsoft Agent è stato deprecato a partire da Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

``` syntax
HRESULT Load(
   VARIANT vLoadKey,  // data provider
   long * pdwCharID,  // address of a variable for character ID
   long * pdwReqID    // address of a variable for request ID
);
```

Carica un carattere nella raccolta di [**caratteri**](./iagent.md) .

-   Restituisce \_ OK per indicare che l'operazione è stata completata.

<dl> <dt>

<span id="vLoadKey"></span><span id="vloadkey"></span><span id="VLOADKEY"></span>*vLoadKey*
</dt> <dd>

Tipo di dati Variant che deve essere uno dei seguenti:



|            |                                                                       |
|------------|-----------------------------------------------------------------------|
| *filespec* | Percorso del file locale del file di definizione del carattere specificato. |
| *URL*      | Indirizzo HTTP per il file di definizione del carattere.                 |



 

</dd> <dt>

<span id="pdwCharID"></span><span id="pdwcharid"></span><span id="PDWCHARID"></span>*pdwCharID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID del carattere.

</dd> <dt>

<span id="pdwReqID"></span><span id="pdwreqid"></span><span id="PDWREQID"></span>*pdwReqID*
</dt> <dd>

Indirizzo di una variabile che riceve l'ID della richiesta di [**caricamento**](load-method.md) .

</dd> </dl>

È possibile caricare i caratteri dalla sottodirectory Microsoft Agent specificando un percorso relativo, ovvero uno che non include i due punti o un carattere di barra iniziali. Questa operazione previene il prefisso del percorso con la directory characters di Agent, che si trova nella directory% Windows% msagent localizzata \\ . È anche possibile usare un indirizzo relativo per specificare la propria directory nella directory chars dell'agente.

Non è possibile caricare più volte lo stesso carattere, ovvero un carattere con lo stesso GUID, da una singola connessione. Analogamente, non è possibile caricare contemporaneamente il carattere predefinito e altri caratteri da una singola connessione, perché il carattere predefinito potrebbe essere uguale a quello dell'altro carattere. Tuttavia, è possibile creare un'altra connessione (usando CoCreateInstance) e caricare lo stesso carattere.

Il provider di dati Microsoft Agent supporta il caricamento di dati di tipo carattere archiviati come singolo file strutturato (. ACS) con dati di tipo carattere e dati di animazione insieme o come dati di tipo carattere separati (. ACF) e animazione (. File ACA). In genere, usare il singolo strutturato. File ACS per caricare un carattere archiviato in un'unità disco o in una rete locale e a cui si accede utilizzando il protocollo file convenzionale, ad esempio i percorsi UNC. Usare l'oggetto separato. ACF e. File ACA quando si desidera caricare i file di animazione singolarmente da un sito remoto a cui si accede utilizzando il protocollo HTTP.

Per. I file ACS, usando il metodo [**Load**](load-method.md) , consentono di accedere alle animazioni di un carattere; una volta caricato, è possibile usare il metodo [**Play**](play-method.md) per animare il carattere. Per. File ACF, viene usato anche il metodo [**Prepare**](/windows/desktop/lwef/iagentcharacter--prepare) per caricare i dati dell'animazione. Il metodo **Load** non supporta il download. File ACS da un sito HTTP.

Il caricamento di un carattere non visualizza automaticamente il carattere. Usare prima il metodo [**show**](show-method.md) per rendere visibile il carattere.

 

 