---
description: Nel corso del tempo possono esistere versioni diverse per TAPI, applicazioni e provider di servizi per una linea o un telefono.
ms.assetid: 36a17ae8-31db-4db9-a401-097d47aa26ad
title: Negoziazione della versione TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7cd6d816c07cb1c6c93d9cc219509f257d9a2695671b5197002171f0f819f17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119404066"
---
# <a name="tapi-version-negotiation"></a>Negoziazione della versione TAPI

Nel corso del tempo possono esistere versioni diverse per TAPI, applicazioni e provider di servizi per una linea o un telefono. Le nuove versioni possono definire nuove funzionalità, nuovi campi per le strutture di dati e così via. I numeri di versione indicano quindi come interpretare varie strutture di dati.

Per consentire l'interoperabilità ottimale di versioni diverse di applicazioni, versioni di TAPI e versioni di provider di servizi di fornitori diversi, TAPI fornisce un semplice meccanismo di negoziazione della versione in due passaggi per le applicazioni. L'applicazione, TAPI e il provider di servizi, devono concordare due versioni diverse per ogni dispositivo line. Il primo è il numero di versione per telefonia di base e supplementare ed è indicato come versione dell'API. L'altra è per le estensioni specifiche del provider, se presenti, e viene definita versione dell'estensione. Il formato delle strutture di dati e dei tipi di dati usati dalle funzionalità di base e supplementari di TAPI è definito dalla versione dell'API, mentre la versione dell'estensione determina il formato delle strutture di dati definite dalle estensioni specifiche del fornitore.

La negoziazione della versione procede in due fasi. Nella prima fase viene negoziato il numero di versione dell'API e viene ottenuto l'identificatore di estensione associato alle estensioni specifiche del fornitore supportate nel dispositivo. Nella seconda fase viene negoziata la versione dell'estensione. Se l'applicazione non usa estensioni API, ignora la seconda fase e le estensioni non vengono attivate dal provider di servizi. Se l'applicazione vuole usare le estensioni, ma le estensioni del provider di servizi (l'identificatore dell'estensione) non vengono riconosciute dall'applicazione, l'applicazione deve ignorare anche la negoziazione per la versione dell'estensione. Ogni fornitore ha un proprio set di versioni legali (riconosciute) per ogni set di specifiche di estensione che distribuisce.

La [**funzione lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) viene usata per negoziare il numero di versione dell'API da usare. Recupera anche l'identificatore di estensione supportato dal dispositivo line, restituisce zeri se non sono supportate estensioni. Con questa chiamata di funzione, l'applicazione fornisce l'intervallo di versioni dell'API con cui è compatibile. TAPI negozia a sua volta con il provider di servizi della riga per determinare l'intervallo di versioni api che supporta. TAPI seleziona quindi un numero di versione (in genere, anche se non necessariamente, il numero di versione più alto) nell'intervallo di versioni sovrapposto fornito dall'applicazione, dalla DLL e dal provider di servizi. Questo numero viene restituito all'applicazione, insieme all'identificatore dell'estensione che definisce le estensioni disponibili dal provider di servizi di tale riga.

Se l'applicazione vuole usare le estensioni definite dall'identificatore di estensione restituito, deve prima chiamare [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) per negoziare la versione dell'estensione. In una fase di negoziazione simile, l'applicazione specifica la versione dell'API già concordata e l'intervallo di versioni dell'estensione che supporta. TAPI passa queste informazioni al provider di servizi per la riga . Il provider di servizi controlla la versione dell'API e l'intervallo di versioni dell'estensione rispetto al proprio e seleziona il numero di versione dell'estensione appropriato, se presente.

Quando in seguito l'applicazione chiama [**lineGetDevCaps,**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)restituisce un set di funzionalità del dispositivo per la riga che corrispondono ai risultati della negoziazione della versione. Sono incluse le funzionalità del dispositivo della riga coerenti con la versione dell'API e le funzionalità specifiche del dispositivo della riga coerenti con la versione dell'estensione. Quando si apre una riga, l'applicazione deve specificare entrambi questi numeri di versione. A questo punto, viene eseguito il commit dell'applicazione, della DLL e del provider di servizi all'utilizzo delle versioni concordate. Se le estensioni specifiche del dispositivo non devono essere usate, la versione dell'estensione deve essere specificata come zero.

In un ambiente in cui più applicazioni aprono lo stesso dispositivo line, la prima applicazione che apre il dispositivo line seleziona le versioni per tutte le applicazioni future che vogliono usare la riga (i provider di servizi non supportano più versioni contemporaneamente). Analogamente, un'applicazione che apre più dispositivi line può risultare più semplice usare tutti i dispositivi line con lo stesso numero di versione dell'API.

Ogni funzione che accetta *un parametro dwAPIVersion* o un parametro simile deve impostare questo parametro sulla versione api più recente supportata dall'applicazione o sulla versione dell'API negoziata usando la funzione [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) o [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) in un dispositivo specifico. Usare la tabella seguente come guida:



| Funzione                                                     | Significato                                                                               |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)             | Usare la versione [**restituita da lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)                     | Usare la versione più recente supportata dall'applicazione.                                     |
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)                     | Usare la versione [**restituita da lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist)           | Usare la versione più recente supportata dall'applicazione.                                     |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)         | Usare la versione più recente supportata dall'applicazione.                                     |
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   | Usare la versione più recente supportata dall'applicazione.                                     |
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion)   | Usare la versione [**restituita da lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)                                 | Usare la versione [**restituita da lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)         | Usare la versione più recente supportata dall'applicazione.                                     |
| [**Finestra di dialogo lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog)           | Usare la versione più recente supportata dall'applicazione.                                     |
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)                   | Usare la versione restituita [**da phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Usare la versione più recente supportata dall'applicazione.                                     |
| [**phoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Usare la versione restituita [**da phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)                               | Usare la versione restituita [**da phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |



 

> [!IMPORTANT]
> Quando si negozia una versione dell'API, impostare sempre i numeri di versione alti e bassi sull'intervallo di versioni che l'applicazione può supportare. Ad esempio, non usare mai 0x00000000 per la versione bassa o 0xFFFFFFFF per la versione elevata perché questi valori richiedono che l'applicazione supporti tutte le versioni di TAPI, sia passate che future.

 

 

 



