---
title: Modifiche al supporto hardware legacy di DX9
description: Modifiche al supporto hardware legacy di DX9
ms.assetid: 25C7DFC7-58F4-4F6D-8D26-6DBA92424A0B
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc1ae5c4b15a2019450cc5b209f34561d8ec672d
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "106300574"
---
# <a name="changes-in-dx9-legacy-hardware-support"></a>Modifiche al supporto hardware legacy di DX9

## <a name="platform"></a>Piattaforma

**Client** -Windows 8 


## <a name="description"></a>Descrizione

Intel e AMD/ATI non supportano più le parti grafiche DX9 e non aggiorneranno i driver per questi dispositivi per Windows 8. Inoltre, questi dispositivi non sono inclusi in Windows 8. Gli ultimi driver per questi dispositivi sono quelli disponibili in WU e nei siti Web OEM/IHV. molti dati di vista e molti di questi driver di versione finale presentano problemi in Windows 8. Inoltre, nVidia ha recentemente dichiarato di non supportare le parti di DX9 (vista e precedente) per dispositivi mobili (notebook) per Windows 8. Continuano a supportare le parti DX9 del desktop.

Tutte queste combinazioni di driver/parti si trovano nell'elenco di fallback software di Internet Explorer 9. Ciò significa che, per motivi di prestazioni o di stabilità, Internet Explorer 9 utilizza il rendering del software su questi dispositivi. Questo è un buon indizio che l'esperienza con le app di Windows Store non sarà soddisfacente su questi driver e parti.

## <a name="manifestation"></a>Manifestazione

Poiché non è disponibile alcun supporto per questi dispositivi, molti utenti con queste parti si troveranno in esecuzione sul driver di visualizzazione di base di Microsoft. Si tratta di una GPU software WDDM 1,2 basata su DISTORSIONe ed è effettivamente più veloce di alcune delle parti di questa classe, ad esempio la serie Intel GMA500. Supporta Aero-Glass e DWM ed è in grado di eseguire app di Windows Store.

Tuttavia, presenta alcune limitazioni importanti:

-   Non supporta più monitor o proiezione
-   Non supporta la sospensione, sebbene supporti la sospensione
-   Spesso non è possibile modificare la risoluzione dello schermo

## <a name="mitigation"></a>Strategia di riduzione del rischio

Se dopo il test si scopre che l'esperienza utente non è accettabile, è possibile scegliere di impostare i requisiti hardware per i propri prodotti che escludono le parti Intel e AMD DX9 precedenti. Si può anche scegliere di avvisare i clienti che potrebbero avere un'esperienza inaccettabile su queste parti.

## <a name="tests"></a>Test

Valutare le prestazioni e l'esperienza su questi dispositivi:

-   Qual è l'esperienza della versione del driver finale disponibile?
-   Qual è l'esperienza di MSBDD?

 

 




