---
description: Il Servizio Copia Shadow del volume (VSS) fornisce l'infrastruttura di sistema per l'esecuzione di applicazioni VSS Windows sistemi basati su Windows.
ms.assetid: 237b2729-1e9b-4d0e-9c59-990e047a0360
title: Oggetto Servizio Copia Shadow del volume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f71e21ba0f20eaa0f3723cd0da6cb3efb89bae027678d154ab8b5b5568532ac8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119866241"
---
# <a name="the-volume-shadow-copy-service"></a>Oggetto Servizio Copia Shadow del volume

Il Servizio Copia Shadow del volume (VSS) fornisce l'infrastruttura di sistema per l'esecuzione di applicazioni VSS Windows sistemi basati su Windows.

Anche se in gran parte trasparente per gli utenti e gli sviluppatori, VSS esegue le operazioni seguenti:

-   Coordina le attività di provider, writer e richiedenti nella creazione e nell'uso di copie shadow
-   Fornisce il provider di sistema predefinito
-   Implementa le funzionalità dei driver di basso livello necessarie per il funzionamento di qualsiasi provider

Il Servizio viene avviato on demand, quindi, perché le operazioni del Servizio Copia Shadow del volume abbiano esito positivo, questo servizio deve essere abilitato.

 

 



