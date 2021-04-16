---
description: Il concetto di linea si è evoluto nel tempo ed è stato sostituito in parte dai concetti relativi all'indirizzo e al terminale. TAPI 3 non usa direttamente il concetto di linea, ma TAPI 2 continua a incorporare questo paradigma.
ms.assetid: 3e457c7d-da2e-4667-aade-053610abbb8a
title: Linea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8275555e0cb34f5831ce671e22a89a1499fb1796
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558669"
---
# <a name="line"></a>Linea

Il concetto di linea si è evoluto nel tempo ed è stato sostituito in parte dai concetti relativi all'indirizzo e al terminale. TAPI 3 non usa direttamente il concetto di linea, ma TAPI 2 continua a incorporare questo paradigma.

Un *dispositivo a linee* è un dispositivo fisico, ad esempio una lavagna fax, un modem o una scheda ISDN connessa a una rete. Il dispositivo potrebbe non essere fisicamente connesso al computer in cui è in esecuzione l'applicazione TAPI, ad esempio un pool di modem in un server. I dispositivi linea supportano le funzionalità di comunicazione consentendo alle applicazioni di inviare o ricevere informazioni da una rete. Un dispositivo linea contiene un set di uno o più canali omogenei che possono essere utilizzati per stabilire le chiamate.

All'interno delle applicazioni TAPI 2. x, un dispositivo a linee è la rappresentazione logica di un dispositivo telefonico fisico. Sebbene "line" contenga spesso un elemento con due endpoint, è possibile astrarre un dispositivo a linee in un singolo punto perché TAPI lo Visualizza solo come punto di ingresso alla riga che conduce all'opzione.

![dispositivi linea](images/ch0501.png)

Sebbene le tre righe nell'illustrazione precedente siano costituite da hardware diverso e utilizzate per diverse funzioni, vengono astratte allo stesso tipo di dispositivo e regolate dalle stesse regole. Il telefono non rappresenta un dispositivo telefonico, ma un dispositivo di linea usato per le chiamate vocali. Quando si usa questo dispositivo a linee per le chiamate in ingresso o in uscita, l'applicazione deve anche aprire e controllare un'istanza della classe del dispositivo telefonico, descritta in dettaglio nelle sezioni successive.

La classe del dispositivo di linea è una rappresentazione indipendente dal dispositivo di un dispositivo a linee fisico, ad esempio un modem. Può contenere uno o più canali di comunicazione identici (usati per la segnalazione e/o le informazioni) tra l'applicazione e il Commuter o la rete. Poiché i canali che appartengono a una singola riga hanno funzionalità identiche, sono intercambiabili. In molti casi, come per i contenitori, un provider di servizi modella una riga come avente un solo canale. Altre tecnologie, come ISDN, offrono un numero maggiore di canali e il provider di servizi deve gestirli di conseguenza.

**TAPI 2. x:** Le applicazioni individuano le funzionalità della linea usando la funzione [**lineGetDevCaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) . La negoziazione della versione con le funzioni [**lineNegotiateExtVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateextversion) di [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) deve essere stata chiamata in precedenza.

**TAPI 3. x:** Le applicazioni si basano principalmente sul concetto di indirizzo.

 

 
