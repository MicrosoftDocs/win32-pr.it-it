---
description: Nel frammento di codice seguente viene illustrato come richiedere e impostare un indirizzo multicast per una conferenza.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Acquisizione di un indirizzo multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128730"
---
# <a name="acquiring-a-multicast-address"></a><span data-ttu-id="eff89-103">Acquisizione di un indirizzo multicast</span><span class="sxs-lookup"><span data-stu-id="eff89-103">Acquiring a Multicast Address</span></span>

<span data-ttu-id="eff89-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="eff89-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="eff89-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="eff89-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="eff89-106">Nel frammento di codice seguente viene illustrato come richiedere e impostare un indirizzo multicast per una conferenza.</span><span class="sxs-lookup"><span data-stu-id="eff89-106">The following code fragment illustrates how to request and set a multicast address for a conference.</span></span>

<span data-ttu-id="eff89-107">Per motivi di semplicità, in questo frammento viene mostrata l'assegnazione di un indirizzo multicast a un elemento multimediale.</span><span class="sxs-lookup"><span data-stu-id="eff89-107">For the sake of simplicity, this fragment shows the assignment of one multicast address to one media item.</span></span> <span data-ttu-id="eff89-108">In realtà, la selezione di un ambito, la richiesta di indirizzo multicast e l'assegnazione verranno eseguite per ogni elemento multimediale che interessano la conferenza.</span><span class="sxs-lookup"><span data-stu-id="eff89-108">In actuality, the selection of a scope, the multicast address request, and the assignment will be performed for every media item involved in the conference.</span></span>

<span data-ttu-id="eff89-109">Questo frammento presuppone che la [connessione a un server ILS](connecting-to-an-ils-server.md) sia già stata eseguita.</span><span class="sxs-lookup"><span data-stu-id="eff89-109">This fragment assumes that [connecting to an ILS server](connecting-to-an-ils-server.md) has already been performed.</span></span> <span data-ttu-id="eff89-110">Le operazioni illustrate qui verranno eseguite nella sezione "modificare le impostazioni, se necessario" di [creazione di un annuncio](creating-a-conference-announcement.md)per la conferenza.</span><span class="sxs-lookup"><span data-stu-id="eff89-110">The operations shown here would be performed in the "Modify the settings if necessary" section of [Creating a Conference Announcement](creating-a-conference-announcement.md).</span></span>


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a><span data-ttu-id="eff89-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="eff89-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eff89-112">Interfacce COM multicast</span><span class="sxs-lookup"><span data-stu-id="eff89-112">Multicast COM Interfaces</span></span>](multicast-com-interfaces.md)
</dt> <dt>

[<span data-ttu-id="eff89-113">**IMcastAddressAllocation**</span><span class="sxs-lookup"><span data-stu-id="eff89-113">**IMcastAddressAllocation**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[<span data-ttu-id="eff89-114">**IMcastScope**</span><span class="sxs-lookup"><span data-stu-id="eff89-114">**IMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[<span data-ttu-id="eff89-115">**IMcastLeaseInfo**</span><span class="sxs-lookup"><span data-stu-id="eff89-115">**IMcastLeaseInfo**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[<span data-ttu-id="eff89-116">**IEnumMcastScope**</span><span class="sxs-lookup"><span data-stu-id="eff89-116">**IEnumMcastScope**</span></span>](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[<span data-ttu-id="eff89-117">**ITConferenceBlob**</span><span class="sxs-lookup"><span data-stu-id="eff89-117">**ITConferenceBlob**</span></span>](itconferenceblob.md)
</dt> <dt>

[<span data-ttu-id="eff89-118">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="eff89-118">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="eff89-119">**ITMediaCollection**</span><span class="sxs-lookup"><span data-stu-id="eff89-119">**ITMediaCollection**</span></span>](itmediacollection.md)
</dt> <dt>

[<span data-ttu-id="eff89-120">**IEnumBstr**</span><span class="sxs-lookup"><span data-stu-id="eff89-120">**IEnumBstr**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[<span data-ttu-id="eff89-121">**ITMedia**</span><span class="sxs-lookup"><span data-stu-id="eff89-121">**ITMedia**</span></span>](itmedia.md)
</dt> <dt>

[<span data-ttu-id="eff89-122">**ITConnection**</span><span class="sxs-lookup"><span data-stu-id="eff89-122">**ITConnection**</span></span>](itconnection.md)
</dt> </dl>

 

 



