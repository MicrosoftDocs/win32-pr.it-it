---
title: Server-Side configurazione Interfaccia utente
description: Implementare un'interfaccia utente di configurazione per il server implementando l'interfaccia COM IEAPProviderConfig.
ms.assetid: b205c573-6694-42c0-b4f1-1480932dd644
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 92bf6a1f5b5f0e1302e68dd8ca9070771bfbc7714759a384f67782ffdad6e2ae
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120021811"
---
# <a name="server-side-configuration-user-interface"></a>Server-Side configurazione Interfaccia utente

Implementare un'interfaccia utente di configurazione per il server implementando l'interfaccia COM [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Questa interfaccia COM deriva da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e aggiunge tre metodi: [**IEAPProviderConfig::Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize), [**IEAPProviderConfig::ServerInvokeConfigUI**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui)e [**IEAPProviderConfig::Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize).

L'interfaccia utente deve supportare l'amministrazione remota. In altre parole, anche se l'interfaccia utente configurerà il protocollo di autenticazione nel server, l'interfaccia utente stessa potrebbe essere in esecuzione in un computer diverso. Per supportare l'amministrazione remota, separare il codice dell'interfaccia utente dal codice che esegue effettivamente la configurazione. Il codice di configurazione si trova nel server in cui viene eseguito il protocollo di autenticazione.

Usare il Active Template Library (ATL) per [**implementare IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Per altre informazioni, vedere l'interfaccia utente di configurazione lato server di esempio nella directory degli esempi dell'SDK. L'identificatore di classe (CLSID) per l'oggetto dell'interfaccia utente di configurazione deve essere inserito nel Registro di sistema con il nome di valore [RAS \_ EAP \_ VALUENAME \_ CONFIG \_ CLSID](authentication-protocol-registry-values.md). Per altre informazioni, vedere [Valori del Registro di sistema del protocollo di autenticazione](authentication-protocol-registry-values.md).

Quando l'utente fa clic sul pulsante Configura per un protocollo di autenticazione nella finestra di dialogo Proprietà per Routing e RAS, il sistema verifica se nel Registro di sistema è presente un valore CLSID RAS EAP VALUENAME CONFIG per questo protocollo di \_ \_ \_ \_ autenticazione. In tal caso, COM crea un'istanza dell'oggetto dell'interfaccia utente di configurazione. Se il sistema non riesce a trovare IL CLSID CONFIG RAS EAP VALUENAME nel Registro di sistema e il sistema ha accesso ai servizi \_ \_ directory \_ (DS), il sistema tenta di creare un'istanza dell'oggetto dall'archivio \_ classi.

Nel caso in cui l'utente sia connesso a più computer contemporaneamente, viene creata un'istanza di più oggetti dell'interfaccia utente di configurazione.

 

 