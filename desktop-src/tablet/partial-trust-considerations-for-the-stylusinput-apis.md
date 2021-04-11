---
description: Panoramica dei problemi di attendibilità parziale e del Application Programming Interface di StylusInput (API).
ms.assetid: 32c26632-03f4-4f21-8c67-ebf38b67d251
title: Considerazioni sull'attendibilità parziale per l'API StylusInput
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ceda5edfb2e4133bb0fcb3d260ff1e13f9fdb521
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104232707"
---
# <a name="partial-trust-considerations-for-the-stylusinput-api"></a>Considerazioni sull'attendibilità parziale per l'API StylusInput

Il metodo [**RealTimeStylus**](realtimestylus-class.md) che accetta il parametro *handle* richiede le autorizzazioni [UIPermissionWindow. AllWindows](/dotnet/api/system.security.permissions.uipermissionwindow?view=dotnet-plat-ext-3.1&preserve-view=true) e [SecurityPermissionFlag. UnmanagedCode](/previous-versions/windows/) , oltre alle autorizzazioni richieste dal costruttore che accetta il parametro *attachedControl* .

Per ulteriori informazioni sui problemi di sicurezza e di attendibilità, vedere [sicurezza e attendibilità](security-and-trust.md).

 

 
