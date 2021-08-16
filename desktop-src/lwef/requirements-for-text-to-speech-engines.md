---
title: Requisiti per i motori di sintesi vocale
description: Requisiti per i motori di sintesi vocale
ms.assetid: 21d19949-c9b4-4d9c-9684-6d15162f7a7d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3025be266d0aa40cd5a3bca6adb63e333310df444be7bd07e3a72b0f10b9c49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118746416"
---
# <a name="requirements-for-text-to-speech-engines"></a>Requisiti per i motori di sintesi vocale

\[Microsoft Agent è deprecato a Windows 7 e potrebbe non essere disponibile nelle versioni successive di Windows.\]

Il motore deve essere completamente conforme a SAPI 4.0. Inoltre, il motore deve supportare anche le interfacce SAPI seguenti per le notifiche di testo con tag e segnalibri. Queste interfacce consentono a Microsoft Agent di impostare l'output del testo su un fumetto di parole di un carattere e di sincronizzare la lingua del carattere (o equivalente) con le parole pronunciate.

-   [ITTSCentralW](ittscentralw.md)
-   [ITTSNotifySinkW](ittsnotifysinkw.md)
-   [ITTSBufNotifySinkW](ittsbufnotifysinkw.md)
-   [ITTSAttributesW](ittsattributesw.md)

 

 




