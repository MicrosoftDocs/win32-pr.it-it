---
title: Formato driver installabile
description: Formato driver installabile
ms.assetid: 4573567e-237d-47f9-9510-31d01326205f
keywords:
- driver installabili, formati
- driver installabili, funzione DriverProc
- driver installabili, messaggi
- messaggi del driver
- formati dei driver
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c02f6bb2515d1f182146b84b7f0b971fa4b73fe2e2caf5abf63dfd4ddb272df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118140790"
---
# <a name="installable-driver-format"></a>Formato driver installabile

Ogni driver installabile esporta una [funzione DriverProc.](/windows/win32/api/mmiscapi/nc-mmiscapi-driverproc) Questa funzione comune del punto di ingresso riceve i *messaggi del driver* dal sistema che indirizzano il driver a eseguire azioni o fornire informazioni. Il sistema invia messaggi del driver alla funzione **DriverProc** quando un'applicazione o una DLL apre o chiude il driver o richiede l'invio di un messaggio al driver. La **funzione DriverProc** elabora il messaggio o lo passa al gestore di messaggi predefinito, la [funzione DefDriverProc.](/windows/win32/api/mmiscapi/nf-mmiscapi-defdriverproc) In entrambi i casi, **DriverProc** deve restituire un valore che indica se l'azione richiesta ha avuto esito positivo.

 

 