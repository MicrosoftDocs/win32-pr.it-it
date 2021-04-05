---
title: Funzioni di callback
description: Funzioni di callback
ms.assetid: d96e93e5-ebc9-4ad4-aaec-dcc4197a3fc5
keywords:
- driver installabili, funzioni di callback
- driver installabili, funzione DriverCallback
- driver installabili, eventi
- DriverCallback (funzione)
- Messaggio DRV_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7e23f933567d125dd07f81047ea8868c12f41ac
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872481"
---
# <a name="callback-functions"></a>Funzioni di callback

I driver installabili possono notificare all'applicazione, alla finestra o all'attività che ha aperto l'istanza specificata informazioni sugli eventi tramite la funzione [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) . Questa funzione fornisce al driver i mezzi per restituire informazioni a un'applicazione o a una DLL continuando a elaborare una richiesta.

Se un driver supporta le funzioni di callback, l'applicazione o la DLL che apre l'istanza deve fornire un valore che corrisponde all'indirizzo di una funzione di callback, a un handle di finestra o a un handle di attività. Questo valore e un flag che identifica il tipo del valore vengono in genere passati in una struttura a cui punta il secondo parametro del [**messaggio \_ aperto DRV**](drv-open.md) .

 

 