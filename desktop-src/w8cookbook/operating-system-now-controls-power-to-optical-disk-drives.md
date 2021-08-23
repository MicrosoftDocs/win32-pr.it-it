---
title: Il sistema operativo controlla ora l'alimentazione alle unità disco ottico
description: Il sistema operativo controlla ora l'alimentazione alle unità disco ottico
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc43ad47f6a9468c2850627f267d433bfa346d059231d5daa91e860d5a793aef
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119593801"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a>Il sistema operativo controlla ora l'alimentazione alle unità disco ottico

## <a name="platforms"></a>Piattaforme

**Client** : Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

Nelle versioni precedenti di Windows, l'alimentazione all'unità ottico non era gestita quando l'unità ottico non era in uso. Se nell'unità disco ottico (ODD) non è presente alcun supporto, il sistema operativo disattiva l'alimentazione sull'unità ottico. Questa funzionalità è denominata ZERO POWER ODD (ZPODD). La funzionalità è applicabile solo alle unità ottiche che usano un connettore SATA (Serial Advanced Technology Attachment).

## <a name="manifestation"></a>Manifestazione

Non sono stati rilevati effetti negativi da questo nuovo comportamento. Tuttavia, è necessario tenere presente questo aspetto perché può causare un comportamento imprevisto del software di scrittura di contenuti multimediali.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Per ripristinare lo stato always on, disattivare questa funzionalità nel Registro di sistema. Il percorso assoluto del valore del Registro di sistema è:

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

Il tipo è DWORD (32 bit) e, se il valore è 0, ZPODD è disabilitato. Se si tratta di qualsiasi altro valore, ZPODD è abilitato.

## <a name="tests"></a>Test

Testare il software di scrittura multimediale per individuare eventuali anomalie che si verificano a causa di questa nuova funzionalità. Informare [Microsoft](mailto:OptIssue@microsoft.com) di eventuali problemi che si verificano con questa nuova funzionalità.

 

 




