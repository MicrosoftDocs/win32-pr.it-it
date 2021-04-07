---
description: TAPI 3 prevede una serie di oggetti indipendenti dai cinque oggetti TAPI principali (TAPI, Address, Call, CallHub e Terminal).
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Oggetti Stand-Alone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103881646"
---
# <a name="stand-alone-objects"></a>Oggetti Stand-Alone

TAPI 3 prevede una serie di oggetti indipendenti dai cinque oggetti TAPI principali (TAPI, Address, Call, CallHub e Terminal). Le [interfacce di eventi](./event-interfaces.md) e le interfacce di [enumeratore](enumerator-interfaces.md) sono oggetti autonomi e vengono riepilogate separatamente. Di seguito vengono riepilogate le interfacce autonome non di eventi e non enumeratori.



| Interfaccia                                             | Descrizione                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | Fornisce metodi per consentire alle applicazioni client di automazione, ad esempio Visual Basic di recuperare informazioni sulla raccolta.                                                                                             |
| [**ITCollection2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | Estende [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) fornendo metodi aggiuntivi per la modifica delle raccolte.                                                                                                       |
| [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | Interfaccia COM standard per l'implementazione dell'automazione.                                                                                                                                                           |
| [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | Interfaccia COM standard per ottenere i puntatori alle interfacce di oggetti.                                                                                                                                             |
| [**ITDispatchMapper**](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | Consente a un'applicazione di recuperare il puntatore di invio di un'altra interfaccia su un oggetto, dato un puntatore [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) corrente. Utile per alcuni linguaggi di scripting. |
| [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | Fornisce metodi che consentono a un'applicazione TAPI 3 di utilizzare la [telefonia assistita](assisted-telephony-overview.md).                                                                                                |



 



| Interfaccia                                  | Descrizione                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | Avvia, arresta e sospende le azioni correnti, ad esempio una riproduzione.                                                                                                             |
| [**ITMediaPlayback**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | Fornisce metodi specifici per la riproduzione che consentono a un'applicazione di eseguire operazioni come l'impostazione dell'elenco di file da riprodurre e la modifica della velocità di riproduzione.              |
| [**ITMediaRecord**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | Fornisce metodi specifici della registrazione che consentono a un'applicazione di eseguire operazioni come l'impostazione dei nomi dei file da registrare e la modifica della durata di una registrazione. |



 



| Interfaccia                                                  | Descrizione                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITScriptableAudioFormat**](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | Recupera il formato audio da o imposta il formato audio per una traccia.                                                                                             |
| [**ITStaticAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | Fornisce metodi su oggetti terminali audio statici necessari per supportare i dispositivi telefonici. TAPI 3,1 MSPs deve esporre questa interfaccia su tutti i terminali audio statici. |



 

 

 
