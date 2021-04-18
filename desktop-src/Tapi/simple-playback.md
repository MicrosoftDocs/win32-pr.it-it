---
description: Nell'argomento seguente viene descritto come eseguire la riproduzione semplice.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Riproduzione semplice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0a7d07e37721bc84abb71c683ce4441580a80e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106318935"
---
# <a name="simple-playback"></a>Riproduzione semplice

Nell'argomento seguente viene descritto come eseguire la riproduzione semplice.

**Per eseguire la riproduzione semplice**

1.  Selezionare il terminale riproduzione file a livello di chiamata.
2.  Creare il terminale di riproduzione nella chiamata TAPI.
3.  Impostare le proprietà: nome file e tipo di archiviazione.
4.  Chiamare il metodo [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) sul terminale riproduzione file per avviare la riproduzione dei flussi.

Il codice di esempio seguente illustra la riproduzione semplice.

Per prima cosa, usare l'interfaccia [**ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) per creare il terminale per la registrazione. Indica a TSP/MSP di eseguire la riproduzione dei file in questa chiamata. Il TSP/MSP crea un terminale che l'applicazione deve usare e la restituisce in seguito al completamento dell'operazione.


```C++

```



Ottenere il puntatore all'interfaccia [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) dall'interfaccia terminal e usarlo per impostare il nome del file per la riproduzione.


```C++
pMediaPlayback->Release();
```



Supponendo che il file contenga un flusso audio e che la chiamata disponga di un flusso audio di acquisizione, il contenuto audio nel file verrà riprodotto in quel flusso.

 

 



