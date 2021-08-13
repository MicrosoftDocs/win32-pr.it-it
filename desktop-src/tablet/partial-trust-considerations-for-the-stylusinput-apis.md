---
description: Panoramica dei problemi di attendibilità parziale e dell'API (Application Programming Interface) StylusInput.
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Considerazioni sull'attendibilità parziale per l'API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 596e8b50692ae09e9fbaf73f9254afbec8f29d6481a2dc3e27727beb27546441
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449351"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>Considerazioni sull'attendibilità parziale per l'API StylusInput

L'oggetto [**RealTimeStylus**](realtimestylus-class.md) che accetta il parametro *handle* richiede le autorizzazioni [UIPermissionWindow.AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag.UnmanagedCode,](/previous-versions/windows/) oltre alle autorizzazioni richieste dal costruttore che accetta il parametro *attachedControl.*

Per altre informazioni sui problemi di sicurezza e attendibilità, vedere [Sicurezza e attendibilità](security-and-trust.md).

 

 
