---
description: Un'estensione dello snap-in allegato è il componente di un allegato che Visualizza l'interfaccia utente specifica del servizio.
ms.assetid: 1cafa02f-f240-476c-8ce2-ba088afaf889
title: Estensioni degli snap-in allegati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c55267edcd30f32ad371a4aa276587b4eca06c57
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321001"
---
# <a name="attachment-snap-in-extensions"></a>Estensioni degli snap-in allegati

Un'estensione dello snap-in allegato è il componente di un allegato che Visualizza l'interfaccia utente specifica del servizio. L'estensione dello snap-in è ospitata dagli snap-in Configurazione sicurezza. La comunicazione tra l'estensione degli allegati e il relativo host di snap-in viene gestita dai meccanismi standard di MMC descritti nella documentazione di [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .

Oltre alle interfacce che l'estensione dello snap-in deve supportare per essere un'estensione dello snap-in MMC, un'estensione dello snap-in di allegati deve supportare anche l'interfaccia COM, [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo). Questa interfaccia implementa metodi che indicano se sono presenti dati specifici del servizio che devono essere salvati nel database di sicurezza e, in tal caso, recuperare e salvare questi nuovi dati. Gli snap-in configurazione di sicurezza chiamano i metodi di questa interfaccia regolarmente per aggiornare il database di sicurezza.

Gli snap-in configurazione di sicurezza implementano un'interfaccia, [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata), che fornisce i metodi per recuperare i dati specifici del servizio dal database di sicurezza. Le estensioni degli snap-in allegati possono chiamare metodi di questa interfaccia per recuperare i dati dal database di sicurezza.

Questa architettura è illustrata nella figura seguente.

![estensioni degli snap-in allegati](images/model2.png)

Quando si crea un'estensione dello snap-in allegato, è necessario installarla e registrarla con gli snap-in Configurazione sicurezza. A tale scopo, aggiungere chiavi al registro di sistema, come illustrato in [registrazione di un'estensione dello snap-in allegato](registering-an-attachment-snap-in-extension.md). Quando viene avviato lo snap-in Configurazione sicurezza, viene controllato il registro di sistema e vengono caricate tutte le estensioni di snap-in registrate. Le estensioni vengono visualizzate come nodi nell'area di sicurezza per ogni servizio nello snap-in Configurazione sicurezza.

> [!Note]
> Un'estensione dello snap-in allegato può estendere solo i nodi dei servizi. Il nodo servizi è lo snap-in MMC che contiene gli strumenti per amministrare i servizi installati nel sistema. L'estensione dello snap-in allegati viene dichiarata come subordinata a un tipo di nodo dei servizi specifici e quindi, per ogni occorrenza del tipo di nodo servizi, la console MMC aggiunge automaticamente le estensioni dello snap-in correlate.
> 
> Ogni estensione dello snap-in di allegato è proprietaria di un nodo del riquadro ambito e del riquadro dei risultati correlati in MMC.

 

 

 
