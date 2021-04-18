---
description: L'estensione dello snap-in deve visualizzare agli utenti la configurazione e le informazioni di analisi correnti.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Visualizzazione delle informazioni di configurazione e analisi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315353"
---
# <a name="displaying-configuration-and-analysis-information"></a>Visualizzazione delle informazioni di configurazione e analisi

L'estensione dello snap-in deve visualizzare agli utenti la configurazione e le informazioni di analisi correnti.

Per visualizzare le informazioni, è necessario che il nodo dell'estensione dello snap-in allegati estenda gli snap-in Configurazione sicurezza utilizzando il nodo servizi. Il nodo servizi è lo snap-in MMC che amministra i servizi installati nel sistema.

I tipi di nodo che possono essere estesi sono i seguenti:

-   Servizi di configurazione NodeType = {24a7f717-1f0c-11D1-affb-00C04FB984F9}
-   Inspection Services NodeType = {678050c7-1ff8-11D1-affb-00C04FB984F9}

Quando il nodo servizi è espanso, MMC notifica tutte le estensioni dello snap-in registrate. Ogni snap-in allegati deve essere inserito nel nodo servizi ed eseguire le attività seguenti:

-   Chiamare **QueryInterface** per ottenere un puntatore all'interfaccia [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) esposta dagli snap-in configurazione di sicurezza.
-   Chiamare [**ISceSvcAttachmentData:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) per informare gli snap-in di configurazione della sicurezza che l'estensione dello snap-in è stata caricata e per stabilire un contesto per le comunicazioni.
-   Chiamare [**ISceSvcAttachmentData:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) per recuperare le informazioni di configurazione dal database. Questo passaggio può essere eseguito quando l'estensione dello snap-in si Inizializza o quando l'utente apre il nodo.

Per ulteriori informazioni, vedere [aggiunta di un nodo di estensione dello snap-in allegato](adding-an-attachment-snap-in-extension-node.md).

 

 



