---
title: Server d'inoltro
description: Il server d'inoltro è il componente in modalità kernel del router responsabile dell'inoltro dei dati da un'interfaccia del router all'altra.
ms.assetid: 69cdbefa-9137-48cb-940a-badfb3f4f231
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5011d340b444c9d0be5b26ee5449f041bb7419fd4a52f8a983ce2b85d9b106f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119674021"
---
# <a name="forwarder"></a>Server d'inoltro

Il server d'inoltro è il componente in modalità kernel del router responsabile dell'inoltro dei dati da un'interfaccia del router all'altra. Il server d'inoltro decide anche se un pacchetto è destinato al recapito locale, se è destinato a essere inoltrato da un'altra interfaccia o da entrambi.

Esistono due server d'inoltro in modalità kernel: unicast e multicast.

Il gestore di router ottiene le route migliori per tutte le destinazioni dal gestore tabelle di routing. Queste route vengono passate al server d'inoltro unicast. Il server d'inoltro unicast usa queste route per eseguire l'inoltro effettivo dei dati unicast. In questo modo, il server d'inoltro unicast mantiene una cache delle route migliori nella vista unicast della tabella di routing.

Il gestore di gruppi multicast usa le informazioni della vista multicast della tabella di routing per aggiungere voci di inoltro multicast al server d'inoltro multicast.

 

 




