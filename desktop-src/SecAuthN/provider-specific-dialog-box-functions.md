---
description: Le funzioni della finestra di dialogo specifiche del provider consentono a un provider di visualizzare e gestire informazioni specifiche della rete mediante la modifica delle finestre di dialogo di sistema o la visualizzazione di finestre di dialogo personalizzate.
ms.assetid: c9a52867-0a0b-40d8-a09d-2b7bed517e13
title: Funzioni della finestra di dialogo Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 567c4dcb9f1fd6c2e289d678cf09b3d0d66e4207
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316735"
---
# <a name="provider-specific-dialog-box-functions"></a>Funzioni della finestra di dialogo Provider-Specific

Le funzioni della finestra di dialogo specifiche del provider consentono a un provider di visualizzare e gestire informazioni specifiche della rete mediante la modifica delle finestre di dialogo di sistema o la visualizzazione di finestre di dialogo personalizzate.

Le funzioni della finestra di dialogo seguenti aggiungono pulsanti alla finestra di dialogo **Proprietà** di file Manager. Il provider può quindi gestire gli eventi di questi pulsanti per eseguire attività specifiche della rete. Si noti che esiste un limite al numero di pulsanti che è possibile aggiungere. Per questo motivo, i provider devono usare questa funzionalità con moderazione. Inoltre, un provider potrebbe non essere in grado di aggiungere un pulsante perché lo spazio disponibile è già stato utilizzato da altri provider. Questa situazione deve essere gestita da un provider di rete.



| Funzione                                           | Descrizione                                                                                                                             |
|----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext)     | Determina i nomi dei pulsanti aggiunti a una finestra di dialogo delle proprietà per una risorsa specifica.<br/>                                      |
| [**NPPropertyDialog**](/windows/desktop/api/Npapi/nf-npapi-nppropertydialog)       | Chiamato quando un utente fa clic su un pulsante aggiunto tramite la funzione [**NPGetPropertyText**](/windows/desktop/api/Npapi/nf-npapi-npgetpropertytext) .<br/>               |
| [**NPSearchDialog**](/windows/desktop/api/Npapi/nf-npapi-npsearchdialog)           | Consente ai provider di rete di implementare una propria funzionalità di ricerca oltre a quella specificata nella finestra di dialogo di **connessione** .<br/> |
| [**NPFormatNetworkName**](/windows/desktop/api/Npapi/nf-npapi-npformatnetworkname) | Consente ai provider di rete di formattare o modificare in altro modo i nomi di rete prima di essere presentati all'utente.<br/>                 |



 

 

 




