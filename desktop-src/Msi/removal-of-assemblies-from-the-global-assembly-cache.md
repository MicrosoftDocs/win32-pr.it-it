---
description: Il Windows installer determina se consentire la rimozione di un assembly di Common Language Runtime in base a un elenco di client che mantiene indipendentemente dall'assembly.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Rimozione di assembly dalla Global Assembly Cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7490142c1d3bd375b79513685198571b0638fbe16e03b99b39f59ec5ec9a9219
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119327551"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a>Rimozione di assembly dalla Global Assembly Cache

Il Windows installer determina se consentire la rimozione di un assembly di Common Language Runtime in base a un elenco di client che mantiene indipendentemente dall'assembly. Il Windows installer mantiene un bit di blocco per rappresentare Windows client del programma di installazione dell'assembly. Il programma di installazione aggiunge l'assembly per il primo client Windows Installer e lo sblocca quando viene rimosso l'Windows del programma di installazione. L'assembly mantiene un bit di blocco per ogni client di un assembly.

Il Windows installer non è direttamente responsabile della rimozione fisica degli assembly di Common Language Runtime dal computer. Il programma di installazione sblocca l'assembly quando l'Windows client del programma di installazione viene rimosso. Se il Windows Installer è l'ultimo client dell'assembly, Common Language Runtime offre la possibilità di forzare una pulizia sincrona dell'assembly. Il processo di pulizia è atomico e non è disponibile alcun provisioning per un "rollback" a questo punto. Tutti gli assembly di Common Language Runtime devono essere annullati dopo che l'utente ha avuto la possibilità di annullare l'installazione o la rimozione.

 

 



