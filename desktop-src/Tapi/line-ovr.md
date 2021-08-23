---
description: Il concetto di linea si è evoluto nel tempo ed è stato in parte sostituito dai concetti relativi a indirizzi e terminali. TAPI 3 non usa direttamente il concetto di linea, ma TAPI 2 continua a incorporare questo paradigma.
ms.assetid: 3e457c7d-da2e-4667-aade-053610abbb8a
title: A linee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c299924a69d3e6e4889d14a72a571ca11ed2dc9e97514702f8ba4836f4c5b99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660206"
---
# <a name="line"></a>A linee

Il concetto di linea si è evoluto nel tempo ed è stato in parte sostituito dai concetti relativi a indirizzi e terminali. TAPI 3 non usa direttamente il concetto di linea, ma TAPI 2 continua a incorporare questo paradigma.

Un *dispositivo linea* è un dispositivo fisico, ad esempio una scheda fax, un modem o una scheda ISDN connessa a una rete. Il dispositivo potrebbe non essere fisicamente connesso al computer in cui è in esecuzione l'applicazione TAPI, ad esempio un pool di modem in un server. I dispositivi line supportano le funzionalità di comunicazione consentendo alle applicazioni di inviare o ricevere informazioni da una rete. Un dispositivo linea contiene un set di uno o più canali omogenei che possono essere usati per stabilire le chiamate.

Nelle applicazioni TAPI 2.x, un dispositivo linea è la rappresentazione logica di un dispositivo telefonico fisico. Anche se "line" spesso indica qualcosa con due endpoint, è possibile astrarre un dispositivo linea a un singolo punto perché TAPI lo visualizza solo come punto di ingresso alla linea che porta all'interruttore.

![dispositivi line](images/ch0501.png)

Anche se le tre righe nella figura precedente sono costituite da hardware diverso e usate per funzioni diverse, vengono astratte allo stesso tipo di dispositivo e regolate dalle stesse regole. Il telefono non rappresenta un dispositivo telefonico, ma un dispositivo linea usato per le chiamate vocali. Quando si usa questo dispositivo linea per le chiamate in ingresso o in uscita, l'applicazione deve anche aprire e controllare un'istanza della classe phone-device, descritta in dettaglio nelle sezioni successive.

La classe del dispositivo linea è una rappresentazione indipendente dal dispositivo di un dispositivo di linea fisico, ad esempio un modem. Può contenere uno o più canali di comunicazione identici (usati per la segnalazione e/o le informazioni) tra l'applicazione e il commutatore o la rete. Poiché i canali appartenenti a una singola riga hanno funzionalità identiche, sono intercambiabili. In molti casi (come con POTS), un provider di servizi modella una linea come con un solo canale. Altre tecnologie, ad esempio ISDN, offrono più canali e il provider di servizi deve trattarli di conseguenza.

**TAPI 2.x:** Le applicazioni individuano le funzionalità di linea [**usando la funzione lineGetDevCaps.**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) La negoziazione della versione tramite le funzioni [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) deve essere stata chiamata in precedenza.

**TAPI 3.x:** Le applicazioni si basano principalmente sul concetto di indirizzo.

 

 
