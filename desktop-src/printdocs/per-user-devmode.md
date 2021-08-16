---
description: Un utente può specificare le impostazioni predefinite del documento per una stampante. Questa operazione viene chiamata DEVMODE per utente perché influisce solo sulle impostazioni predefinite per un determinato utente e le informazioni per ogni stampante vengono definite in una struttura DEVMODE separata.
ms.assetid: f791f847-c31e-4a06-93cb-49117d8f0cb8
title: Per-User DEVMODE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b5e9fd2872d055dba6d04f060e6d2e581e461fd20ddc418f643d09170cda31d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118731926"
---
# <a name="per-user-devmode"></a>Per-User DEVMODE

Un utente può specificare le impostazioni predefinite del documento per una stampante. Questa operazione viene chiamata *DEVMODE per* utente perché influisce solo sulle impostazioni predefinite per un determinato utente e le informazioni per ogni stampante vengono definite in una [**struttura DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea) separata.

Per impostare il valore DEVMODE per utente, chiamare [**SetPrinter**](setprinter.md) con la struttura [**PRINTER INFO \_ \_ 2**](printer-info-2.md) o [**PRINTER INFO \_ \_ 9.**](printer-info-9.md) Per reimpostare devMODE per utente sul valore [**DEVMODE**](/windows/win32/api/wingdi/ns-wingdi-devmodea)predefinito globale, chiamare **SetPrinter** con la [**struttura PRINTER INFO \_ \_ 8.**](printer-info-8.md)

 

 



