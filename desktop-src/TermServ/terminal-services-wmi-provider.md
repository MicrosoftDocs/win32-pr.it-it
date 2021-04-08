---
title: Provider WMI Servizi Desktop remoto
description: Il provider WMI Servizi Desktop remoto fornisce accesso a livello di codice alle informazioni e alle impostazioni esposte dallo snap-in Microsoft Management Console (MMC) Servizi Desktop remoto Configuration/Connections.
ms.assetid: d205a3da-3f9a-4ee1-9c99-a39e9cce0a11
ms.tgt_platform: multiple
keywords:
- Servizi Desktop remoto Servizi Desktop remoto, provider WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25d947db18c0cde63bcb6c4c3954fc9811e0f0f1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104046907"
---
# <a name="remote-desktop-services-wmi-provider"></a>Provider WMI Servizi Desktop remoto

Il provider WMI Servizi Desktop remoto fornisce accesso a livello di codice alle informazioni e alle impostazioni esposte dallo snap-in Microsoft Management Console (MMC) Servizi Desktop remoto Configuration/Connections.

La DLL del provider viene caricata dal processo di gestione di Windows (Winmgmt.exe) quando un client effettua una richiesta al server. L'amministrazione è possibile utilizzando i metodi del provider. Il provider viene registrato sia come istanza sia come provider di metodi.

Il provider WMI Servizi Desktop remoto è stato implementato come provider dinamico derivato dalla classe di base del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) , ereditando tutte le proprietà e i metodi e una libreria a collegamento dinamico in-process.

Per ulteriori informazioni, vedere la [Servizi Desktop remoto riferimento al provider WMI](terminal-services-wmi-provider-reference.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Servizi Desktop remoto riferimento al provider WMI](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 