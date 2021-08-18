---
title: Funzioni di callback
description: Funzioni di callback
ms.assetid: d96e93e5-ebc9-4ad4-aaec-dcc4197a3fc5
keywords:
- driver installabili, funzioni di callback
- driver installabili, funzione DriverCallback
- driver installabili, eventi
- Funzione DriverCallback
- DRV_OPEN messaggio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fabb833b0aa3adef444f8242d540eb48dcbe381ebc5c7f62c6dedc0d5e9160e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786201"
---
# <a name="callback-functions"></a>Funzioni di callback

I driver installabili possono notificare all'applicazione, alla finestra o all'attività che ha aperto l'istanza specificata sugli eventi usando la [funzione DriverCallback.](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) Questa funzione offre al driver i mezzi per restituire informazioni a un'applicazione o a una DLL continuando a elaborare una richiesta.

Se un driver supporta le funzioni di callback, l'applicazione o la DLL che apre l'istanza deve fornire un valore che sia l'indirizzo di una funzione di callback, un handle di finestra o un handle di attività. Questo valore e un flag che identificano il tipo del valore vengono in genere passati in una struttura a cui punta il secondo parametro del messaggio [**DRV \_ OPEN.**](drv-open.md)

 

 