---
title: Oggetto immagine standard
description: Oggetto immagine standard
ms.assetid: 2df9e0a7-444b-454c-983a-82e82b9ed9d1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e8a711fc0c33cf5e99b0db6e90941dbe855289b
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "103963486"
---
# <a name="standard-picture-object"></a>Oggetto immagine standard

L'oggetto Picture standard fornisce un'astrazione indipendente dal linguaggio per le immagini GDI: bitmap, icone, metafile e metafile avanzati. Come per l'oggetto tipo di carattere standard, il sistema fornisce un'implementazione standard di questo oggetto. Le interfacce primarie sono [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) e [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp), il secondo derivato da **IDispatch** per fornire l'accesso alle proprietà dell'immagine tramite l'automazione OLE. Un oggetto immagine viene creato nuovo con [**OleCreatePictureIndirect**](/windows/desktop/api/OleCtl/nf-olectl-olecreatepictureindirect).

L'oggetto Picture supporta inoltre l'interfaccia in uscita [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) in modo che un client possa determinare quando le proprietà dell'immagine cambiano. Di conseguenza, l'oggetto immagine supporta anche [**IConnectionPointContainer**](/windows/desktop/api/OCIdl/nn-ocidl-iconnectionpointcontainer) e un punto di connessione per **IPropertyNotifySink**.

L'oggetto Picture supporta inoltre [**IPersistStream**](/windows/desktop/api/ObjIdl/nn-objidl-ipersiststream) in modo che possa salvare e caricare autonomamente da un'istanza di [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream). Un oggetto che utilizza un oggetto immagine internamente normalmente Salva e carica l'immagine come parte della gestione della persistenza dell'oggetto. La funzione [**OleLoadPicture**](/windows/desktop/api/OleCtl/nf-olectl-oleloadpicture) semplifica la creazione di un oggetto immagine in base al contenuto del flusso.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del controllo](control-properties.md)
</dt> </dl>

 

 