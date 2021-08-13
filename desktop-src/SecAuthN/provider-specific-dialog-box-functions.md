---
description: Le funzioni delle finestre di dialogo specifiche del provider consentono a un provider di visualizzare e gestire informazioni specifiche della rete modificando le finestre di dialogo di sistema o visualizzando finestre di dialogo personalizzate.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Provider-Specific funzioni della finestra di dialogo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4d31a38f09dd0e0806fe21f491d02b5e18fe0abb1e5a181e40f0ab6370280b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118920578"
---
# <a name="provider-specific-dialog-box-functions"></a>Provider-Specific funzioni della finestra di dialogo

Le funzioni delle finestre di dialogo specifiche del provider consentono a un provider di visualizzare e gestire informazioni specifiche della rete modificando le finestre di dialogo di sistema o visualizzando finestre di dialogo personalizzate.

Le funzioni della finestra di dialogo seguenti aggiungono pulsanti alla finestra di **dialogo Proprietà** file manager . Il provider può quindi gestire gli eventi di tali pulsanti per eseguire attività specifiche della rete. Si noti che è previsto un limite al numero di pulsanti che è possibile aggiungere. Per questo problema, i provider devono usare questa funzionalità con moderità. Inoltre, un provider potrebbe non essere in grado di aggiungere un pulsante perché lo spazio disponibile è già stato usato da altri provider. Un provider di rete deve gestire questa situazione.



| Funzione                                           | Descrizione                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | Determina i nomi dei pulsanti aggiunti a una finestra di dialogo delle proprietà per una risorsa specifica.<br/>                                      |
| [**NPPropertyDialog**](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | Chiamato quando un utente fa clic su un pulsante aggiunto usando la [**funzione NPGetPropertyText.**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)<br/>               |
| [**NPSearchDialog**](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | Consente ai provider di rete di implementare funzionalità di ricerca proprie oltre a quella disponibile nella **finestra di dialogo** Connessione .<br/> |
| [**NPFormatNetworkName**](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | Consente ai provider di rete di formattare o modificare in altro modo i nomi di rete prima che siano presentati all'utente.<br/>                 |



 

 

 




