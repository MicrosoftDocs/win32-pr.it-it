---
description: I servizi HTTP di Microsoft Windows (WinHTTP) forniscono agli sviluppatori un Application Programming Interface client HTTP (API) per inviare richieste tramite il protocollo HTTP ad altri server HTTP.
ms.assetid: 354ab65d-5e46-451d-b36b-2f8166a1a048
title: Servizi HTTP di Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f03a3204257410e4db0182724ab63743116f021
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307094"
---
# <a name="windows-http-services"></a><span data-ttu-id="a1c3a-103">Servizi HTTP di Windows</span><span class="sxs-lookup"><span data-stu-id="a1c3a-103">Windows HTTP Services</span></span>

## <a name="purpose"></a><span data-ttu-id="a1c3a-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="a1c3a-104">Purpose</span></span>

<span data-ttu-id="a1c3a-105">I servizi HTTP di Microsoft Windows (WinHTTP) forniscono agli sviluppatori un Application Programming Interface client HTTP (API) per inviare richieste tramite il protocollo HTTP ad altri server HTTP.</span><span class="sxs-lookup"><span data-stu-id="a1c3a-105">Microsoft Windows HTTP Services (WinHTTP) provides developers with an HTTP client application programming interface (API) to send requests through the HTTP protocol to other HTTP servers.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="a1c3a-106">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="a1c3a-106">Where applicable</span></span>

<span data-ttu-id="a1c3a-107">WinHTTP supporta applicazioni client desktop, servizi Windows e applicazioni basate su Windows Server.</span><span class="sxs-lookup"><span data-stu-id="a1c3a-107">WinHTTP supports desktop client applications, Windows services, and Windows server-based applications.</span></span>

<span data-ttu-id="a1c3a-108">Per altre informazioni su come usare WinHTTP per le applicazioni basate su Microsoft .NET Framework, vedere l' [API WinHttpHandler](/dotnet/api/system.net.http?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="a1c3a-108">For more information on how to use WinHTTP for applications built on the Microsoft .NET Framework, see the [WinHttpHandler API](/dotnet/api/system.net.http?view=netframework-4.8)</span></span>

## <a name="developer-audience"></a><span data-ttu-id="a1c3a-109">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="a1c3a-109">Developer audience</span></span>

<span data-ttu-id="a1c3a-110">WinHTTP offre un componente di automazione (API) di C/C++ Application Programming Interface e un Component Object Model (COM) appropriato per l'utilizzo in applicazioni basate su Active Server Pages (ASP).</span><span class="sxs-lookup"><span data-stu-id="a1c3a-110">WinHTTP offers both a C/C++ application programming interface (API) and a Component Object Model (COM) automation component suitable for use in Active Server Pages (ASP) based applications.</span></span>

<span data-ttu-id="a1c3a-111">Una conoscenza di base del protocollo HTTP è importante per l'uso di entrambe le interfacce.</span><span class="sxs-lookup"><span data-stu-id="a1c3a-111">A basic understanding of the HTTP protocol is important to use either interface.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="a1c3a-112">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="a1c3a-112">Run-time requirements</span></span>

<span data-ttu-id="a1c3a-113">WinHTTP 5,1 offre miglioramenti rispetto alla versione 5,0.</span><span class="sxs-lookup"><span data-stu-id="a1c3a-113">WinHTTP 5.1 offers improvements over version 5.0.</span></span> <span data-ttu-id="a1c3a-114">È incluso nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a1c3a-114">It is included in the operating system.</span></span> <span data-ttu-id="a1c3a-115">Per ulteriori informazioni sulle nuove funzionalità, vedere Novità di [WinHTTP 5,1](what-s-new-in-winhttp-5-1.md) e novità di [Windows Server 2008 e Windows Vista](what-s-new-in-windows-longhorn.md).</span><span class="sxs-lookup"><span data-stu-id="a1c3a-115">For more information about new features, see [What's New in WinHTTP 5.1](what-s-new-in-winhttp-5-1.md) and [What's New in Windows Server 2008 and Windows Vista](what-s-new-in-windows-longhorn.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a1c3a-116">Il download di WinHTTP 5,0 non è più disponibile.</span><span class="sxs-lookup"><span data-stu-id="a1c3a-116">The WinHTTP 5.0 download is no longer available.</span></span> <span data-ttu-id="a1c3a-117">A partire dal 1 ° ottobre 2004, Microsoft ha rimosso il download di WinHTTP 5,0 SDK da MSDN e ha terminato il supporto tecnico per la versione 5,0.</span><span class="sxs-lookup"><span data-stu-id="a1c3a-117">As of October 1, 2004, Microsoft removed the WinHTTP 5.0 SDK download from MSDN and terminated product support for version 5.0.</span></span>

 

## <a name="in-this-section"></a><span data-ttu-id="a1c3a-118">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="a1c3a-118">In this section</span></span>

-   [<span data-ttu-id="a1c3a-119">Informazioni su WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a1c3a-119">About WinHTTP</span></span>](about-winhttp.md)
-   [<span data-ttu-id="a1c3a-120">Uso di WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a1c3a-120">Using WinHTTP</span></span>](using-winhttp.md)
-   [<span data-ttu-id="a1c3a-121">Riferimento a WinHTTP</span><span class="sxs-lookup"><span data-stu-id="a1c3a-121">WinHTTP Reference</span></span>](winhttp-reference.md)

 

 
