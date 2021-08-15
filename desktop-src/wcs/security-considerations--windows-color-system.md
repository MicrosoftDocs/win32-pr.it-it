---
title: Considerazioni sulla sicurezza Windows color system
description: Considerazioni sulla sicurezza Windows color system
ms.assetid: 9e8b7c38-3c4f-4537-a7e1-6ad0daa39497
keywords:
- Windows Sistema colori (WCS), sicurezza
- WCS (Windows Color System),sicurezza
- gestione dei colori delle immagini, sicurezza
- gestione dei colori, sicurezza
- sicurezza per Windows Color System (WCS)
- Color Management Module (CMM)
- CMM (Color Management Module)
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e710a0224c10d4f7cd7aa1565e88d00da539370974719129a37d735f11a29fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118444668"
---
# <a name="security-considerations-windows-color-system"></a>Considerazioni sulla sicurezza: Windows color system

In questo documento vengono fornite informazioni sulle considerazioni sulla sicurezza correlate alla gestione dei colori delle immagini. Questo documento non fornisce tutte le informazioni necessarie sui problemi di sicurezza, ma è possibile usarlo come punto di partenza e riferimento per questa area di tecnologia.

## <a name="non-microsoft-cmms-can-run-in-system-context"></a>I CCM non Microsoft possono essere eseguiti nel contesto di sistema

I moduli DIM (Color Management Modules) non Microsoft devono essere considerati come driver di stampante non Microsoft perché possono essere eseguiti in un contesto di sistema per le operazioni di stampa.
