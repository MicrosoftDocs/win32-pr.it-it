---
title: Controlli Rich Edit senza finestra
description: Questa sezione contiene informazioni sugli elementi di programmazione usati con controlli Rich Edit senza finestra.
ms.assetid: vs|controls|~\controls\richedit\windowlessricheditcontrols.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0431c5cb513aff003098e3d022fe73c6b6d83e9a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044318"
---
# <a name="windowless-rich-edit-controls"></a>Controlli Rich Edit senza finestra

Questa sezione contiene informazioni sugli elementi di programmazione usati con controlli Rich Edit senza finestra. Il Component Object Model (COM) definisce un set di interfacce per supportare gli oggetti privi di finestra. Gli oggetti senza finestra possono entrare nello stato attivo sul posto senza avere la propria finestra, ma usare invece la finestra del contenitore. Di conseguenza, un oggetto senza finestra utilizza un minor numero di risorse di sistema e offre prestazioni migliori grazie all'attivazione e alla disattivazione più veloci. Gli oggetti senza finestra, inoltre, possono essere non rettangolari e trasparenti.

### <a name="overviews"></a>Cenni preliminari



| Argomento                                                                          | Contenuto                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informazioni sui controlli Rich Edit senza finestra](about-windowless-rich-edit-controls.md) | Un controllo Rich Edit senza finestra, noto anche come oggetto servizi di testo, è un oggetto che fornisce la funzionalità di un [controllo Rich Edit](rich-edit-controls.md) senza fornire la finestra.<br/> |



 

### <a name="functions"></a>Funzioni



| Argomento                                            | Contenuto                                                                                                                                                                                                                                                             |
|--------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) | La funzione [**CreateTextServices**](/windows/desktop/api/Textserv/nf-textserv-createtextservices) crea un'istanza di un oggetto servizi di testo. L'oggetto servizi di testo supporta varie interfacce, tra cui [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) e il modello a oggetti di testo (Tom).<br/> |



 

### <a name="interfaces"></a>Interfacce



| Argomento                                  | Contenuto                                                                                                                |
|----------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost)         | L'interfaccia [**ITextHost**](/windows/desktop/api/Textserv/nl-textserv-itexthost) viene utilizzata da un oggetto servizi di testo per ottenere i servizi host di testo.<br/> |
| [**ITextServices**](/windows/desktop/api/Textserv/nl-textserv-itextservices) | Estende il TOM per fornire funzionalità aggiuntive per l'operazione senza finestra.<br/>                                     |



 

 

 





