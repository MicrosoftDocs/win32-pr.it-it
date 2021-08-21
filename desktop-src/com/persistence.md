---
title: Persistenza
description: Persistenza
ms.assetid: 4916ea52-a21c-4938-81cb-392b5ca1f6c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c8600307bfe6c29f72fb9d29e633358062c4e8c1c61da8898173cf190f1d08
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500331"
---
# <a name="persistence"></a>Persistenza

Un controllo implementa una o più interfacce di persistenza per supportare la persistenza del relativo stato. Ad esempio, [**l'interfaccia IPersistStreamInit**](/windows/desktop/api/OCIdl/nn-ocidl-ipersiststreaminit) supporta la persistenza basata sul flusso dello stato del controllo. **IPersistStreamInit è** una sostituzione di [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) e aggiunge un metodo di inizializzazione, [**InitNew**](/windows/desktop/api/OCIdl/nf-ocidl-ipersiststreaminit-initnew). Gli altri metodi sono gli stessi in entrambe le interfacce. **IPersistStreamInit** non deriva da **IPersistStream.** un oggetto supporta solo una delle due interfacce a seconda che richieda la possibilità di inizializzare nuove istanze di se stesso.

Altre interfacce di persistenza che un controllo può offrire [**includono: IPersistStorage**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststorage), [**IPersistMemory**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa768210(v=vs.85)), [**IPersistPropertyBag**](/windows/win32/api/ocidl/nn-ocidl-ipersistpropertybag), [**IPersistMoniker**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775042(v=vs.85)). L'implementatore del controllo deve decidere quali tipi di persistenza sono più importanti e implementare le interfacce di persistenza appropriate. L'implementatore del controllo decide anche cosa salvare. Ad esempio, un controllo può salvare i valori correnti delle relative proprietà o la posizione e le dimensioni all'interno del contenitore. Il client decide quale interfaccia preferisce usare.

Prima di caricare un controllo dallo stato persistente, un client può controllare il flag OLEMISC SETCLIENTSITEFIRST per determinare se il controllo supporta l'recupero del sito client e delle proprietà di ambiente prima di caricarne lo stato \_ permanente. Questa ottimizzazione consente di risparmiare tempo quando si crea un'istanza di un controllo poiché il controllo è quindi libero di ignorare i relativi valori persistenti anziché caricarli solo per sottoporli a override dalle proprietà di ambiente fornite dal client.

Un controllo può anche supportare il salvataggio e il ripristino dello stato in un set di proprietà OLE, un set di identificatori e valori in un formato specificato. Questa funzionalità può essere utile con contenitori come Visual Basic, che salva i programmi in un formato testuale. Un controllo che vuole supportare questa funzionalità implementa [**IDataObject::GetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-getdata) e [**IDataObject::SetData**](/windows/desktop/api/ObjIdl/nf-objidl-idataobject-setdata) per passare rispettivamente i valori delle proprietà a e dal contenitore. È compito del contenitore convertire queste informazioni in testo e salvarle. Gli identificatori utilizzati dal controllo corrispondono ai nomi delle proprietà del controllo e ai valori. Per la definizione di questo set di proprietà, vedere OLE CDK.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[ActiveX Controlli](activex-controls.md)
</dt> </dl>

 

 