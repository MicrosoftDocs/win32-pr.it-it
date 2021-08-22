---
title: Registrazione di un dispositivo ospitato con l'host del dispositivo
description: Registrare un dispositivo ospitato significa fornire all'host del dispositivo la descrizione del dispositivo e il relativo oggetto di controllo del dispositivo.
ms.assetid: 1d85b412-9b1b-415d-8664-8d96a6644793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486d01364b684e2aa6792b8a6c0b91ccc87a26670057c67192fe587ac049c388
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999561"
---
# <a name="registering-a-hosted-device-with-the-device-host"></a>Registrazione di un dispositivo ospitato con l'host del dispositivo

Registrare un dispositivo ospitato significa fornire all'host del dispositivo la descrizione del dispositivo e il relativo oggetto di controllo del dispositivo. L'host del dispositivo costruisce quindi una descrizione completa del dispositivo UPnP, lo pubblica e annuncia il dispositivo in rete usando il protocollo di individuazione UPnP. Dopo la pubblicazione, un dispositivo è disponibile per i punti di controllo.

I dispositivi vengono registrati in due modi:

-   Un'applicazione crea un'istanza dell'oggetto controllo dispositivo e passa un puntatore all'host del dispositivo.
-   L'applicazione passa il ProgID per un oggetto controllo dispositivo registrato all'host del dispositivo. L'host del dispositivo crea un'istanza quando l'host del dispositivo riceve la prima richiesta per il dispositivo.

Indipendentemente dal metodo usato, l'host del dispositivo pubblica e annuncia il dispositivo non appena viene registrato. La differenza tra i due approcci ha a che fare con quando viene caricato il codice del dispositivo. Quando l'applicazione passa un puntatore all'oggetto controllo dispositivo, il codice del dispositivo viene caricato ed eseguito al momento della registrazione. Quando l'applicazione passa un ProgID, il codice del dispositivo viene caricato solo quando viene richiamata un'azione, viene eseguita una query su una proprietà o arriva una richiesta di sottoscrizione di eventi. Il secondo approccio è leggermente più efficiente. Tuttavia, non è adatto per i dispositivi che devono essere in esecuzione prima dell'arrivo di qualsiasi richiesta di controllo o sottoscrizione di eventi, perché con questo approccio, gli oggetti di controllo del dispositivo vengono creati solo quando sono necessari. Questo secondo metodo può anche creare problemi di prestazioni quando riceve la prima richiesta per un tipo di dispositivo.

Per assicurarsi che un dispositivo sia annunciato automaticamente dall'host del dispositivo in rete all'avvio del computer, richiamare [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice). **RegisterDevice** garantisce che il codice del dispositivo sia caricato solo quando viene ricevuta una richiesta di sottoscrizione di controllo o di evento.

Se i dispositivi sono temporanei o con bridge, richiamare [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)e il dispositivo non viene annunciato automaticamente al riavvio del computer.

## <a name="discovery-announcement-lifetime"></a>Durata dell'annuncio di individuazione

Ogni dispositivo registrato con l'host del dispositivo è associato a una durata, specificata dal dispositivo al momento della registrazione. La durata del dispositivo è il periodo di tempo per cui gli annunci di individuazione del dispositivo sono validi. La durata viene passata al punto di controllo come intestazione nell'annuncio di individuazione iniziale. L'host del dispositivo aggiorna automaticamente l'annuncio prima dell'ora di scadenza. I valori della durata dell'annuncio di individuazione devono essere di 15 minuti o più (il valore predefinito è 30 minuti).

## <a name="device-identifiers-created-at-registration"></a>Identificatori di dispositivo creati alla registrazione

Quando si crea un modello di descrizione del dispositivo, lo sviluppatore del dispositivo deve specificare il percorso della risorsa per la descrizione del servizio e le icone associate. Il percorso della risorsa è determinato dall'applicazione del dispositivo.

Poiché lo stesso dispositivo può essere registrato più volte nello stesso computer, il nome definito dall'utente specificato nel modello di descrizione del dispositivo non è sufficiente per identificare in modo univoco un dispositivo. Pertanto, quando un dispositivo viene registrato, l'host del dispositivo crea un identificatore di dispositivo. Questo identificatore di dispositivo, in associazione con il nome definito dall'utente nel modello di descrizione del dispositivo, può essere usato per identificare in modo univoco un dispositivo.

Questo identificatore viene usato anche quando il dispositivo viene temporaneamente annullato e quindi nuovamente registrato. Quando un dispositivo viene annullato temporaneamente, l'host del dispositivo non elimina il nome definito dall'utente. I motivi per cui non si elimina il nome definito dall'utente includono:

-   È in corso l'aggiornamento del dispositivo.
-   Si stanno modificando le proprietà del dispositivo.
-   Un servizio è temporaneamente non disponibile.
-   Si sta aggiungendo un nuovo servizio a un dispositivo.
-   Si sta aggiornando la DLL.
-   Il dispositivo è in modalità stand-by.

Per altre informazioni sulla registrazione, vedere le sezioni seguenti:

-   [Come registrare un dispositivo con l'host del dispositivo](how-to-register-a-device-with-the-device-host.md)
-   [Annullamento della registrazione di un dispositivo](unregistering-a-device.md)
-   [**IUPnPRegistrar::UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice)
-   [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)

 

 




