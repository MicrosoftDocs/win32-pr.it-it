---
description: Un provider di servizi multimediali (MSP) consente a un'applicazione di controllare i supporti per un meccanismo di trasporto specifico.
ms.assetid: f886380f-d970-4511-bf71-fb1eb767e4f4
title: Provider di servizi multimediali
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3dd78f5ff4a13da4365f99bd2cb539738b6f3fd6
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320600"
---
# <a name="media-service-providers"></a><span data-ttu-id="57ae0-103">Provider di servizi multimediali</span><span class="sxs-lookup"><span data-stu-id="57ae0-103">Media Service Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="57ae0-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="57ae0-104">Purpose</span></span>

<span data-ttu-id="57ae0-105">Un provider di servizi multimediali (MSP) consente a un'applicazione di controllare i supporti per un meccanismo di trasporto specifico.</span><span class="sxs-lookup"><span data-stu-id="57ae0-105">A media service provider (MSP) enables an application to control media for a particular transport mechanism.</span></span> <span data-ttu-id="57ae0-106">Un MSP è sempre associato a un provider di servizi di telefonia (TSP).</span><span class="sxs-lookup"><span data-stu-id="57ae0-106">An MSP is always paired with a Telephony Service Provider (TSP).</span></span>

<span data-ttu-id="57ae0-107">Media Service Provider Interface (MSPI) è un set di interfacce e metodi implementati da un MSP per consentire a un'applicazione di controllare il trasporto multimediale durante una sessione di comunicazione.</span><span class="sxs-lookup"><span data-stu-id="57ae0-107">The Media Service Provider Interface (MSPI) is a set of interfaces and methods implemented by an MSP to allow an application control over media transport during a communications session.</span></span> <span data-ttu-id="57ae0-108">Un MSP gestisce i meccanismi specifici del dispositivo e specifici del protocollo necessari per applicare questi controlli e comunica con il relativo TSP associato o un'applicazione tramite l'uso dei metodi forniti in MSPI.</span><span class="sxs-lookup"><span data-stu-id="57ae0-108">An MSP handles the device-specific and protocol-specific mechanisms required to enact these controls, and communicates with its paired TSP or an application through use of the methods provided in the MSPI.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="57ae0-109">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="57ae0-109">Developer audience</span></span>

<span data-ttu-id="57ae0-110">È necessaria una certa familiarità con COM.</span><span class="sxs-lookup"><span data-stu-id="57ae0-110">Familiarity with COM is required.</span></span> <span data-ttu-id="57ae0-111">L'esperienza di sviluppo con le telecomunicazioni o altre applicazioni di telefonia è utile, ma non necessaria.</span><span class="sxs-lookup"><span data-stu-id="57ae0-111">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="57ae0-112">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="57ae0-112">Run-time requirements</span></span>

<span data-ttu-id="57ae0-113">MSPI consente lo sviluppo di provider di servizi multimediali per determinati protocolli o dispositivi in esecuzione su sistemi operativi Windows Server 2003, Windows XP e Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="57ae0-113">MSPI enables development of media service providers for particular protocols or devices running on Windows Server 2003 operating systems, Windows XP, and Windows 2000.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="57ae0-114">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="57ae0-114">In this section</span></span>



| <span data-ttu-id="57ae0-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="57ae0-115">Topic</span></span>                                                                       | <span data-ttu-id="57ae0-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="57ae0-116">Description</span></span>                                                           |
|-----------------------------------------------------------------------------|-----------------------------------------------------------------------|
| [<span data-ttu-id="57ae0-117">Overview</span><span class="sxs-lookup"><span data-stu-id="57ae0-117">Overview</span></span>](about-the-media-service-provider-msp-.md)<br/>            | <span data-ttu-id="57ae0-118">Informazioni generali sull'architettura e i componenti MSP.</span><span class="sxs-lookup"><span data-stu-id="57ae0-118">General information about MSP architecture and components.</span></span><br/> |
| [<span data-ttu-id="57ae0-119">Riferimento</span><span class="sxs-lookup"><span data-stu-id="57ae0-119">Reference</span></span>](media-service-provider-interface-mspi-reference.md)<br/> | <span data-ttu-id="57ae0-120">Documentazione per le interfacce MSPI.</span><span class="sxs-lookup"><span data-stu-id="57ae0-120">Documentation for the MSPI interfaces.</span></span><br/>                     |



 

## <a name="related-topics"></a><span data-ttu-id="57ae0-121">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="57ae0-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="57ae0-122">Panoramica della telefonia Microsoft</span><span class="sxs-lookup"><span data-stu-id="57ae0-122">Microsoft Telephony Overview</span></span>](microsoft-telephony-overview.md)
</dt> <dt>

[<span data-ttu-id="57ae0-123">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="57ae0-123">TAPI 3.1</span></span>](tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="57ae0-124">Provider di servizi di telefonia</span><span class="sxs-lookup"><span data-stu-id="57ae0-124">Telephony Service Providers</span></span>](./telephony-service-providers-start-page.md)
</dt> </dl>

 

