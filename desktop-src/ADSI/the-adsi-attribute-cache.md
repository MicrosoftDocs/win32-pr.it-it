---
title: Cache degli attributi ADSI
description: Il modello a oggetti ADSI fornisce una cache degli attributi sul lato client per ogni oggetto ADSI.
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- The ADSI Attribute Cache ADSI
- ADSI ADSI , uso, accesso e modifica dei dati con ADSI, cache degli attributi
- attributi ADSI, memorizzazione nella cache degli attributi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5940d431fc476fdecd8397875bf06a04ed82ea30ab4ed2e98b94ccef98f0e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930047"
---
# <a name="the-adsi-attribute-cache"></a>Cache degli attributi ADSI

Il modello a oggetti ADSI fornisce una cache degli attributi sul lato client per ogni oggetto ADSI. La cache degli attributi è paragonabile a una tabella in memoria che contiene i nomi e i valori della maggior parte degli attributi dell'oggetto scaricati. Alcuni attributi, ad esempio gli attributi operativi, non vengono memorizzati nella cache. ADSI usa la memorizzazione nella cache delle proprietà per migliorare le prestazioni della manipolazione degli attributi e aggiungere funzionalità di transazione per le operazioni di lettura e scrittura degli attributi. Questa funzionalità è fondamentale per i client scritti in linguaggi che non dispongono di un meccanismo di invio in batch nativo per l'impostazione di attributi, ad esempio microsoft Visual Basic di sviluppo. Senza la cache delle proprietà ADSI, tali client devono accedere al server ogni volta che un attributo viene letto o scritto.

Quando un oggetto viene creato o associato per la prima volta, la cache delle proprietà per l'oggetto è vuota. Quando viene chiamato il metodo [**IADs::GetInfo,**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) ADSI carica gli attributi richiesti per l'oggetto dal servizio directory sottostante nella cache locale. Quando viene letto un valore di attributo specifico e la cache è vuota, ADSI esegue una chiamata implicita al metodo **IADs::GetInfo.** Quando la cache viene riempita, tutte le operazioni di lettura degli attributi funzionano solo sul contenuto della cache.

Quando viene scritto un valore di attributo, il nuovo valore viene archiviato nella cache locale fino a quando non viene chiamato il metodo [**IADs::SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) Quando viene **chiamato il metodo IADs::SetInfo,** viene eseguito il commit degli attributi nella cache nel servizio directory sottostante. Dopo la chiamata al metodo **IADs::SetInfo,** i valori rimangono nella cache fino a quando non vengono aggiornati in modo esplicito con un'altra chiamata al metodo [**IADs::GetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-getinfo)

> [!IMPORTANT]
> Il [**metodo IADs::GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) deve essere usato con attenzione perché questo metodo sovrascriverà sempre i valori degli attributi nella cache dal servizio directory sottostante, anche se il valore memorizzato nella cache è stato modificato. Ciò significa che sovrascriverà i valori degli attributi che sono stati modificati nella cache, ma di cui non è stato eseguito il commit nel servizio directory sottostante con una chiamata al metodo [**IADs::SetInfo.**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)

 

La figura seguente illustra i diversi metodi usati per operare sulla cache.

![Cache degli attributi adsi](images/ds2propc.png)

 

 




