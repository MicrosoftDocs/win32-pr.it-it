---
title: Cache degli attributi ADSI
description: Il modello a oggetti ADSI fornisce una cache degli attributi sul lato client per ogni oggetto ADSI.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- ADSI cache degli attributi ADSI
- ADSI ADSI, uso, accesso e manipolazione di dati con ADSI, cache degli attributi
- attributi ADSI, caching degli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df3062ed5862f11e9db5dadd83b80ac624218c81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103707375"
---
# <a name="the-adsi-attribute-cache"></a>Cache degli attributi ADSI

Il modello a oggetti ADSI fornisce una cache degli attributi sul lato client per ogni oggetto ADSI. La cache degli attributi è paragonabile a una tabella in memoria che contiene i nomi e i valori della maggior parte degli attributi degli oggetti che sono stati scaricati. Alcuni attributi, ad esempio gli attributi operativi, non vengono memorizzati nella cache. ADSI utilizza la memorizzazione nella cache delle proprietà per migliorare le prestazioni della manipolazione degli attributi e aggiungere la funzionalità di transazione per le operazioni di lettura e scrittura degli attributi. Questa funzionalità è essenziale per i client scritti in linguaggi che non dispongono di un meccanismo di invio in batch nativo per l'impostazione di attributi, ad esempio Microsoft Visual Basic Development System. Senza la cache delle proprietà ADSI, tali client dovranno accedere al server ogni volta che un attributo viene letto o scritto.

Quando un oggetto viene creato o associato per la prima volta a, la cache delle proprietà per l'oggetto è vuota. Quando viene chiamato il metodo [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) , ADSI carica gli attributi richiesti per l'oggetto dal servizio directory sottostante nella cache locale. Quando viene letto un valore di attributo specifico e la cache è vuota, ADSI esegue una chiamata implicita al metodo **IADs:: GetInfo** . Quando la cache viene riempita, tutte le operazioni di lettura degli attributi funzionano solo sul contenuto della cache.

Quando viene scritto un valore di attributo, il nuovo valore viene archiviato nella cache locale fino a quando non viene chiamato il metodo [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) . Quando viene chiamato il metodo **IADs:: SetInfo** , viene eseguito il commit degli attributi nella cache nel servizio directory sottostante. Dopo la chiamata al metodo **IADs:: SetInfo** , i valori rimangono nella cache fino a quando non vengono aggiornati in modo esplicito con un'altra chiamata al metodo [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) .

> [!IMPORTANT]
> È necessario usare attentamente il metodo [**IADs:: GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) perché questo metodo sovrascriverà sempre i valori dell'attributo nella cache dal servizio directory sottostante, anche se il valore memorizzato nella cache è stato modificato. Ovvero, sovrascriverà i valori di attributo che sono stati modificati nella cache, ma non ne è stato eseguito il commit nel servizio directory sottostante con una chiamata al metodo [**IADs:: SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) .

 

Nella figura seguente vengono illustrati i diversi metodi utilizzati per operare sulla cache.

![cache degli attributi ADSI](images/ds2propc.png)

 

 




