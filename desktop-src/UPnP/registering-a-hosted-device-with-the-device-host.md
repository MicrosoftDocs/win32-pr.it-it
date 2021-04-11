---
title: Registrazione di un dispositivo ospitato con l'host del dispositivo
description: La registrazione di un dispositivo ospitato significa fornire all'host del dispositivo la descrizione del dispositivo e il relativo oggetto controllo dispositivo.
ms.assetid: 1d85b412-9b1b-415d-8664-8d96a6644793
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4a607af4f6ada359a9ee32e98e416d8271fd502
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104221352"
---
# <a name="registering-a-hosted-device-with-the-device-host"></a>Registrazione di un dispositivo ospitato con l'host del dispositivo

La registrazione di un dispositivo ospitato significa fornire all'host del dispositivo la descrizione del dispositivo e il relativo oggetto controllo dispositivo. L'host del dispositivo crea quindi una descrizione del dispositivo UPnP completa, la pubblica e annuncia il dispositivo sulla rete usando il protocollo di individuazione UPnP. Una volta pubblicato, un dispositivo è disponibile per i punti di controllo.

I dispositivi vengono registrati in due modi:

-   Un'applicazione crea un'istanza dell'oggetto controllo del dispositivo e passa un puntatore all'host del dispositivo.
-   L'applicazione passa il ProgID per un oggetto controllo dispositivo registrato all'host del dispositivo. L'host del dispositivo ne crea un'istanza quando l'host del dispositivo riceve la prima richiesta per il dispositivo.

Indipendentemente dal metodo usato, l'host del dispositivo pubblica e annuncia il dispositivo non appena viene registrato. La differenza tra i due approcci è quella di eseguire il caricamento del codice del dispositivo. Quando l'applicazione passa un puntatore all'oggetto controllo del dispositivo, il codice del dispositivo viene caricato e in esecuzione al momento della registrazione. Quando l'applicazione passa un ProgID, il codice del dispositivo viene caricato solo quando viene richiamata un'azione, viene eseguita una query su una proprietà o viene ricevuta una richiesta di sottoscrizione dell'evento. Il secondo approccio è leggermente più efficiente. Tuttavia, non è adatto per i dispositivi che devono essere in esecuzione prima che vengano ricevute richieste di controllo o di sottoscrizione di eventi, perché l'uso di questo approccio, gli oggetti di controllo del dispositivo vengono creati solo quando sono necessari. Il secondo metodo può inoltre creare problemi di prestazioni quando riceve la prima richiesta per un tipo di dispositivo.

Per assicurarsi che un dispositivo venga annunciato automaticamente dall'host del dispositivo sulla rete all'avvio del computer, richiamare [**IUPnPRegistrar:: RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice). **RegisterDevice** garantisce che il codice del dispositivo venga caricato solo quando viene ricevuta una richiesta di sottoscrizione a un controllo o a un evento.

Se i dispositivi sono temporanei o con bridging, richiamare [**IUPnPRegistrar:: RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)e il dispositivo non viene nuovamente annunciato quando il computer viene riavviato.

## <a name="discovery-announcement-lifetime"></a>Durata degli annunci di individuazione

Ogni dispositivo registrato con l'host del dispositivo è associato a una durata, specificata dal dispositivo durante la registrazione. La durata del dispositivo è il periodo di tempo per cui gli annunci di individuazione del dispositivo sono validi. La durata viene passata al punto di controllo come intestazione nell'annuncio iniziale di individuazione. L'host del dispositivo aggiorna automaticamente l'annuncio prima della data di scadenza. I valori della durata dell'annuncio di individuazione devono essere di 15 minuti o più (il valore predefinito è 30 minuti).

## <a name="device-identifiers-created-at-registration"></a>Identificatori di dispositivo creati alla registrazione

Quando si crea un modello di descrizione del dispositivo, lo sviluppatore del dispositivo deve fornire il percorso della risorsa per la descrizione del servizio e le icone associate. Il percorso della risorsa è determinato dall'applicazione del dispositivo.

Poiché lo stesso dispositivo può essere registrato più volte nello stesso computer, il UDN specificato nel modello di descrizione del dispositivo non è sufficiente per identificare in modo univoco un dispositivo. Pertanto, quando un dispositivo viene registrato, l'host del dispositivo crea un identificatore del dispositivo. Questo identificatore di dispositivo, in associazione a UDN nel modello di descrizione del dispositivo, può essere usato per identificare in modo univoco un dispositivo.

Questo identificatore viene usato anche quando viene temporaneamente annullata la registrazione del dispositivo e quindi la nuova registrazione. Quando viene annullata la registrazione temporanea di un dispositivo, l'host del dispositivo non elimina il UDN. I motivi per cui non si eliminano i UDN includono:

-   È in corso l'aggiornamento del dispositivo.
-   Si stanno modificando le proprietà del dispositivo.
-   Un servizio è temporaneamente non disponibile.
-   Si sta aggiungendo un nuovo servizio a un dispositivo.
-   Si sta aggiornando la DLL.
-   Il dispositivo è in modalità standby.

Per ulteriori informazioni sulla registrazione, vedere le sezioni seguenti:

-   [Come registrare un dispositivo con l'host del dispositivo](how-to-register-a-device-with-the-device-host.md)
-   [Annullamento della registrazione di un dispositivo](unregistering-a-device.md)
-   [**IUPnPRegistrar::UnregisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-unregisterdevice)
-   [**IUPnPReregistrar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpreregistrar)

 

 




