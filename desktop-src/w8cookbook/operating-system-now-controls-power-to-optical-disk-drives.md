---
title: Il sistema operativo ora controlla l'alimentazione alle unità disco ottico
description: Il sistema operativo ora controlla l'alimentazione alle unità disco ottico
ms.assetid: FDAE818F-742E-4E8C-9426-2AA86B42B0D9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5aee28a7606f022c877077dbe5477ede959dbdb
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "103730735"
---
# <a name="operating-system-now-controls-power-to-optical-disk-drives"></a>Il sistema operativo ora controlla l'alimentazione alle unità disco ottico

## <a name="platforms"></a>Piattaforme

**Client** -Windows 8  
**Server** : Windows Server 2012  


## <a name="description"></a>Descrizione

Nelle versioni precedenti di Windows, l'alimentazione dell'unità ottica non è stata gestita quando l'unità ottica non è in uso. A questo punto, se non è presente alcun supporto nell'unità disco ottico (dispari), il sistema operativo disattiva l'alimentazione dell'unità ottica. Questa funzionalità è denominata zero Power ODD (ZPODD). Questa funzionalità è applicabile solo alle unità ottiche che usano un connettore SATA (Serial Advanced Technology Attachment).

## <a name="manifestation"></a>Manifestazione

Non sono stati rilevati effetti negativi da questo nuovo comportamento. è tuttavia necessario tenerne conto perché potrebbe causare un comportamento imprevisto del software per la scrittura di contenuti multimediali.

## <a name="mitigation"></a>Strategia di riduzione del rischio

Per ripristinare lo stato always on, disattivare questa funzionalità nel registro di sistema. Il percorso assoluto del valore del registro di sistema è:

`HKLM\SYSTEM\CurrentControlSet\Services\cdrom\Parameters\ZeroPowerODDEnabled`

Il tipo è DWORD (32 bit) e se il valore è 0, ZPODD è disabilitato; Se è qualsiasi altro valore, ZPODD è abilitato.

## <a name="tests"></a>Test

Testare il software per la scrittura di contenuti multimediali per eventuali anomalie che si verificano a causa di questa nuova funzionalità. [Segnala a Microsoft](mailto:OptIssue@microsoft.com) eventuali problemi riscontrati con questa nuova funzionalità.

 

 




