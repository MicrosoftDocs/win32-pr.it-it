---
title: Informazioni su Windows Connect Now
description: Windows Connect Now (WCN) fornisce un meccanismo semplice e sicuro per i dispositivi e i punti di accesso alla rete, ad esempio stampanti, fotocamere e PC, per la connessione e lo scambio delle impostazioni.
ms.assetid: 5c654800-e58b-4a94-b7a6-9a603f540603
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0118c6a053c480a36138f8dae850ee0862501944
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104118295"
---
# <a name="about-windows-connect-now"></a><span data-ttu-id="b6b9b-103">Informazioni su Windows Connect Now</span><span class="sxs-lookup"><span data-stu-id="b6b9b-103">About Windows Connect Now</span></span>

<span data-ttu-id="b6b9b-104">Windows Connect Now (WCN) fornisce un meccanismo semplice e sicuro per i dispositivi e i punti di accesso alla rete, ad esempio stampanti, fotocamere e PC, per la connessione e lo scambio delle impostazioni.</span><span class="sxs-lookup"><span data-stu-id="b6b9b-104">Windows Connect Now (WCN) provides a simple and secure mechanism for network access points and devices (like printers, camera, and PCs) to connect and exchange settings.</span></span> <span data-ttu-id="b6b9b-105">Questa API è l'implementazione Microsoft Wi-Fi del protocollo/Wi-Fi Simple Configuration (WSC), che è stato creato da Wi-Fi Alliance come soluzione per la rete domestica e le piccole imprese.</span><span class="sxs-lookup"><span data-stu-id="b6b9b-105">This API is the Microsoft implementation of the Wi-Fi Protected Setup (WPS)/Wi-Fi Simple Configuration (WSC) protocol, which was created by the Wi-Fi Alliance as a solution for home networking and small businesses.</span></span> <span data-ttu-id="b6b9b-106">Questa tecnologia non è destinata a scenari aziendali.</span><span class="sxs-lookup"><span data-stu-id="b6b9b-106">This technology is not intended for enterprise scenarios.</span></span>

> [!Note]  
> <span data-ttu-id="b6b9b-107">Il nome della specifica è stato modificato tra la versione 1.0 e la versione 2.</span><span class="sxs-lookup"><span data-stu-id="b6b9b-107">The specification name changed between version 1.0h and version 2.</span></span> <span data-ttu-id="b6b9b-108">La specifica della versione 1.0 è stata denominata Wi-Fi installazione protetta (WPS).</span><span class="sxs-lookup"><span data-stu-id="b6b9b-108">The version 1.0h specification was named Wi-Fi Protected Setup (WPS).</span></span> <span data-ttu-id="b6b9b-109">A partire dalla specifica della versione 2, la specifica è denominata Wi-Fi Simple Configuration (WSC).</span><span class="sxs-lookup"><span data-stu-id="b6b9b-109">Starting with version 2 specification, the specification is named Wi-Fi Simple Configuration (WSC).</span></span> <span data-ttu-id="b6b9b-110">Nella documentazione, i termini WPS e WSC vengono usati in modo interscambiabile, a meno che non sia stato specificato.</span><span class="sxs-lookup"><span data-stu-id="b6b9b-110">In our documentation, the terms WPS and WSC are used interchangeably unless noted.</span></span>

 

<span data-ttu-id="b6b9b-111">Windows Connect consente ora alle applicazioni di cercare i dispositivi con supporto per WCN usando l' [API di individuazione funzioni](/previous-versions/windows/desktop/fundisc/fd-portal).</span><span class="sxs-lookup"><span data-stu-id="b6b9b-111">Windows Connect Now enables applications to search for WCN-capable devices using the [Function Discovery API](/previous-versions/windows/desktop/fundisc/fd-portal).</span></span> <span data-ttu-id="b6b9b-112">L'ambito di una ricerca può essere limitato a uno specifico SSID, stato, categoria o persino ampliato per includere tutti i dispositivi che supportano WCN.</span><span class="sxs-lookup"><span data-stu-id="b6b9b-112">The scope of a search can be narrowed down to a specific SSID, state, category, or even broadened to include all WCN-capable devices.</span></span> <span data-ttu-id="b6b9b-113">Una volta individuati i dispositivi, l'API WCN consente la comunicazione con il dispositivo che supporta WCN per semplificare la configurazione o la connettività.</span><span class="sxs-lookup"><span data-stu-id="b6b9b-113">Once devices are located, the WCN API allows communication with the WCN-capable device in order to facilitate configuration or connectivity.</span></span>

 

 