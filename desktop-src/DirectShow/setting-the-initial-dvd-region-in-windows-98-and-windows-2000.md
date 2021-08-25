---
description: Impostazione dell'area DVD iniziale
ms.assetid: b8238cb4-a101-4998-866f-4cf9ebd5d277
title: Impostazione dell'area DVD iniziale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7bf019c7d5ddae8efb257435e1b23037575a37f809ef012190b49c619cc3211
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102321"
---
# <a name="setting-the-initial-dvd-region"></a>Impostazione dell'area DVD iniziale

È responsabilità del produttore del sistema selezionare un'area DVD iniziale per l'unità DVD nei PC.

> [!Note]  
> Per impostare l'area è possibile usare solo dischi crittografati.

 

### <a name="windows-2000-and-later"></a>Windows 2000 e versioni successive

A partire Windows 2000, l'area DVD predefinita viene selezionata in base alle impostazioni locali per cui è configurato il computer. Windows 2000 imposta sempre l'area iniziale per un'unità DVD usando questa area predefinita e l'area del disco, se nell'unità è presente un disco. Il produttore del sistema non deve eseguire alcun operazione per impostare l'area iniziale per le unità DVD Windows 2000 o versioni successive.

Per le unità RPC1, se non è presente alcun disco nell'unità durante l'avvio, l'area predefinita viene impostata solo in base alle impostazioni locali del computer. Se durante l'avvio è presente un disco DVD nell'unità, l'area predefinita viene selezionata come area dell'unità, purché corrisponda a un'area del disco. in caso contrario, l'area più bassa del disco viene selezionata come area iniziale dell'unità. L'utente (o il produttore del sistema) ha una modifica rimanente consentita, nel caso in cui il valore predefinito non fosse corretto.

Per le unità RPC2, se durante il processo di installazione Windows 2000 rileva che l'unità non ha alcuna area impostata, tenterà di selezionare un'area come indicato sopra, ma solo se nell'unità è presente un disco. Le unità RPC1 sceglieranno l'area senza dischi nell'unità. Una volta impostata un'area per le unità RPC2, non viene modificata automaticamente da una nuova installazione o da un'installazione pulita del sistema operativo.

L'OEM può impostare una chiave del Registro di sistema contenente l'area DVD predefinita per il sistema. Al primo avvio, l'area dell'unità verrà impostata su questo valore. La chiave del Registro di Windows 2000 e versioni successive è HKLM \\ System \\ CurrentControlSet \\ Control Class \\ \\ <CDROM GUID> \\ <instance number> \\ DefaultDVDRegion(binary) .

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Supporto delle modifiche all'area DVD in Windows](dvd-region-change-support-in-windows.md)
</dt> </dl>

 

 



