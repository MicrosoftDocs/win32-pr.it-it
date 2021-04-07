---
description: Le interfacce di oggetti terminal consentono a un'applicazione di accedere ai dispositivi di manipolazione usati per creare o ricevere flussi multimediali.
ms.assetid: 08320d1c-1400-4746-b526-74b0789c5fc0
title: Interfacce di oggetti Terminal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed3286d9a2bf3c247f813d3a1f942b0490de0154
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103760790"
---
# <a name="terminal-object-interfaces"></a>Interfacce di oggetti Terminal

Le interfacce di [oggetti Terminal](terminal-object.md) consentono a un'applicazione di accedere ai dispositivi di manipolazione usati per creare o ricevere flussi multimediali.

Queste interfacce vengono implementate da un MSP e non saranno disponibili se l'indirizzo non è supportato da un provider di servizi multimediali. Se è presente un MSP associato, l'interfaccia [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport) viene esposta nell' [oggetto Address](address-object.md).

Le interfacce [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal) e [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass) non sono direttamente esposte sull'oggetto terminale, ma sono strettamente correlate e sono elencate di seguito per praticità di riferimento.



| Interfaccia                                                                  | Descrizione                                                                                                                       |
|----------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)                                           | Interfaccia di base per l'oggetto terminale. Fornisce metodi per ottenere informazioni come la classe Terminal e i supporti supportati. |
| [**ITAMMediaFormat**](/windows/win32/api/tapi3/nn-tapi3-itammediaformat)                                 | Imposta e ottiene il formato multimediale DirectShow.                                                                                            |
| [**ITBasicAudioTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasicaudioterminal)                       | Fornisce metodi per impostare e ottenere caratteristiche del terminale audio standard, ad esempio volume.                                          |
| [**IEnumTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminal)                                     | Enumera [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal).                                                                                      |
| [**IEnumTerminalClass**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumterminalclass)                           | Enumera la [**classe Terminal**](terminal-class.md).                                                                              |
| [**IEnumPluggableSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggablesuperclassinfo)       | Enumera [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo).                                        |
| [**IEnumPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumpluggableterminalclassinfo) | Enumera [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo).                                                  |
| [**ITFileTrack**](/windows/desktop/api/tapi3if/nn-tapi3if-itfiletrack)                                         | Recupera e imposta le informazioni relative alle tracce del terminale del file.                                                                   |
| [**ITASRTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itasrterminalevent)                           | Recupera la descrizione degli eventi del terminale di riconoscimento vocale automatico.                                                        |
| [**ITFileTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itfileterminalevent)                         | Recupera la descrizione degli eventi terminal del file.                                                                                |
| [**ITMultiTrackTerminal**](/windows/desktop/api/tapi3if/nn-tapi3if-itmultitrackterminal)                       | Enumera, crea o rimuove tracce nei terminali multitraccia.                                                                   |



 



| Interfaccia                                                                                      | Descrizione                                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [**ITPluggableTerminalClassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalclassinfo)                           | Recupera le informazioni relative a un terminale collegabile.                                                                       |
| [**ITPluggableTerminalClassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalclassregistration)           | Crea, modifica o Elimina la voce del registro di sistema per un terminale innestabile.                                                   |
| [**ITPluggableTerminalInitialization**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalinitialization)                 | Esegue la creazione di un oggetto Terminal primario per i terminali collegabili, consentendo a Terminal Manager di inizializzare il terminale. |
| [**ITPluggableTerminalSuperclassInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itpluggableterminalsuperclassinfo)                 | Recupera il nome e il CLSID di una classe terminale innestabile.                                                                  |
| [**ITPluggableTerminalSuperclassRegistration**](/windows/desktop/api/Termmgr/nn-termmgr-itpluggableterminalsuperclassregistration) | Recupera e imposta le informazioni su una superclasse Terminal (Name e CLSID).                                                 |
| [**ITPluggableTerminalEventSink**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink)                           | Notifica alle applicazioni client le modifiche apportate a un terminale innestabile.                                                          |
| [**ITPluggableTerminalEventSinkRegistration**](/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration)   | Registra e Annulla la registrazione di un'applicazione client per la notifica di eventi Terminal collegabili.                             |



 



| Interfaccia                                            | Descrizione                                                        |
|------------------------------------------------------|--------------------------------------------------------------------|
| [**ITTTSTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itttsterminalevent)     | Recupera la descrizione degli eventi del terminale di sintesi vocale. |
| [**ITToneDetectionEvent**](/windows/desktop/api/Tapi3if/nn-tapi3if-ittonedetectionevent) | Recupera informazioni su un evento di rilevamento di un tono.                |
| [**ITToneTerminalEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-ittoneterminalevent)   | Recupera la descrizione degli eventi del terminale di tono.                 |



 

 

 
