---
title: Interfacce (controlli e pagine delle proprietà)
description: Per creare oggetti COM e pagine delle proprietà standard, vengono utilizzate le interfacce seguenti.
ms.assetid: f0d655b3-fa92-4553-ba21-617649a922a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e143ab1793eaf0335bbcf04093707bdc359e868e
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300880"
---
# <a name="interfaces-controls-and-property-pages"></a>Interfacce (controlli e pagine delle proprietà)

Per creare oggetti COM e pagine delle proprietà standard, vengono utilizzate le interfacce seguenti.



| Interfaccia                                             | Descrizione                                                                                                                                                                                                  |
|-------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont)                                | Fornisce un wrapper per un oggetto del tipo di carattere di Windows.                                                                                                                                                             |
| [**IFontDisp**](/windows/win32/api/ocidl/nn-ocidl-ifontdisp)                        | Espone le proprietà di un oggetto del tipo di carattere tramite l'automazione. Fornisce un subset dei metodi [**IFont**](/windows/desktop/api/OCIdl/nn-ocidl-ifont) .                                                                                           |
| [**IOleControl**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrol)                    | Fornisce le funzionalità per supportare i tasti di scelta rapida, le proprietà di ambiente e gli eventi negli oggetti controllo.                                                                                                  |
| [**IOleControlSite**](/windows/desktop/api/OCIdl/nn-ocidl-iolecontrolsite)            | Fornisce i metodi che consentono a un oggetto sito di gestire ogni controllo incorporato all'interno di un contenitore.                                                                                                           |
| [**IPerPropertyBrowsing**](/windows/desktop/api/OCIdl/nn-ocidl-iperpropertybrowsing)  | Recupera le informazioni nelle pagine delle proprietà offerte da un oggetto.                                                                                                                                        |
| [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture)                          | Gestisce un oggetto immagine e le relative proprietà. Gli oggetti immagine forniscono un'astrazione indipendente dal linguaggio per bitmap, icone e metafile.                                                                       |
| [**IPictureDisp**](/windows/win32/api/ocidl/nn-ocidl-ipicturedisp)                  | Espone le proprietà dell'oggetto immagine tramite l'automazione. Fornisce un subset delle funzionalità disponibili tramite i metodi [**IPicture**](/windows/desktop/api/OCIdl/nn-ocidl-ipicture) .                                                |
| [**IPointerInactive**](/windows/desktop/api/OCIdl/nn-ocidl-ipointerinactive)          | Consente a un oggetto di rimanere inattivo nella maggior parte dei casi, continuando comunque a interagire con il mouse, incluso il trascinamento della selezione.                                                                         |
| [**IPrint**](/windows/desktop/api/DocObj/nn-docobj-iprint)                              | Consente di abilitare la stampa a livello di codice in documenti composti in generale e in documenti attivi.                                                                                                   |
| [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink)    | Implementata da un oggetto sink per ricevere notifiche sulle modifiche delle proprietà da un oggetto che supporta [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) come interfaccia in uscita.                       |
| [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage)                | Fornisce le funzionalità principali di un oggetto pagina delle proprietà che gestisce una pagina specifica all'interno di una finestra delle proprietà.                                                                                                 |
| [**IPropertyPage2**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage2)              | Estensione di [**IPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypage) per supportare la selezione iniziale di una proprietà in una pagina.                                                                                                 |
| [**IPropertyPageSite**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertypagesite)        | Fornisce le funzionalità principali per un oggetto sito della pagina delle proprietà.                                                                                                                                                  |
| [**IQuickActivate**](/windows/desktop/api/OCIdl/nn-ocidl-iquickactivate)              | Consente a controlli e contenitori di evitare colli di bottiglia delle prestazioni per il caricamento di controlli. Combina l'handshake in fase di caricamento o di inizializzazione tra il controllo e il relativo contenitore in un'unica chiamata. |
| [**ISimpleFrameSite**](/windows/desktop/api/OCIdl/nn-ocidl-isimpleframesite)          | Fornisce semplici controlli frame che fungono da contenitori semplici per altri controlli annidati.                                                                                                                      |
| [**ISpecifyPropertyPage**](/windows/desktop/api/OCIdl/nn-ocidl-ispecifypropertypages) | Indica che un oggetto supporta le pagine delle proprietà.                                                                                                                                                            |



 

 

 
