---
title: Esecuzione di una chiamata di procedura remota
description: Dopo che il programma client di applicazioni distribuite che usa handle di associazione espliciti ha un handle di associazione, può eseguire procedure remote.
ms.assetid: f424bb01-e562-49eb-abaf-cc2d76a6ad8f
keywords:
- Chiamata di procedura remota RPC, attività, esecuzione di una chiamata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8218fd99e11c65f15dbbe7a56c2ece1b93720839498352d610312a0f66f95bc5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020081"
---
# <a name="making-a-remote-procedure-call"></a>Esecuzione di una chiamata di procedura remota

Dopo che il programma client di applicazioni distribuite che usa handle di associazione espliciti ha un handle di associazione, può eseguire procedure remote.

Microsoft RPC offre anche handle di associazione personalizzati, handle di associazione impliciti e handle di associazione automatici. Questi handle di associazione offrono programmi client e server diversi livelli di controllo sul processo di esecuzione di procedure remote. Per informazioni dettagliate sui diversi tipi di handle e sulla flessibilità offerta, vedere [Associazione e handle](binding-and-handles.md).

Per eseguire la chiamata di routine in modalità remota, chiamare la funzione stub sul lato client nello stesso modo in cui viene chiamata qualsiasi funzione C.

 

 




