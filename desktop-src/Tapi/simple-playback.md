---
description: L'argomento seguente descrive come eseguire una riproduzione semplice.
ms.assetid: 37869822-aed7-4102-8110-5a896400885c
title: Riproduzione semplice
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51724b92fea0a46850609e96de85231a9f1df1f7e538f6def4df07442ef19ca2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118862227"
---
# <a name="simple-playback"></a>Riproduzione semplice

L'argomento seguente descrive come eseguire una riproduzione semplice.

**Per eseguire una riproduzione semplice**

1.  Selezionare Il terminale di riproduzione file a livello di chiamata.
2.  Creare il terminale di riproduzione nella chiamata TAPI.
3.  Impostare le proprietà, ovvero il nome del file e il tipo di archiviazione.
4.  Chiamare il [**metodo Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) nel terminale di riproduzione file per avviare la riproduzione dei flussi.

Il codice di esempio seguente illustra una riproduzione semplice.

Per prima cosa, usare [**l'interfaccia ITBasicCallControl2**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2) per creare il terminale per la registrazione. Questo indica al provider di servizi di configurazione/provider di servizi di configurazione di eseguire la riproduzione di file in questa chiamata. Il provider di servizi di configurazione/provider di servizi di configurazione crea un terminale che l'applicazione può usare e lo restituisce in caso di esito positivo.


```C++

```



Ottenere il [**puntatore all'interfaccia ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) dall'interfaccia del terminale e usarlo per impostare il nome del file da riprodurre.


```C++
pMediaPlayback->Release();
```



Supponendo che il file contenga un flusso audio e che la chiamata abbia un flusso audio di acquisizione, il contenuto audio nel file verrà riprodotto in tale flusso.

 

 



