---
description: 'Le applicazioni possono eseguire la registrazione per ricevere notifiche degli eventi del dispositivo hardware di acquisizione immagini Windows (WIA) chiamando uno dei seguenti metodi di interfaccia IWiaDevMgr o IWiaDevMgr2: IWiaDevMgr:: RegisterEventCallbackCLSID o IWiaDevMgr2:: RegisterEventCallbackCLSIDIWiaDevMgr:: RegisterEventCallbackInterface o IWiaDevMgr2:: RegisterEventCallbackInterfaceIWiaDevMgr:: RegisterEventCallbackProgram o IWiaDevMgr2:: RegisterEventCallbackProgram'
ms.assetid: 0c142083-835f-4bbd-ab32-eb6130f99c59
title: Registrazione degli eventi WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa9fc36540a64211428579bc13b84902490ea103
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966716"
---
# <a name="registering-wia-events"></a>Registrazione degli eventi WIA

Le applicazioni possono eseguire la registrazione per ricevere notifiche relative agli eventi del dispositivo hardware di acquisizione immagini Windows (WIA) chiamando uno dei seguenti metodi di interfaccia [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) :

-   [**IWiaDevMgr:: RegisterEventCallbackCLSID**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackclsid) o [ **IWiaDevMgr2:: RegisterEventCallbackCLSID**](-wia-iwiadevmgr2-registereventcallbackclsid.md)
-   [**IWiaDevMgr:: RegisterEventCallbackInterface**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackinterface) o [ **IWiaDevMgr2:: RegisterEventCallbackInterface**](-wia-iwiadevmgr2-registereventcallbackinterface.md)
-   [**IWiaDevMgr:: RegisterEventCallbackProgram**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadevmgr-registereventcallbackprogram) o [ **IWiaDevMgr2:: RegisterEventCallbackProgram**](-wia-iwiadevmgr2-registereventcallbackprogram.md)

Tutti questi metodi accettano parametri che specificano l'evento e il dispositivo hardware per cui l'applicazione deve ricevere una notifica. Le applicazioni si registrano per ricevere un evento per tutti i dispositivi WIA passando un valore **null** per il parametro che specifica il dispositivo hardware.

Il metodo **RegisterEventCallbackInterface** registra un'applicazione per ricevere un evento del dispositivo hardware WIA se l'applicazione è in esecuzione nel momento in cui si verifica l'evento. Quando si verifica l'evento per cui è registrata l'applicazione, WIA chiama il metodo [**IWiaEventCallback:: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) dell'oggetto fornito dall'applicazione per trasmettere le informazioni sull'evento.

Il metodo **RegisterEventCallbackCLSID** registra un'applicazione che è un componente Component Object Model registrato (com) per ricevere un evento del dispositivo hardware WIA anche se l'applicazione non è in esecuzione. Oltre ai parametri indicati in precedenza, questo metodo accetta un parametro, *pClsID*, che specifica l'ID della classe dell'applicazione. Quando si verifica l'evento specificato, il sistema WIA utilizza la funzione [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) e l'ID di classe specificato da *pClsID* per creare una nuova istanza dell'applicazione e chiama il metodo [**IWiaEventCallback:: ImageEventCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaeventcallback-imageeventcallback) dell'applicazione per trasmettere le informazioni sull'evento.

Il metodo **RegisterEventCallbackProgram** registra un'applicazione per ricevere un evento del dispositivo hardware WIA anche se l'applicazione non è in esecuzione quando si verifica l'evento. L'applicazione non deve essere un componente COM registrato. WIA avvia l'applicazione con un'istruzione della riga di comando. **RegisterEventCallbackProgram** accetta un parametro, *bstrCommandline*, che specifica il percorso completo e il nome file dell'applicazione eseguibile. **RegisterEventCallbackProgram** esiste per compatibilità con le applicazioni che non sono state scritte per WIA e che devono essere evitate. In alternativa, utilizzare **RegisterEventCallbackInterface** o **RegisterEventCallbackCLSID** .

Per determinare quali gestori sono registrati per gli eventi in un dispositivo WIA specifico, un'applicazione chiama un metodo [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) o [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) di un elemento radice. Questo metodo crea un oggetto di enumerazione per le informazioni di registrazione. L'applicazione può quindi usare l'interfaccia [**IEnumWIA \_ dev \_ Caps**](/windows/desktop/api/wia_xp/nn-wia_xp-ienumwia_dev_caps) dell'oggetto per enumerare le informazioni sui gestori registrati per ricevere gli eventi per il dispositivo.

Se si verifica un evento per il quale un'applicazione in esecuzione viene registrata tramite **RegisterEventCallbackInterface** e **RegisterEventCallbackCLSID** o **RegisterEventCallbackProgram**, WIA invia una notifica all'applicazione in esecuzione e non tenta di avviare una nuova istanza dell'applicazione perché la registrazione degli eventi tramite **RegisterEventCallbackInterface** ha la precedenza su **RegisterEventCallbackCLSID** e **RegisterEventCallbackProgram**.

> [!Note]  
> In un'applicazione multithread, non esiste alcuna garanzia che il thread in cui verrà restituito il callback di notifica degli eventi sia lo stesso thread che ha registrato il callback.

 

 

 
