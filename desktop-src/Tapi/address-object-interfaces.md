---
description: Gli oggetti address sono entità che possono effettuare o ricevere chiamate. Le interfacce e i metodi correlati consentono a un'applicazione di ottenere e impostare informazioni relative a un indirizzo, ad esempio se l'indirizzo dispone del supporto dell'ID chiamante.
ms.assetid: 6e347e4c-aec3-4bbd-95f3-a68e6e136e11
title: Interfacce dell'oggetto Address
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2254ba47e81ebd40f5ce95a1c870c363d09243c69cec0c4ec358cf3ee5604de7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117949177"
---
# <a name="address-object-interfaces"></a>Interfacce dell'oggetto Address

[Gli oggetti](address-object.md) address sono entità che possono effettuare o ricevere chiamate. Le interfacce e i metodi correlati consentono a un'applicazione di ottenere e impostare informazioni relative a un indirizzo, ad esempio se l'indirizzo dispone del supporto dell'ID chiamante.

Le [**interfacce ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent), [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo), [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard), [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation), [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)e [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress) non sono esposte direttamente nell'oggetto Address, ma sono strettamente correlate e sono elencate qui per praticità di riferimento.



| Interfaccia                                                            | Descrizione                                                                                                                                     |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ITAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                       | Funge da interfaccia di base per l'oggetto Address.                                                                                                  |
| [**ITAddress2**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress2)                                     | Deriva da [**ITAddress.**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress) fornisce metodi aggiuntivi che supportano i dispositivi telefonici.                                            |
| [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities)               | Ottiene informazioni relative alle funzionalità di un indirizzo.                                                                                          |
| [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent)                             | Fornisce informazioni sugli eventi di indirizzo.                                                                                                 |
| [**ITAddressTranslation**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslation)                 | Esegue la conversione degli indirizzi.                                                                                                                   |
| [**ITAddressTranslationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresstranslationinfo)         | Ottiene informazioni sulla conversione degli indirizzi.                                                                                                           |
| [**ITCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                               | Fornisce metodi per recuperare le informazioni sulla scheda chiamante.                                                                                          |
| [**ITForwardInformation**](/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation)                 | Fornisce metodi per la configurazione e l'implementazione dell'inoltro di chiamate.                                                                               |
| [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol)   | Supporta le applicazioni legacy che richiedono l'accesso diretto a un dispositivo e alla relativa configurazione.                                                      |
| [**ITLegacyAddressMediaControl2**](/windows/desktop/api/Tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2) | Estende [**ITLegacyAddressMediaControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol) consentendo la configurazione dei parametri correlati ai dispositivi line. |
| [**ITLocationInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itlocationinfo)                             | Ottiene informazioni correlate alla posizione dell'entità chiamante.                                                                                  |
| [**ITMediaSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itmediasupport)                             | Ottiene informazioni relative alle funzionalità di supporto multimediale di un indirizzo.                                                                            |
| [**ITTerminalSupport**](/windows/win32/api/tapi3if/nn-tapi3if-itterminalsupport)                       | Ottiene informazioni sui terminali disponibili e fornisce un metodo per creare terminali aggiuntivi.                                                   |
| [**IEnumAddress**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumaddress)                                 | Enumera [**ITAddress.**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddress)                                                                                                      |
| [**IEnumCallingCard**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumcallingcard)                         | Enumera [**ITCallingCard.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallingcard)                                                                                              |



 

Se l'indirizzo è [un indirizzo Wave MSP,](wave-msp.md) [**l'interfaccia ITLegacyWaveSupport**](/windows/desktop/api/tapi3if/nn-tapi3if-itlegacywavesupport) viene esposta anche nell'oggetto Address.

 

 
