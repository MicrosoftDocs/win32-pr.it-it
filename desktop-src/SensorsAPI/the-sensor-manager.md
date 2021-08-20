---
description: L'oggetto di gestione dei sensori fornisce l'accesso ai sensori disponibili per l'uso.
ms.assetid: dd39d533-9983-41b4-a9a3-d94dcadebaac
title: Oggetto Sensor Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9ce54dd72b642e599d8b7b26b8c94d1531767ec31b5ccd81a47b88746853a10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117968414"
---
# <a name="the-sensor-manager-object"></a>Oggetto Sensor Manager

L'oggetto di gestione dei sensori fornisce l'accesso ai sensori disponibili per l'uso.

Per usare l'API Sensor, è necessario chiamare prima il metodo **COM CoCreateInstance** per creare un'istanza dell'oggetto gestore sensori e recuperare un puntatore alla relativa interfaccia, [**denominato ISensorManager**](/windows/desktop/api/sensorsapi/nn-sensorsapi-isensormanager). Il gestore dei sensori gestisce l'elenco dei sensori disponibili. È possibile usare **ISensorManager** per chiamare metodi che recuperano gruppi di sensori in base alla categoria o al tipo oppure è possibile chiamare un metodo per recuperare un determinato sensore usando il relativo ID univoco. Il gestore dei sensori consente anche di registrarsi per ricevere un evento che notifica quando un nuovo sensore è stato connesso alla piattaforma.

In alcuni casi, il gestore dei sensori fornisce un puntatore a un sensore, ma l'utente non ha abilitato il sensore. Ad esempio, è spesso possibile recuperare i valori per le proprietà del sensore non privato, ad esempio il produttore o il modello del sensore, prima che l'utente aseni il sensore. Queste informazioni consentono di decidere se chiedere all'utente l'autorizzazione per usare il sensore. È possibile chiamare [**ISensorManager::RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) per richiedere all'utente di abilitare un sensore specifico o una raccolta di sensori.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione delle autorizzazioni utente](managing-user-permissions.md)
</dt> <dt>

[Richiesta di autorizzazioni utente](requesting-user-permissions.md)
</dt> </dl>

 

 
