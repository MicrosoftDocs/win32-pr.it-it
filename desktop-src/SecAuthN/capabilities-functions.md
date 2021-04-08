---
description: L'API del provider di rete specifica una singola funzione di funzionalità.
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: Funzioni funzionalità
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104049770"
---
# <a name="capabilities-functions"></a>Funzioni funzionalità

L'API del provider di rete specifica una singola funzione di funzionalità. Quando il sistema operativo richiede informazioni sulle funzionalità di un provider di rete, il [*router multi-provider*](/windows/desktop/SecGloss/m-gly) (MPR) chiama la funzione [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) di ogni provider di rete la cui rete è attiva.

La funzione [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) restituisce una maschera di maschera che indica le funzioni dell'API del provider di rete supportata dal provider di rete. La funzione **NPGetCaps** è l'unica funzione che deve essere implementata da un provider di rete. Il sistema operativo chiama questa funzione per determinare quali altre funzioni dell'API del provider di rete supporta il provider.

 

 
