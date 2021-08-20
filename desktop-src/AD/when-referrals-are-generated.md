---
title: Quando vengono generate le segnalazioni
description: Un riferimento è il modo in cui un server di directory comunica che non contiene i dati necessari per completare una query, ma contiene un riferimento a un server che può contenere i dati necessari.
ms.assetid: 2c11a52a-26e2-4a50-a0a3-5463a0852b27
ms.tgt_platform: multiple
keywords:
- Generazione di riferimenti in Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef1eb05d1495e1f6884d6ce6123356ed29235da421839042909fc05aaa4d9d67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182164"
---
# <a name="when-referrals-are-generated"></a>Quando vengono generate le segnalazioni

Un riferimento è il modo in cui un server di directory comunica che non contiene i dati necessari per completare una query, ma contiene un riferimento a un server che può contenere i dati necessari. Tenere presente che le segnalazioni non vengono generate solo dalle richieste di query.

Le operazioni seguenti possono comportare una o più segnalazioni:

-   Associazione a un server che non contiene l'oggetto specificato dal nome distinto richiesto, ma contiene dati relativi a un server o a un dominio che può contenere tale oggetto. Per ADSI, ciò può verificarsi se l'applicazione chiama [**ADsGetObject**](/windows/desktop/api/adshlp/nf-adshlp-adsgetobject) o [**ADsOpenObject**](/windows/desktop/api/adshlp/nf-adshlp-adsopenobject) per eseguire l'associazione a un oggetto presente in un altro dominio nella foresta (riferimento interno) o un contesto dei nomi completamente separato dalla foresta (riferimento esterno). Per l'API LDAP, ciò può verificarsi quando si eseguono operazioni di aggiunta, modifica, eliminazione o ricerca che specificano un oggetto presente in un altro dominio nella foresta (riferimento interno) o un contesto dei nomi completamente separato dalla foresta (riferimento esterno).

    Se la risoluzione dei nomi non riesce a trovare un oggetto in locale e non sono presenti oggetti **crossRef** per tale parte dello spazio dei nomi, il controller di dominio tenterà di costruire un riferimento esterno basato sui componenti di dominio del nome distinto. Ad esempio, se una ricerca è basata su "CN=a,CN=b,DC=c,DC=d,DC=e", il controller di dominio costruisce un riferimento al server LDAP all'indirizzo DNS "c.d.e".

    Tutti i controller di dominio Windows 2000 (che supportano solo dc= denominazione per i componenti superiori) si riconoscono tra loro e non sono necessari riferimenti incrociati esterni per l'associazione di un client da una foresta a un'altra. Se altri server di directory non Windows 2000, ad esempio un server Netscape, usano la denominazione DC= e ha un RR SRV appropriato registrato in DNS, si otterrà anche il vantaggio dei riferimenti automatici. In caso contrario, è necessario aggiungere manualmente un oggetto **crossRef** esterno.

-   Esecuzione di una ricerca nel sottoalbero in un dominio che contiene domini subordinati nella foresta o domini esterni subordinati, schemi o contenitori di configurazione. Verrà creata una segnalazione al dominio subordinato, al dominio esterno, allo schema o al contenitore di configurazione. Se la ricerca delle segnalazioni è abilitata, la segnalazione sarà trasparente per il chiamante.

 

 