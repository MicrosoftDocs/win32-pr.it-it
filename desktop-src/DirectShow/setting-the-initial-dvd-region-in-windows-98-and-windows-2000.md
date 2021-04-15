---
description: Impostazione dell'area DVD iniziale
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Impostazione dell'area DVD iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d3f5181b804a9d83c04eed0abc70095bf9f1cf2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520386"
---
# <a name="setting-the-initial-dvd-region"></a>Impostazione dell'area DVD iniziale

È responsabilità del produttore del sistema selezionare un'area DVD iniziale per l'unità DVD nei PC.

> [!Note]  
> Per impostare l'area è possibile utilizzare solo dischi crittografati.

 

### <a name="windows-2000-and-later"></a>Windows 2000 e versioni successive

A partire da Windows 2000, l'area DVD predefinita viene selezionata in base alle impostazioni locali per cui è configurato il computer. Windows 2000 imposta sempre l'area iniziale per un'unità DVD che usa questa area predefinita e l'area del disco, se è presente un disco nell'unità. Il produttore del sistema non deve eseguire alcuna operazione per impostare l'area iniziale per le unità DVD di Windows 2000 o versioni successive.

Per le unità RPC1, se non è presente alcun disco nell'unità durante l'avvio, l'area predefinita viene impostata solo in base alle impostazioni locali del computer. Se è presente un disco DVD nell'unità durante l'avvio, l'area predefinita viene selezionata come area dell'unità, purché corrisponda a un'area del disco; in caso contrario, viene selezionata l'area minima del disco come area iniziale dell'unità. All'utente (o produttore del sistema) è consentita una modifica rimanente, nel caso in cui il valore predefinito non sia corretto.

Per le unità RPC2, se durante il processo di installazione Windows 2000 rileva che nell'unità non è impostata alcuna area, tenterà di selezionare un'area come sopra, ma solo se è presente un disco nell'unità. (Le unità RPC1 scelgono l'area senza disco nell'unità). Una volta impostata un'area per le unità RPC2, non viene modificata automaticamente da una nuova installazione o da un'installazione pulita del sistema operativo.

L'OEM può impostare una chiave del registro di sistema contenente l'area DVD predefinita per il sistema. Al primo avvio, l'area dell'unità verrà impostata su questo valore. La chiave del registro di sistema in Windows 2000 e versioni successive è HKLM \\ System \\ CurrentControlSet \\ Control \\ Class \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion (Binary).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto delle modifiche all'area DVD in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



