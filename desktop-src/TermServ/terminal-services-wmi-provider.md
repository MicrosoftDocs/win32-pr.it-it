---
title: Servizi Desktop remoto provider WMI
description: Il Servizi Desktop remoto WMI fornisce l'accesso a livello di codice alle informazioni e alle impostazioni esposte dallo snap-in Servizi Desktop remoto Configuration/Connections Microsoft Management Console (MMC).
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto , provider WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ec4ed84dee9b2521c392b8b39ee1297121a85e1c4f8ad41f7d96d0d73042a5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869601"
---
# <a name="remote-desktop-services-wmi-provider"></a>Servizi Desktop remoto provider WMI

Il Servizi Desktop remoto WMI fornisce l'accesso a livello di codice alle informazioni e alle impostazioni esposte dallo snap-in Servizi Desktop remoto Configuration/Connections Microsoft Management Console (MMC).

La DLL del provider viene caricata dal Windows management (Winmgmt.exe) quando un client effettua una richiesta al server. L'amministrazione è possibile usando i metodi del provider. Il provider viene registrato sia come istanza che come provider di metodi.

Il Servizi Desktop remoto WMI è stato implementato come provider dinamico derivato dalla classe di base del servizio [**Win32, \_**](/windows/desktop/CIMWin32Prov/win32-service) ereditando tutte le proprietà e i metodi e una libreria a collegamento dinamico in-process.

Per altre informazioni, vedere le informazioni di [Servizi Desktop remoto riferimento al provider WMI.](terminal-services-wmi-provider-reference.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi Desktop remoto riferimento al provider WMI](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 