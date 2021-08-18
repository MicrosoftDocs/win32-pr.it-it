---
description: Una pagina di riferimento eventi (ERP) è un documento HTML che fornisce Network Monitor sugli eventi rilevati durante l'operazione di esperti o di monitoraggio.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Informazioni sulle pagine di riferimento per gli eventi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f277e2fc31050c5702c1f3cbb3a9b188515386f0b30522fd511771c0b9f3a69e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119744871"
---
# <a name="about-event-reference-pages"></a>Informazioni sulle pagine di riferimento per gli eventi

Una pagina di riferimento eventi (ERP) è un documento HTML che fornisce Network Monitor sugli eventi rilevati durante l'operazione di esperti o di monitoraggio.

È possibile visualizzare gli EP nel Visualizzatore eventi di Network Monitor, strumento di controllo di monitoraggio o in qualsiasi browser che supporti le funzionalità HTML di Microsoft Internet Explorer versione 4.01 o successiva. In altre informazioni, è possibile aggiungere controlli supportati o linguaggi con script nel proprio ERP.

Tuttavia, gli EERP vengono visualizzati solo se l'esperto designa il documento HTML in base al nome. Quando viene designato correttamente, l'ERP viene visualizzato nel riquadro inferiore quando l'evento nel Visualizzatore eventi selezionato. La figura seguente mostra un ERP associato al monitoraggio dell'intervallo IP (Internet Protocol).

![un erp associato al monitoraggio dell'intervallo IP](images/exview2.png)

## <a name="expert-events"></a>Eventi esperti

Gli eventi esperti sono identificati dal **membro EventIdent** di una [**struttura NMEVENTDATA.**](nmeventdata.md) Quando si scrive un esperto, si determinano i **valori EventIdent,** in genere numerati 1, 2, 3 e così via. Si supponga, ad esempio, che un esperto generi due eventi (**EventIdent1** ed **EventIdent2**). Se si vuole che Visualizzatore eventi gli eventi separatamente, è necessario creare due documenti ERP separati.

 

 



