---
description: Nel tempo è possibile che esistano versioni diverse per le applicazioni TAPI, TAPI e i provider di servizi.
ms.assetid: 39b16328-931e-4d75-a6ec-1edc97f1a287
title: Negoziazione della versione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: beffff7ceeb90ccf419e138986562ca90f83c204
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968286"
---
# <a name="version-negotiation"></a>Negoziazione della versione

Nel tempo è possibile che esistano versioni diverse per le applicazioni TAPI, TAPI e i provider di servizi. L'interoperabilità ottimale di un'applicazione TAPI richiede una conoscenza non solo della versione TAPI dell'applicazione, ma anche delle versioni del provider di servizi, TAPISVR e DLL di TAPI.

La mancata corretta negoziazione della versione può causare gravi problemi. Alcune strutture utilizzate, ad esempio, hanno membri dati aggiunti da una versione a quella successiva. Se la dimensione della struttura non corrisponde a quella prevista dall'applicazione o da TAPI, le conseguenze variano a causa di perdite di memoria in AVs intermittenti.

Per ulteriori informazioni, vedere [controllo delle versioni di TAPI](./tapi-versioning.md).

**TAPI 2. x:** Le applicazioni negoziano con TAPI e TAPISVR durante [**lineInitializeEx**](/windows/win32/api/tapi/nf-tapi-lineinitializeexa). Le applicazioni eseguono la negoziazione del dispositivo con i provider di servizi chiamando [**lineNegotiateAPIVersion**](/windows/win32/api/tapi/nf-tapi-linenegotiateapiversion) per ogni riga che l'applicazione potrebbe usare.

**TAPI 3. x:** Non è necessario eseguire la negoziazione della versione. Tuttavia, è possibile utilizzare [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) per determinare se un'interfaccia è disponibile nella propria versione.

 

 
