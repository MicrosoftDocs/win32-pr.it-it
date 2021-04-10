---
description: Il Windows Installer determina se consentire la rimozione di un assembly Common Language Runtime in base a un elenco di client che mantiene indipendentemente dall'assembly.
ms.assetid: 3f83ad88-e6a4-484b-bcf5-8e2e65f1f41f
title: Rimozione di assembly dalla Global assembly cache
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47d50bc2856891c67952a27b27a27cf1cf2d1d65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104231537"
---
# <a name="removal-of-assemblies-from-the-global-assembly-cache"></a>Rimozione di assembly dalla Global assembly cache

Il Windows Installer determina se consentire la rimozione di un assembly Common Language Runtime in base a un elenco di client che mantiene indipendentemente dall'assembly. Il Windows Installer mantiene un bit pin per rappresentare Windows Installer client dell'assembly. Il programma di installazione aggiunge l'assembly per il primo client di Windows Installer e lo sblocca quando viene rimosso l'ultimo client Windows Installer. L'assembly gestisce un bit pin per ogni client di un assembly.

Il Windows Installer non è responsabile direttamente della rimozione fisica di Common Language Runtime assembly dal computer. Il programma di installazione Sblocca l'assembly quando viene rimosso l'ultimo client di Windows Installer. Se il Windows Installer è l'ultimo client dell'assembly, il Common Language Runtime fornisce l'opzione per forzare una pulizia sincrona dell'assembly. Il processo di pulizia è atomico e non è presente alcun provisioning per un "rollback" a questo punto. Quando l'utente ha avuto la possibilità di annullare l'installazione o la rimozione, tutti gli assembly di Common Language Runtime devono essere rilevati.

 

 



