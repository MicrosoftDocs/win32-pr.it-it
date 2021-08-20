---
title: Modifiche al supporto hardware legacy DX9
description: Modifiche al supporto hardware legacy DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bfd0b8bbb05161ffe14ff57cc5db97fe88a22bf6e64a495e2b43dd8240def82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118211807"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a>Modifiche al supporto hardware legacy DX9

## <a name="platform"></a>Piattaforma

**Client** : Windows 8 


## <a name="description"></a>Descrizione

Intel e AMD/ATI non supportano più le parti grafiche DX9 e non aggiornano i driver per questi dispositivi per Windows 8. Inoltre, questi dispositivi non vengono trattati in modo Windows 8. Gli ultimi driver per questi dispositivi sono quelli disponibili in WU e nei siti Web OEM/IHV; molte date da Vista e molti di questi driver di versione finale presentano problemi Windows 8. Inoltre, nVidia ha dichiarato di recente che non supporterà le parti DX9 (Vista e versioni precedenti) per dispositivi mobili (notebook) per Windows 8. Continuano a supportare le parti DX9 desktop.

Tutte queste combinazioni di driver/parti sono nell'Internet Explorer di fallback software 9. Ciò significa che per motivi di prestazioni o stabilità, Internet Explorer 9 usa il rendering software in questi dispositivi. Si tratta di un buon indicatore del fatto che l'esperienza Windows app di Store non sarà soddisfacente per questi driver e parti.

## <a name="manifestation"></a>Manifestazione

Poiché non è disponibile alcun supporto in-box per questi dispositivi, molti utenti con queste parti verranno eseguiti in Microsoft Basic Display Driver. Si tratta di una GPU software WDDM 1.2 basata su WARP ed è effettivamente più veloce di alcune delle parti di questa classe, ad esempio la serie Intel GMA500. Supporta l'aero-glass e DWM ed è in grado di eseguire Windows store.

Tuttavia, presenta alcune limitazioni importanti:

-   Non supporta più monitor o proiezioni
-   Non supporta la sospensione, anche se supporta l'ibernazione
-   Spesso non consente la modifica della risoluzione dello schermo

## <a name="mitigation"></a>Strategia di riduzione del rischio

Se dopo il test l'esperienza utente non è accettabile, è possibile scegliere di impostare i requisiti hardware per i prodotti che escludono queste parti Intel e AMD DX9 precedenti. È anche possibile scegliere di avvisare i clienti che potrebbero avere un'esperienza inaccettabile in queste parti.

## <a name="tests"></a>Test

Valutare le prestazioni e l'esperienza in questi dispositivi:

-   Qual è l'esperienza della versione finale del driver disponibile?
-   Qual è l'esperienza in MSBDD?

 

 




