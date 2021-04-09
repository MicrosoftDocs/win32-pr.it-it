---
title: Persistenza
description: Persistenza
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ba5fc0c8e389c7babdf80b76719b39fc02d5604
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047458"
---
# <a name="persistence"></a>Persistenza

Un controllo implementa una o più interfacce di persistenza per supportare la persistenza dello stato. Ad esempio, l'interfaccia [**IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) supporta la persistenza basata sul flusso dello stato del controllo. **IPersistStreamInit** è una sostituzione di [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) e aggiunge un metodo di inizializzazione, [**InitNew**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew). Gli altri metodi sono gli stessi in entrambe le interfacce. **IPersistStreamInit** non è derivato da **IPersistStream**; un oggetto supporta solo una delle due interfacce a seconda che sia necessaria la possibilità di inizializzare nuove istanze di se stesso.

Altre interfacce di persistenza che possono essere offerte da un controllo includono: [**IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**Metodo IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768205(v=vs.85)), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)). L'implementatore del controllo deve decidere quali tipi di persistenza sono più importanti e implementare le interfacce di persistenza appropriate. L'implementatore del controllo decide anche cosa salvare. Ad esempio, un controllo può salvare i valori correnti delle proprietà o la posizione e le dimensioni all'interno del relativo contenitore. Il client decide quale interfaccia si preferisce usare.

Prima di caricare un controllo dallo stato persistente, un client può controllare il \_ flag SETCLIENTSITEFIRST di OLEMISC per determinare se il controllo supporta il recupero delle proprietà di ambiente e del sito client prima del caricamento dello stato persistente. Questa ottimizzazione può risparmiare tempo quando si crea un'istanza di un controllo, poiché il controllo è libero di ignorare i valori persistenti anziché caricarli solo per eseguirne l'override dalle proprietà di ambiente fornite dal client.

Un controllo può inoltre supportare il salvataggio e il ripristino dello stato in un set di proprietà OLE, un set di identificatori e valori in un formato specificato. Questa funzionalità può essere utile con i contenitori, ad esempio Visual Basic, che consente di salvare i propri programmi in formato testuale. Un controllo che desidera supportare questa funzionalità implementa [**IDataObject:: GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) e [**IDataObject:: SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) per passare i valori delle proprietà rispettivamente a e dal contenitore. Il processo del contenitore consente di convertire queste informazioni in testo e salvarle. Gli identificatori utilizzati dal controllo corrispondono ai nomi delle proprietà del controllo e ai valori. Vedere OLE CDK per la definizione di questo set di proprietà.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Controlli ActiveX](activex-controls.md)
</dt> </dl>

 

 