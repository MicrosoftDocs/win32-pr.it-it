---
description: Il Servizio Copia Shadow del volume (VSS) fornisce l'infrastruttura di sistema per l'esecuzione di applicazioni VSS in sistemi basati su Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: Servizio Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 274e1e561b702dc2e69782fa5e9c2b47e6ea6a23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751602"
---
# <a name="the-volume-shadow-copy-service"></a>Servizio Copia Shadow del volume

Il Servizio Copia Shadow del volume (VSS) fornisce l'infrastruttura di sistema per l'esecuzione di applicazioni VSS in sistemi basati su Windows.

Sebbene in gran parte trasparente per utenti e sviluppatori, VSS esegue le operazioni seguenti:

-   Coordina le attività di provider, writer e richiedenti nella creazione e nell'uso di copie shadow
-   Fornisce il provider di sistema predefinito
-   Implementa la funzionalità di driver di basso livello necessaria per il funzionamento di qualsiasi provider

Il Servizio viene avviato on demand, quindi, perché le operazioni del Servizio Copia Shadow del volume abbiano esito positivo, questo servizio deve essere abilitato.

 

 



