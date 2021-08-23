---
title: Oggetto immagine standard
description: Oggetto immagine standard
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4b74daa4f62791c12927eba3fd0472ed2a956d4b84c03e3cc373c44e12ce25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129763"
---
# <a name="standard-picture-object"></a>Oggetto immagine standard

L'oggetto immagine standard fornisce un'astrazione indipendente dalla lingua per le immagini GDI: bitmap, icone, metafile e metafile migliorati. Come per l'oggetto tipo di carattere standard, il sistema fornisce un'implementazione standard di questo oggetto. Le interfacce principali sono [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) e [**IPictureDisp,**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)le ultime derivate da **IDispatch** per fornire l'accesso alle proprietà dell'immagine tramite l'automazione OLE. Viene creato un nuovo oggetto immagine con [**OleCreatePictureIndirect.**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect)

L'oggetto immagine supporta anche l'interfaccia in uscita [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) in modo che un client possa determinare quando le proprietà dell'immagine cambiano. Di conseguenza, l'oggetto immagine supporta anche [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) e un punto di connessione **per IPropertyNotifySink.**

L'oggetto immagine supporta anche [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) in modo che possa salvare e caricare se stesso da un'istanza di [**IStream.**](/windows/desktop/api/objidl/nn-objidl-istream) Un oggetto che usa internamente un oggetto immagine in genere salva e carica l'immagine come parte della gestione della persistenza dell'oggetto. La [**funzione OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) semplifica la creazione di un oggetto immagine in base al contenuto del flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà dei controlli](control-properties.md)
</dt> </dl>

 

 