---
description: L'API Sensor fornisce un metodo che è possibile usare per richiedere all'utente le autorizzazioni per usare un sensore o una raccolta di sensori.
ms.assetid: c755edcf-18c1-43d5-9dfe-c073e1f96b5f
title: Gestione delle autorizzazioni utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f02fac57959b493683d0fe0a007602e5a7af3f78dc959d0e7eca2811595c23dc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119576251"
---
# <a name="managing-user-permissions"></a>Gestione delle autorizzazioni utente

L'API Sensor fornisce un metodo che è possibile usare per richiedere all'utente le autorizzazioni per usare un sensore o una raccolta di sensori.

Poiché i sensori possono rivelare informazioni riservate, Windows che gli utenti abilitino i sensori prima che il programma possa accedere ai dati.

È possibile richiedere l'autorizzazione quando si vogliono usare sensori per i quali [**l'oggetto SensorState corrente**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) è SENSOR \_ STATE ACCESS \_ \_ DENIED.

Per richiedere le autorizzazioni, chiamare [**il metodo ISensorManager::RequestPermissions.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) Quando si chiama questo metodo, Windows  la finestra di dialogo Abilita sensori per richiedere all'utente di abilitare i sensori richiesti. Questa finestra di dialogo fornisce all'utente i nomi dei sensori richiesti. L'utente può scegliere una delle opzioni seguenti:

-   **Abilitare questi sensori**.
-   **Non abilitare questi sensori**.
-   **Aprire Pannello di controllo altre opzioni**.

Se un utente sceglie Non abilitare questi **sensori,** Windows non  mostrerà di nuovo la finestra di dialogo Abilita sensori per questi sensori specifici, anche se il programma chiama [**RequestPermissions.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) Se l'utente sceglie un'altra opzione, Windows la finestra di dialogo verrà visualizzata quando richiesto. Se la chiamata a **RequestPermissions** contiene alcuni sensori che l'utente ha scelto in precedenza di mantenere disabilitati, l'API Sensor rimuoverà questi sensori dall'elenco dei sensori visualizzati dall'utente.

### <a name="modal-or-modeless-behavior"></a>Comportamento modale o non modale

Il [**metodo RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) accetta un argomento  **booleano** che determina se la finestra di dialogo Abilita sensori viene visualizzata come finestra modale o non modale. Questa impostazione influisce anche sul fatto che il comportamento del codice restituito della finestra di dialogo sia sincrono o asincrono.

Quando è modale, la finestra di dialogo ha lo stato attivo esclusivo tra le finestre dell'applicazione fino a quando l'utente non sceglie un'opzione e il codice **restituito HRESULT** dalla chiamata a [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) indica la scelta dell'utente. Quando non è modali, la finestra di dialogo non ha lo stato attivo esclusivo e la chiamata a **RequestPermissions viene** restituita immediatamente. In questo caso, il codice restituito indica se il metodo ha avuto esito positivo, ma non può essere usato per verificare la scelta dell'utente. È quindi possibile determinare quali sensori sono stati abilitati gestendo l'evento [**OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) e controllando la presenza di SENSOR STATE READY in ogni \_ \_ sensore.

Per altre informazioni sui codici restituiti, vedere la [**pagina di riferimento requestPermissions.**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions)

### <a name="best-practice-avoid-multiple-modeless-calls-to-requestpermissions"></a>Procedura consigliata: evitare più chiamate non modali a RequestPermissions

Le chiamate non modali ripetute a  [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) visualizzano più istanze della finestra di dialogo Abilita questi sensori e possono potenzialmente inondare lo schermo con finestre di dialogo, con un'esperienza utente non ottimale. Se si pensa che dopo la prima chiamata a **RequestPermissions** potrebbero essere installati altri sensori di posizione, che richiedono un'altra chiamata a **RequestPermissions,** è necessario chiamare **RequestPermissions** come modale o attendere che tutti i sensori di posizione siano installati per effettuare una chiamata non modale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Privacy e sicurezza in Sensor and Location Platform](privacy-and-security-in-the-sensor-and-location-platform.md)
</dt> <dt>

[Richiesta di autorizzazioni utente](requesting-user-permissions.md)
</dt> </dl>

 

 
