---
description: Una pagina di riferimento a un evento è un documento HTML che fornisce Network Monitor informazioni sugli eventi rilevati durante l'esecuzione dell'esperto o del monitoraggio.
ms.assetid: 097bae90-5dab-4f79-a829-648033b38016
title: Informazioni sulle pagine di riferimento evento
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81e989e3e1d4ab0c41dc78c567c662e8a3090906
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882113"
---
# <a name="about-event-reference-pages"></a>Informazioni sulle pagine di riferimento evento

Una pagina di riferimento a un evento è un documento HTML che fornisce Network Monitor informazioni sugli eventi rilevati durante l'esecuzione dell'esperto o del monitoraggio.

È possibile visualizzare ERPs nel Visualizzatore eventi di Network Monitor, strumento di controllo di monitoraggio o in qualsiasi browser che supporti le funzionalità HTML di Microsoft Internet Explorer versione 4,01 o successiva. In altre lingue, è possibile aggiungere i controlli supportati o le lingue con script nell'ERP.

Tuttavia, ERPs vengono visualizzati solo se l'esperto designa il documento HTML in base al nome. Quando viene designato correttamente, il ERP viene visualizzato nel riquadro inferiore quando viene selezionato l'evento nel Visualizzatore eventi. La figura seguente illustra un ERP associato al monitoraggio intervallo IP (Internet Protocol).

![un ERP associato al monitoraggio intervallo IP](images/exview2.png)

## <a name="expert-events"></a>Eventi esperti

Gli eventi esperti sono identificati dal membro **EventIdent** di una struttura [**NMEVENTDATA**](nmeventdata.md) . Quando si scrive un esperto, è necessario determinare i valori **EventIdent** , che in genere sono numerati 1, 2, 3 e così via. Si supponga, ad esempio, che un esperto generi due eventi (**EventIdent1** e **EventIdent2**). Se si vuole che il Visualizzatore eventi visualizzi gli eventi separatamente, è necessario creare due documenti ERP distinti.

 

 



