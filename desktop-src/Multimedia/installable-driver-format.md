---
title: Formato driver installabile
description: Formato driver installabile
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- driver installabili, formati
- driver installabili, funzione DriverProc
- driver installabili, messaggi
- messaggi driver
- formati di driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86fbbdcb8a49184dee6e9cf13c9f434506b1b48f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337238"
---
# <a name="installable-driver-format"></a>Formato driver installabile

Ogni driver installabile esporta una funzione [DriverProc](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) . Questa funzione di punto di ingresso comune riceve *i messaggi del driver* dal sistema che indirizzano il driver a eseguire azioni o fornire informazioni. Il sistema invia messaggi di driver alla funzione **DriverProc** quando un'applicazione o una DLL apre o chiude il driver o richiede che un messaggio venga inviato al driver. La funzione **DriverProc** elabora il messaggio o passa il messaggio al gestore di messaggi predefinito, ovvero la funzione [DefDriverProc](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) . In entrambi i casi, **DriverProc** deve restituire un valore che indica se l'azione richiesta è stata eseguita correttamente.

 

 