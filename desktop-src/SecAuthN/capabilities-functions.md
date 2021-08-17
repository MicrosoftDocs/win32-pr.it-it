---
description: L'API del provider di rete specifica una singola funzione di funzionalità.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funzioni di funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab47d2c8323131b396640d9154e33749c1716db0d369d3a374f69131468613d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119141274"
---
# <a name="capabilities-functions"></a>Funzioni di funzionalità

L'API del provider di rete specifica una singola funzione di funzionalità. Quando il sistema operativo richiede informazioni sulle funzionalità di un provider di rete, il [*router*](/windows/desktop/SecGloss/m-gly) a più provider chiama la funzione [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) di ogni provider di rete la cui rete è attiva.

La [**funzione NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) restituisce una maschera di bit che indica le funzioni dell'API del provider di rete supportate dal provider di rete. La **funzione NPGetCaps** è l'unica funzione che un provider di rete deve implementare. Il sistema operativo chiama questa funzione per determinare le altre funzioni dell'API del provider di rete supportate dal provider.

 

 
