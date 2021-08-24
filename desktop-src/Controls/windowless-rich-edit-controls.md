---
title: Controlli Rich Edit senza finestra
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli Rich Edit senza finestra.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54d03cbc4c694ce8e10a5b877298f148cd9ac47bd24c364aa3cde7fc19bc994e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119655791"
---
# <a name="windowless-rich-edit-controls"></a>Controlli Rich Edit senza finestra

Questa sezione contiene informazioni sugli elementi di programmazione usati con i controlli Rich Edit senza finestra. Il Component Object Model (COM) definisce un set di interfacce per supportare gli oggetti senza finestra. Gli oggetti senza finestra possono entrare nello stato attivo sul posto senza avere una finestra propria, ma usare la finestra del contenitore. Di conseguenza, un oggetto senza finestra usa meno risorse di sistema e offre prestazioni migliori grazie a un'attivazione e una disattivazione più veloci. Inoltre, gli oggetti senza finestra possono essere non rettangolari e trasparenti.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                                          | Contenuto                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli Rich Edit senza finestra](about-windowless-rich-edit-controls.md) | Un controllo Rich Edit senza finestra, noto anche come oggetto di servizi di testo, è un oggetto che fornisce la funzionalità di un controllo [Rich Edit](rich-edit-controls.md) senza fornire la finestra.<br/> |



 

### <a name="functions"></a>Funzioni



| Argomento                                            | Contenuto                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | La [**funzione CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) crea un'istanza di un oggetto di servizi di testo. L'oggetto servizi di testo supporta un'ampia gamma di interfacce, tra cui [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e il modello a oggetti di testo (TOM, Text Object Model).<br/> |



 

### <a name="interfaces"></a>Interfacce



| Argomento                                  | Contenuto                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | [**L'interfaccia ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) viene usata da un oggetto servizi di testo per ottenere i servizi host di testo.<br/> |
| [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) | Estende TOM per fornire funzionalità aggiuntive per il funzionamento senza finestra.<br/>                                     |



 

 

 





