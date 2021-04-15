---
title: La porta 3 è deprecata per i driver NDIS 6,30
description: La porta 3 è deprecata per i driver NDIS 6,30
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/01/2020
ms.locfileid: "104474494"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a><span data-ttu-id="19a48-103">La porta 3 è deprecata per i driver NDIS 6,30</span><span class="sxs-lookup"><span data-stu-id="19a48-103">Port 3 is deprecated for NDIS 6.30 drivers</span></span>

## <a name="platforms"></a><span data-ttu-id="19a48-104">Piattaforme</span><span class="sxs-lookup"><span data-stu-id="19a48-104">Platforms</span></span>

<span data-ttu-id="19a48-105">**Client** -Windows 8</span><span class="sxs-lookup"><span data-stu-id="19a48-105">**Clients** – Windows 8</span></span>  
<span data-ttu-id="19a48-106">**Server** : Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="19a48-106">**Servers** – Windows Server 2012</span></span>  


## <a name="description"></a><span data-ttu-id="19a48-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="19a48-107">Description</span></span>

<span data-ttu-id="19a48-108">Windows 8 rimuove il supporto della piattaforma per i driver WLAN miniport NDIS per creare o avviare la porta di estendibilità IHV (nota anche come terza porta).</span><span class="sxs-lookup"><span data-stu-id="19a48-108">Windows 8 removes platform support for NDIS miniport WLAN drivers to create or start up the IHV extensibility port (also known as 3rd port).</span></span> <span data-ttu-id="19a48-109">Questa funzionalità è stata introdotta in Windows 7 come misura tampone mentre Wi-Fi Alliance (WFA) ha sviluppato la specifica Wi-Fi diretta.</span><span class="sxs-lookup"><span data-stu-id="19a48-109">This feature was introduced in Windows 7 as a stopgap measure while the Wi-Fi Alliance (WFA) developed the Wi-Fi Direct specification.</span></span> <span data-ttu-id="19a48-110">La specifica è ora terminata, i prodotti che usano Wi-Fi Direct vengono certificati e Windows 8 introduce uno stack nativo Wi-Fi diretto.</span><span class="sxs-lookup"><span data-stu-id="19a48-110">The specification is now finished, products using Wi-Fi Direct are being certified, and Windows 8 introduces a native Wi-Fi Direct stack.</span></span>

## <a name="manifestation"></a><span data-ttu-id="19a48-111">Manifestazione</span><span class="sxs-lookup"><span data-stu-id="19a48-111">Manifestation</span></span>

<span data-ttu-id="19a48-112">Niente, perché la terza porta è una funzionalità della piattaforma che i driver miniport di rete WLAN si avviano se questa funzionalità è necessaria.</span><span class="sxs-lookup"><span data-stu-id="19a48-112">Nothing, as third port is a platform capability that WLAN miniport drivers start up if they need this functionality.</span></span>

## <a name="solution"></a><span data-ttu-id="19a48-113">Soluzione</span><span class="sxs-lookup"><span data-stu-id="19a48-113">Solution</span></span>

<span data-ttu-id="19a48-114">La funzionalità della porta di estendibilità è disponibile per i driver esistenti che non segnalano NDIS 6,30 per garantire la compatibilità dei dispositivi.</span><span class="sxs-lookup"><span data-stu-id="19a48-114">We are keeping the extensibility port feature available for existing drivers that do not report NDIS 6.30 to maintain device compatibility.</span></span> <span data-ttu-id="19a48-115">Tuttavia, i nuovi driver WLAN che segnalano NDIS 6,30 non saranno in grado di avviare la porta. gli sviluppatori di questi driver devono invece usare Wi-Fi Direct.</span><span class="sxs-lookup"><span data-stu-id="19a48-115">However, new WLAN drivers that report NDIS 6.30 will not be able to start this port; instead, developers of these drivers should use Wi-Fi Direct.</span></span>

 

 




