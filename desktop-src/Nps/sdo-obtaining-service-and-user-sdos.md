---
title: Recupero di SDO per servizi e utenti
description: Per ottenere SDO per NPS (IAS) o un utente specifico, chiamare i metodi ISdoMachine GetServiceSDO o ISdoMachine GetUserSDO.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aebef1e695236bd1449ab886cb998a67f09c2cafc8ded446b0b7e1ad89b01181
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120128591"
---
# <a name="obtaining-service-and-user-sdos"></a>Recupero di SDO per servizi e utenti

> [!Note]  
> Il servizio Autenticazione Internet (IAS) è stato rinominato Server dei criteri di rete a partire da Windows Server 2008.

 

Per ottenere gli SDO per NPS (IAS) o un utente specifico, chiamare i [**metodi ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine::GetUserSDO.**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) Questi metodi restituiscono puntatori [**alle interfacce IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per questi oggetti. Per L'utente SDO, usare il [**metodo IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere [**un'interfaccia ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) per l'oggetto. Per il servizio SDO, usare **IUnknown::QueryInterface** per ottenere [**un'interfaccia ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) o [**ISdoServiceControl.**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol)

Prima di chiamare [**ISdoMachine::GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine::GetUserSDO,**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo)chiamare [**ISdoMachine::Attach**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) per associare l'oggetto computer al computer locale.

Vedere [Recupero di un SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) del servizio e Recupero di un [SDO](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) utente per il codice di esempio che illustra come ottenere questi SDO.

 

 