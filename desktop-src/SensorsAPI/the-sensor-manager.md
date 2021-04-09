---
description: L'oggetto di gestione dei sensori consente di accedere ai sensori disponibili per l'utilizzo.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: Oggetto di gestione dei sensori
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 715448a62c058c5e6825368003939e5ae2066847
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128739"
---
# <a name="the-sensor-manager-object"></a>Oggetto di gestione dei sensori

L'oggetto di gestione dei sensori consente di accedere ai sensori disponibili per l'utilizzo.

Per usare l'API del sensore, è prima necessario chiamare il metodo COM **CoCreateInstance** per creare un'istanza dell'oggetto di gestione dei sensori e recuperare un puntatore alla relativa interfaccia, denominato [**ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager). Gestione sensori mantiene l'elenco dei sensori disponibili. È possibile usare **ISensorManager** per chiamare metodi che recuperano gruppi di sensori per categoria o per tipo oppure è possibile chiamare un metodo per recuperare un determinato sensore usando il relativo ID univoco. Gestione sensori consente inoltre di effettuare la registrazione per ricevere un evento che informa l'utente quando un nuovo sensore è stato connesso alla piattaforma.

In alcuni casi, il gestore dei sensori fornisce un puntatore a un sensore, ma l'utente non ha abilitato il sensore. Ad esempio, è spesso possibile recuperare i valori per le proprietà dei sensori non privati, ad esempio il produttore o il modello del sensore, prima che l'utente Abilita il sensore. Queste informazioni possono essere utili per decidere se richiedere all'utente l'autorizzazione per l'uso del sensore. È possibile chiamare [**ISensorManager:: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) per richiedere all'utente di abilitare un sensore o una raccolta di sensori particolare.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle autorizzazioni utente](managing-user-permissions.md)
</dt> <dt>

[Richiesta di autorizzazioni utente](requesting-user-permissions.md)
</dt> </dl>

 

 
