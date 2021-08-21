---
description: L'estensione dello snap-in deve visualizzare le informazioni di analisi e configurazione correnti per gli utenti.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Visualizzazione delle informazioni di configurazione e analisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d33971f413058279aa840db4a61e529eb25ee7f317145a66bcb4474142a35c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118894784"
---
# <a name="displaying-configuration-and-analysis-information"></a>Visualizzazione delle informazioni di configurazione e analisi

L'estensione dello snap-in deve visualizzare le informazioni di analisi e configurazione correnti per gli utenti.

Per visualizzare le informazioni, il nodo dell'estensione dello snap-in degli allegati deve estendere gli snap-in Di configurazione della sicurezza usando il nodo Servizi. Il nodo Servizi è lo snap-in MMC che amministra i servizi installati nel sistema.

I tipi di nodo che è possibile estendere sono i seguenti:

-   Configuration Services NodeType={24a7f717-1f0c-11d1-affb-00c04fb984f9}
-   Inspection Services NodeType={678050c7-1ff8-11d1-affb-00c04fb984f9}

Quando il nodo Servizi viene espanso, MMC invia una notifica a tutte le estensioni snap-in registrate. Ogni snap-in degli allegati deve essere inserito nel nodo Servizi ed eseguire le attività seguenti:

-   Chiamare **QueryInterface** per ottenere un puntatore [**all'interfaccia ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) esposta dagli snap-in Di configurazione della sicurezza.
-   Chiamare [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) per informare gli snap-in di configurazione della sicurezza che l'estensione dello snap-in è caricata e per stabilire un contesto per le comunicazioni.
-   Chiamare [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) per recuperare le informazioni di configurazione dal database. Questo passaggio può essere eseguito quando l'estensione dello snap-in viene inizializzata o quando l'utente apre il relativo nodo.

Per altre informazioni, vedere [Aggiunta di un nodo di estensione dello snap-in allegati](adding-an-attachment-snap-in-extension-node.md).

 

 



