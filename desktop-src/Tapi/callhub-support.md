---
description: Il rilevamento CallHub è una nuova funzionalità della versione 3,0 di TAPI.
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: Supporto di CallHub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314633"
---
# <a name="callhub-support"></a>Supporto di CallHub

Il rilevamento CallHub è una nuova funzionalità della versione 3,0 di TAPI. La funzionalità CallHub è stata aggiunta agli elementi di programmazione TAPI 2,1 con la consegna di Windows 2000. Un *CallHub* rappresenta una visualizzazione di una chiamata di terze parti e gli handle di chiamata di TAPI rappresentano la visualizzazione di una chiamata. Con il rilevamento CallHub, il provider di servizi deve seguire CallHubs e fornire informazioni sulla chiamata nel corso della durata di un CallHub. Quando le nuove entità si uniscono e lasciano il CallHub, il provider di servizi deve informare TAPI.

Un provider di servizi non deve implementare nuove funzioni per supportare CallHub. Deve semplicemente compilare il membro **dwCallID** della struttura [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) . In TAPI 3, TAPI raccoglie tutte le chiamate con lo stesso **dwCallID** e crea un handle CallHub che l'applicazione può usare per tenere traccia della chiamata.

 

 
