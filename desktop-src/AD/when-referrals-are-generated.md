---
title: Quando vengono generati i riferimenti
description: Un riferimento è il modo in cui un server di directory comunica che non contiene i dati necessari per completare una query, ma dispone di un riferimento a un server che può contenere i dati necessari.
ms.assetid: 2c11a52a-26e2-4a50-a0a3-5463a0852b27
ms.tgt_platform: multiple
keywords:
- Active Directory di generazione del riferimento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06e47c1e172f3eaed34dad452aa46847980cd66f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/17/2020
ms.locfileid: "103872242"
---
# <a name="when-referrals-are-generated"></a>Quando vengono generati i riferimenti

Un riferimento è il modo in cui un server di directory comunica che non contiene i dati necessari per completare una query, ma dispone di un riferimento a un server che può contenere i dati necessari. Tenere presente che i riferimenti non sono semplicemente generati dalle richieste di query.

Le operazioni seguenti possono generare uno o più riferimenti:

-   Associazione a un server che non contiene l'oggetto specificato dal nome distinto richiesto, ma che contiene dati relativi a un server o a un dominio che può contenere tale oggetto. Per ADSI, questo problema può verificarsi se l'applicazione chiama [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) o [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) per eseguire l'associazione a un oggetto esistente in un altro dominio nella foresta (riferimento interno) o un contesto di denominazione completamente separato dalla foresta (riferimento esterno). Per l'API LDAP, questo problema può verificarsi quando si eseguono operazioni di aggiunta, modifica, eliminazione o ricerca che specificano un oggetto presente in un altro dominio nella foresta (riferimento interno) o un contesto di denominazione completamente separato dalla foresta (riferimento esterno).

    Se la risoluzione dei nomi non riesce a trovare un oggetto localmente e non sono presenti oggetti **crossRef** per tale parte dello spazio dei nomi, il controller di dominio tenterà di creare un riferimento esterno in base ai componenti del dominio del nome distinto. Se, ad esempio, una ricerca è basata su "CN = a, CN = b, DC = c, DC = d, DC = e", il controller di dominio creerà un riferimento al server LDAP nell'indirizzo DNS "c. d. e".

    Tutti i controller di dominio Windows 2000 (che supportano solo DC = Naming per i componenti superiori) si riconoscono reciprocamente e non sono necessari riferimenti incrociati esterni per l'associazione di un client da una foresta a un'altra. Se altri server di directory non Windows 2000, ad esempio un server Netscape, usano DC = Naming e hanno un record SRV appropriato registrato in DNS, otterrà anche il vantaggio dei riferimenti automatici. In caso contrario, è necessario aggiungere manualmente un oggetto **crossRef** esterno.

-   Esecuzione di una ricerca nel sottoalbero in un dominio che contiene domini subordinati nella foresta o in domini esterni, schemi o contenitori di configurazione subordinati. Verrà creato un riferimento al dominio subordinato, al dominio esterno, allo schema o al contenitore di configurazione. Se il riferimento è abilitato, il riferimento sarà trasparente per il chiamante.

 

 