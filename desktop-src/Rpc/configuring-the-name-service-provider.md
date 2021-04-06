---
title: Configurazione del provider di servizi dei nomi
description: Se l'applicazione distribuita registra l'interfaccia con un servizio dei nomi, sia il client che il server devono utilizzare lo stesso servizio nome.
ms.assetid: a3f201e1-1a01-4794-9026-05e51a96afc0
keywords:
- RPC (Remote Procedure Call), attività, configurazione del provider di servizi nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b7a44ec9a1c83eb7c37f10caae6ca3870679bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044694"
---
# <a name="configuring-the-name-service-provider"></a><span data-ttu-id="19ce2-104">Configurazione del provider di servizi dei nomi</span><span class="sxs-lookup"><span data-stu-id="19ce2-104">Configuring the Name Service Provider</span></span>

<span data-ttu-id="19ce2-105">Se l'applicazione distribuita registra l'interfaccia con un servizio dei nomi, sia il client che il server devono utilizzare lo stesso servizio nome.</span><span class="sxs-lookup"><span data-stu-id="19ce2-105">If your distributed application registers its interface with a name service, both the client and server must be using the same name service.</span></span> <span data-ttu-id="19ce2-106">Microsoft RPC interagisce con Microsoft Locator e con qualsiasi provider di servizi dei nomi (NSP) che aderisce a Microsoft RPC Name Service Interface (NSI), ad esempio il servizio directory di celle DCE a cui si accede tramite il daemon del servizio nome di Digital Equipment Corporation (NSID).</span><span class="sxs-lookup"><span data-stu-id="19ce2-106">Microsoft RPC interoperates with Microsoft Locator and any name service provider (NSP) that adheres to the Microsoft RPC name service interface (NSI)—for example, the DCE Cell Directory Service accessed through Digital Equipment Corporation's name service daemon (NSID).</span></span> <span data-ttu-id="19ce2-107">Microsoft Locator, progettato per l'uso negli ambienti Windows, è il provider di servizi dei nomi predefinito.</span><span class="sxs-lookup"><span data-stu-id="19ce2-107">Microsoft Locator, which is designed for use in Windows environments, is the default name service provider.</span></span>

<span data-ttu-id="19ce2-108">In questa sezione viene illustrata l'installazione e la configurazione dei provider di servizi dei nomi:</span><span class="sxs-lookup"><span data-stu-id="19ce2-108">This section presents a discussion of installing and configuring name service providers:</span></span>

-   [<span data-ttu-id="19ce2-109">Configurazione del servizio nome</span><span class="sxs-lookup"><span data-stu-id="19ce2-109">Configuring the Name Service</span></span>](configuring-the-name-service-for-windows-xp-windows-2000-or-windows-nt.md)
-   [<span data-ttu-id="19ce2-110">Configurazione del servizio nome per Windows 95</span><span class="sxs-lookup"><span data-stu-id="19ce2-110">Configuring the Name Service for Windows 95</span></span>](configuring-the-name-service-for-windows-95.md)
-   [<span data-ttu-id="19ce2-111">Configurazione del servizio nome per Windows 3. x o MS-DOS</span><span class="sxs-lookup"><span data-stu-id="19ce2-111">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>](configuring-the-name-service-for-windows-3-x-or-ms-dos.md)
-   [<span data-ttu-id="19ce2-112">Avvio e arresto di Microsoft Locator</span><span class="sxs-lookup"><span data-stu-id="19ce2-112">Starting and Stopping Microsoft Locator</span></span>](starting-and-stopping-microsoft-locator.md)

 

 




