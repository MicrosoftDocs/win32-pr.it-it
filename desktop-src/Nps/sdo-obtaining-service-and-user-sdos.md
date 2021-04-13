---
title: Recupero del servizio e dell'utente SDOs
description: Per ottenere SDOs per NPS (IAS) o un particolare utente, chiamare i metodi ISdoMachine GetServiceSDO o ISdoMachine GetUserSDO.
ms.assetid: 23e23fb3-0102-4c36-b30f-18604131ee32
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c7562c3b7c6aa1150ba3ce6581441064eb386f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104338246"
---
# <a name="obtaining-service-and-user-sdos"></a>Recupero del servizio e dell'utente SDOs

> [!Note]  
> Il servizio di autenticazione Internet (IAS) è stato rinominato server dei criteri di rete (NPS) a partire da Windows Server 2008.

 

Per ottenere SDOs per NPS (IAS) o un utente specifico, chiamare i metodi [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo) . Questi metodi restituiscono puntatori alle interfacce [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) per questi oggetti. Per l'utente SDO, usare il metodo [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per ottenere un'interfaccia [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) per l'oggetto. Per il servizio SDO, usare **IUnknown:: QueryInterface** per ottenere un'interfaccia [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) o un'interfaccia [**ISdoServiceControl**](/windows/desktop/api/sdoias/nn-sdoias-isdoservicecontrol) .

Prima di chiamare [**ISdoMachine:: GetServiceSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getservicesdo) o [**ISdoMachine:: GetUserSDO**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-getusersdo), chiamare [**ISdoMachine:: Connetti**](/windows/desktop/api/sdoias/nf-sdoias-isdomachine-attach) per associare l'oggetto computer al computer locale.

Vedere [recupero di un servizio SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo) e [recupero di un SDO utente per il](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) codice di esempio che illustra come ottenere questi SDOs.

 

 