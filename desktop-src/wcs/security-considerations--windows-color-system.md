---
title: Considerazioni sulla sicurezza Windows Color System
description: Considerazioni sulla sicurezza Windows Color System
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- Windows Color System (WCS), sicurezza
- WCS (Windows Color System), sicurezza
- Gestione colori immagine, sicurezza
- gestione dei colori, sicurezza
- sicurezza per Windows Color System (WCS)
- Modulo di gestione colori (CMM)
- CMM (modulo di gestione colori)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef47ada0c233900f6e56a1e438d411a2ae84abd3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106320878"
---
# <a name="security-considerations-windows-color-system"></a>Considerazioni sulla sicurezza: sistema colori Windows

In questo documento vengono fornite informazioni sulle considerazioni relative alla sicurezza relative alla gestione dei colori delle immagini. Questo documento non fornisce tutte le informazioni necessarie per i problemi di sicurezza, ma è possibile usarlo come punto di partenza e come riferimento per questa area tecnologica.

## <a name="non-microsoft-cmms-can-run-in-system-context"></a>Il CMM non Microsoft può essere eseguito nel contesto di sistema

I moduli di gestione colori non Microsoft (CMM) devono essere considerati come driver della stampante non Microsoft, perché possono essere eseguiti in un contesto di sistema per le operazioni di stampa.
