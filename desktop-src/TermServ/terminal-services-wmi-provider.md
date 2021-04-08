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
# <a name="remote-desktop-services-wmi-provider"></a><span data-ttu-id="f5112-104">Provider WMI Servizi Desktop remoto</span><span class="sxs-lookup"><span data-stu-id="f5112-104">Remote Desktop Services WMI provider</span></span>

<span data-ttu-id="f5112-105">Il provider WMI Servizi Desktop remoto fornisce accesso a livello di codice alle informazioni e alle impostazioni esposte dallo snap-in Microsoft Management Console (MMC) Servizi Desktop remoto Configuration/Connections.</span><span class="sxs-lookup"><span data-stu-id="f5112-105">The Remote Desktop Services WMI provider provides programmatic access to the information and settings that are exposed by the Remote Desktop Services Configuration/Connections Microsoft Management Console (MMC) snap-in.</span></span>

<span data-ttu-id="f5112-106">La DLL del provider viene caricata dal processo di gestione di Windows (Winmgmt.exe) quando un client effettua una richiesta al server.</span><span class="sxs-lookup"><span data-stu-id="f5112-106">The provider DLL is loaded by the Windows Management process (Winmgmt.exe) when a client makes a request to the server.</span></span> <span data-ttu-id="f5112-107">L'amministrazione è possibile utilizzando i metodi del provider.</span><span class="sxs-lookup"><span data-stu-id="f5112-107">Administration is possible by using the provider methods.</span></span> <span data-ttu-id="f5112-108">Il provider viene registrato sia come istanza sia come provider di metodi.</span><span class="sxs-lookup"><span data-stu-id="f5112-108">The provider is registered as both an instance and a method provider.</span></span>

<span data-ttu-id="f5112-109">Il provider WMI Servizi Desktop remoto è stato implementato come provider dinamico derivato dalla classe di base del [**\_ servizio Win32**](/windows/desktop/CIMWin32Prov/win32-service) , ereditando tutte le proprietà e i metodi e una libreria a collegamento dinamico in-process.</span><span class="sxs-lookup"><span data-stu-id="f5112-109">The Remote Desktop Services WMI provider has been implemented as a dynamic provider derived from the [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service) base class, inheriting all of its properties and methods, and an in-process dynamic link library.</span></span>

<span data-ttu-id="f5112-110">Per ulteriori informazioni, vedere la [Servizi Desktop remoto riferimento al provider WMI](terminal-services-wmi-provider-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f5112-110">For more information, see the [Remote Desktop Services WMI Provider reference](terminal-services-wmi-provider-reference.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f5112-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f5112-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5112-112">Servizi Desktop remoto riferimento al provider WMI</span><span class="sxs-lookup"><span data-stu-id="f5112-112">Remote Desktop Services WMI Provider Reference</span></span>](terminal-services-wmi-provider-reference.md)
</dt> </dl>

 

 