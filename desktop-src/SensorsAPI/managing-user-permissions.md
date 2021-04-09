---
description: L'API del sensore fornisce un metodo che è possibile usare per richiedere all'utente le autorizzazioni per usare un sensore o una raccolta di sensori.
ms.assetid: c755edcf-18c1-43d5-9dfe-c073e1f96b5f
title: Gestione delle autorizzazioni utente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecb65fa5a9962be4850aa4711cafa03fb7658212
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966575"
---
# <a name="managing-user-permissions"></a>Gestione delle autorizzazioni utente

L'API del sensore fornisce un metodo che è possibile usare per richiedere all'utente le autorizzazioni per usare un sensore o una raccolta di sensori.

Poiché i sensori possono rivelare informazioni riservate, Windows richiede che gli utenti abiliti i sensori prima che il programma possa accedere a tutti i dati.

Potrebbe essere necessario richiedere l'autorizzazione quando si vogliono usare i sensori per i quali il [**SensorState**](/windows/win32/api/sensorsapi/ne-sensorsapi-sensorstate) corrente è \_ stato \_ \_ negato.

Per richiedere le autorizzazioni, chiamare il metodo [**ISensorManager:: RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) . Quando si chiama questo metodo, Windows apre la finestra di dialogo **Abilita sensori** per richiedere all'utente di abilitare i sensori richiesti. Questa finestra di dialogo consente all'utente di usare i nomi dei sensori richiesti. L'utente può scegliere una delle opzioni seguenti:

-   **Abilitare i sensori**.
-   **Non abilitare questi sensori**.
-   **Aprire il pannello di controllo per altre opzioni**.

Se un utente sceglie di **non abilitare questi sensori**, Windows non visualizzerà di nuovo la finestra di dialogo **Abilita sensori** per quei sensori specifici, anche se il programma chiama [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions). Se l'utente sceglie un'altra opzione, Windows consentirà la visualizzazione della finestra di dialogo quando richiesto. Se la chiamata a **RequestPermissions** contiene alcuni sensori che l'utente ha scelto in precedenza di rimanere disabilitato, l'API del sensore rimuoverà questi sensori dall'elenco dei sensori che l'utente vede.

### <a name="modal-or-modeless-behavior"></a>Comportamento modale o non modale

Il metodo [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) accetta un argomento **booleano** che determina se la finestra di dialogo **Abilita sensori** viene visualizzata come finestra modale o non modale. Questa impostazione influiscono inoltre sull'eventuale comportamento del codice restituito dalla finestra di dialogo come sincrono o asincrono.

Quando modale, la finestra di dialogo ha lo stato attivo esclusivo tra le finestre dell'applicazione fino a quando l'utente non sceglie un'opzione e il codice **HRESULT** restituito dalla chiamata a [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) indica la scelta dell'utente. Quando non è modale, la finestra di dialogo non ha lo stato attivo esclusivo e la chiamata a **RequestPermissions** restituisce immediatamente un risultato. In questo caso, il codice restituito indica se il metodo ha avuto esito positivo, ma non può essere usato per verificare la scelta dell'utente. È quindi possibile determinare quali sensori sono stati abilitati gestendo l'evento [**OnStateChanged**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensorevents-onstatechanged) e controllando che ogni sensore sia \_ pronto per lo stato del sensore \_ .

Per ulteriori informazioni sui codici restituiti, vedere la pagina di riferimento di [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) .

### <a name="best-practice-avoid-multiple-modeless-calls-to-requestpermissions"></a>Procedura consigliata: evitare più chiamate non modali a RequestPermissions

Le chiamate non modali ripetute a [**RequestPermissions**](/windows/win32/api/sensorsapi/nf-sensorsapi-isensormanager-requestpermissions) visualizzeranno più istanze della finestra di dialogo **Abilita questi sensori** e potrebbero compromettere lo schermo con le finestre di dialogo, causando un'esperienza utente insufficiente. Se si ritiene che dopo la prima chiamata a **RequestPermissions**, potrebbero essere installati altri sensori di posizione, richiedendo un'altra chiamata a **RequestPermissions**, è necessario chiamare **RequestPermissions** modale oppure attendere che tutti i sensori di posizione siano installati per effettuare una chiamata non modale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Privacy e sicurezza nella piattaforma sensore e posizione](privacy-and-security-in-the-sensor-and-location-platform.md)
</dt> <dt>

[Richiesta di autorizzazioni utente](requesting-user-permissions.md)
</dt> </dl>

 

 
