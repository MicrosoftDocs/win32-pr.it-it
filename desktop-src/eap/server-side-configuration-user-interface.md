---
title: Interfaccia utente di configurazione di Server-Side
description: Implementare un'interfaccia utente di configurazione per il server implementando l'interfaccia COM, IEAPProviderConfig.
ms.assetid: b205c573-6694-42c0-b4f1-1480932dd644
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0904c90fea2bef3ccc00c00135be09a711d8454
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337254"
---
# <a name="server-side-configuration-user-interface"></a>Interfaccia utente di configurazione di Server-Side

Implementare un'interfaccia utente di configurazione per il server implementando l'interfaccia COM, [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Questa interfaccia COM deriva da [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) e aggiunge tre metodi: [**IEAPProviderConfig:: Initialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-initialize), [**IEAPProviderConfig:: ServerInvokeConfigUI**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-serverinvokeconfigui)e [**IEAPProviderConfig:: Uninitialize**](/previous-versions/windows/desktop/api/Rrascfg/nf-rrascfg-ieapproviderconfig-uninitialize).

L'interfaccia utente deve supportare l'amministrazione remota. In altre parole, anche se l'interfaccia utente configurerà il protocollo di autenticazione nel server, l'interfaccia utente potrebbe essere in esecuzione in un computer diverso. Per supportare l'amministrazione remota, separare il codice dell'interfaccia utente dal codice che esegue effettivamente la configurazione. Il codice di configurazione risiede nel server in cui viene eseguito il protocollo di autenticazione.

Usare il Active Template Library (ATL) per implementare [**IEAPProviderConfig**](/previous-versions/windows/desktop/api/Rrascfg/nn-rrascfg-ieapproviderconfig). Per ulteriori informazioni, vedere l'interfaccia utente di esempio della configurazione lato server nella directory degli esempi di SDK. L'identificatore di classe (CLSID) per l'oggetto dell'interfaccia utente di configurazione deve essere inserito nel registro di sistema con il nome del valore [RAS \_ EAP \_ valueName \_ config \_ CLSID](authentication-protocol-registry-values.md). Per ulteriori informazioni, vedere [valori del registro di sistema del protocollo di autenticazione](authentication-protocol-registry-values.md).

Quando l'utente fa clic sul pulsante Configura per un protocollo di autenticazione nella finestra di dialogo proprietà per routing e RAS, il sistema verifica se \_ nel registro di sistema è \_ presente un valore CLSID della configurazione di Ras EAP valueName \_ \_ per questo protocollo di autenticazione. In tal caso, COM crea un'istanza dell'oggetto dell'interfaccia utente di configurazione. Se il sistema non è in grado di trovare RAS \_ EAP \_ valueName \_ config \_ CLSID nel registro di sistema e il sistema ha accesso ai servizi directory (DS), il sistema tenta di creare un'istanza dell'oggetto dall'archivio delle classi.

Nel caso in cui l'utente sia connesso a più computer contemporaneamente, viene creata un'istanza di più oggetti dell'interfaccia utente di configurazione.

 

 