---
description: Nel tempo è possibile che esistano versioni diverse per TAPI, le applicazioni e i provider di servizi per una riga o un telefono.
ms.assetid: 36a17ae8-31db-4db9-a401-097d47aa26ad
title: Negoziazione della versione di TAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f41f4ca6f12862d6fc19f982c48b90bdafe2aaa2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315262"
---
# <a name="tapi-version-negotiation"></a>Negoziazione della versione di TAPI

Nel tempo è possibile che esistano versioni diverse per TAPI, le applicazioni e i provider di servizi per una riga o un telefono. Le nuove versioni possono definire nuove funzionalità, nuovi campi per le strutture di dati e così via. I numeri di versione indicano pertanto come interpretare diverse strutture di dati.

Per consentire l'interoperabilità ottimale di versioni diverse di applicazioni, versioni di TAPI e versioni di provider di servizi da fornitori diversi, TAPI fornisce un semplice meccanismo di negoziazione della versione in due passaggi per le applicazioni. È necessario concordare due diverse versioni dell'applicazione, TAPI e del provider di servizi per ogni dispositivo line. Il primo è il numero di versione per la telefonia di base e supplementare e viene indicato come versione dell'API. L'altro è per le estensioni specifiche del provider, se presente, e viene indicato come versione dell'estensione. Il formato delle strutture di dati e dei tipi di dati usati dalle funzionalità di base e supplementare di TAPI è definito dalla versione dell'API, mentre la versione dell'estensione determina il formato delle strutture di dati definite dalle estensioni specifiche del fornitore.

La negoziazione della versione continua con due fasi. Nella prima fase, il numero di versione dell'API viene negoziato e viene ottenuto l'identificatore dell'estensione associato a tutte le estensioni specifiche del fornitore supportate nel dispositivo. Nella seconda fase viene negoziata la versione dell'estensione. Se l'applicazione non usa estensioni API, ignora la seconda fase e le estensioni non vengono attivate dal provider di servizi. Se l'applicazione vuole usare le estensioni, ma le estensioni del provider di servizi (l'identificatore dell'estensione) non sono riconosciute dall'applicazione, l'applicazione deve ignorare la negoziazione anche per la versione dell'estensione. Ogni fornitore dispone di un proprio set di versioni legali (riconosciute) per ogni set di specifiche di estensione che distribuisce.

La funzione [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) viene usata per negoziare il numero di versione dell'API da usare. Recupera anche l'identificatore dell'estensione supportato dal dispositivo a linee, restituendo gli zeri se non sono supportate estensioni. Con questa chiamata di funzione, l'applicazione fornisce l'intervallo di versioni dell'API con cui è compatibile. TAPI a sua volta negozia con il provider di servizi della linea per determinare l'intervallo di versioni dell'API supportato. Successivamente, TAPI seleziona un numero di versione (in genere, anche se non necessariamente, il numero di versione più alto) nell'intervallo di versioni sovrapposte fornito dall'applicazione, dalla DLL e dal provider di servizi. Questo numero viene restituito all'applicazione, insieme all'identificatore dell'estensione che definisce le estensioni disponibili dal provider di servizi di tale riga.

Se l'applicazione vuole usare le estensioni definite dall'identificatore di estensione restituito, deve prima chiamare [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion) per negoziare la versione dell'estensione. In una fase di negoziazione simile, l'applicazione specifica la versione dell'API già concordata e l'intervallo di versioni dell'estensione che supporta. TAPI passa queste informazioni al provider di servizi per la riga. Il provider di servizi controlla la versione dell'API e l'intervallo di versioni dell'estensione rispetto a se stesso e seleziona il numero di versione dell'estensione appropriato, se disponibile.

Quando l'applicazione chiama in un secondo momento [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps), restituisce un set di funzionalità del dispositivo per la riga che corrispondono ai risultati della negoziazione della versione. Sono incluse le funzionalità del dispositivo della linea coerenti con la versione dell'API e le funzionalità specifiche del dispositivo della linea coerenti con la versione dell'estensione. Quando si apre una riga, l'applicazione deve specificare entrambi i numeri di versione. A questo punto, l'applicazione, la DLL e il provider di servizi si impegnano a usare le versioni concordate. Se le estensioni specifiche del dispositivo non devono essere usate, la versione dell'estensione deve essere specificata come zero.

In un ambiente in cui più applicazioni aprono lo stesso dispositivo a linee, la prima applicazione per aprire il dispositivo linea seleziona le versioni per tutte le applicazioni future che vogliono usare la linea (i provider di servizi non supportano più versioni simultaneamente). Analogamente, un'applicazione che apre più dispositivi linea può risultare più semplice utilizzare tutti i dispositivi linea con lo stesso numero di versione dell'API.

Ogni funzione che accetta un parametro *dwAPIVersion* o analogo deve impostare questo parametro sulla versione API più elevata supportata dall'applicazione o sulla versione dell'API negoziata usando la funzione [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion) o [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) in un particolare dispositivo. Usare la tabella seguente come guida:



| Funzione                                                     | Significato                                                                               |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)             | Usa la versione restituita da [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineGetCountry**](/windows/desktop/api/Tapi/nf-tapi-linegetcountry)                     | Usare la versione più recente supportata dall'applicazione.                                     |
| [**lineGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetdevcaps)                     | Usa la versione restituita da [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineGetProviderList**](/windows/desktop/api/Tapi/nf-tapi-linegetproviderlist)           | Usare la versione più recente supportata dall'applicazione.                                     |
| [**lineGetTranslateCaps**](/windows/desktop/api/Tapi/nf-tapi-linegettranslatecaps)         | Usare la versione più recente supportata dall'applicazione.                                     |
| [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion)   | Usare la versione più recente supportata dall'applicazione.                                     |
| [**lineNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateextversion)   | Usa la versione restituita da [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineOpen**](/windows/desktop/api/Tapi/nf-tapi-lineopen)                                 | Usa la versione restituita da [**lineNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-linenegotiateapiversion).   |
| [**lineTranslateAddress**](/windows/desktop/api/Tapi/nf-tapi-linetranslateaddress)         | Usare la versione più recente supportata dall'applicazione.                                     |
| [**lineTranslateDialog**](/windows/desktop/api/Tapi/nf-tapi-linetranslatedialog)           | Usare la versione più recente supportata dall'applicazione.                                     |
| [**phoneGetDevCaps**](/windows/desktop/api/Tapi/nf-tapi-phonegetdevcaps)                   | Usa la versione restituita da [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion) | Usare la versione più recente supportata dall'applicazione.                                     |
| [**phoneNegotiateExtVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateextversion) | Usa la versione restituita da [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |
| [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen)                               | Usa la versione restituita da [**phoneNegotiateAPIVersion**](/windows/desktop/api/Tapi/nf-tapi-phonenegotiateapiversion). |



 

> [!IMPORTANT]
> Quando si negozia una versione dell'API, impostare sempre i numeri di versione alta e bassa sull'intervallo di versioni che l'applicazione è in grado di supportare. Ad esempio, non usare mai 0x00000000 per la versione bassa o 0xFFFFFFFF per l'alta perché questi valori richiedono che l'applicazione supporti tutte le versioni di TAPI, sia passate che future.

 

 

 



