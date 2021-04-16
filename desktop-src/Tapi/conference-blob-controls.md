---
description: Il diagramma seguente illustra gli oggetti principali inclusi nei controlli BLOB della conferenza TAPI 3. Le interfacce visualizzate sono collegate con collegamento ipertestuale nelle pagine di riferimento pertinenti.
ms.assetid: 535bbb33-01cb-4484-b216-4808e47e4db5
title: Controlli BLOB conferenza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bacf13567abd46f56c399cefa732be97b081cfd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527223"
---
# <a name="conference-blob-controls"></a><span data-ttu-id="541df-104">Controlli BLOB conferenza</span><span class="sxs-lookup"><span data-stu-id="541df-104">Conference Blob Controls</span></span>

<span data-ttu-id="541df-105">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="541df-105">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="541df-106">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="541df-106">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="541df-107">Il diagramma seguente illustra gli oggetti principali inclusi nei controlli BLOB della conferenza TAPI 3.</span><span class="sxs-lookup"><span data-stu-id="541df-107">The following diagram illustrates the main objects involved in TAPI 3 conference blob controls.</span></span> <span data-ttu-id="541df-108">Le interfacce visualizzate sono collegate con collegamento ipertestuale nelle pagine di riferimento pertinenti.</span><span class="sxs-lookup"><span data-stu-id="541df-108">Interfaces shown are hyperlinked into the relevant reference pages.</span></span>

![interfacce e controlli BLOB della conferenza](images/rendblob.png)

<span data-ttu-id="541df-110">Il BLOB della conferenza contiene informazioni specifiche del provider su un oggetto Conference.</span><span class="sxs-lookup"><span data-stu-id="541df-110">The conference blob contains provider-specific information on a conference object.</span></span> <span data-ttu-id="541df-111">Un puntatore al BLOB dell'interfaccia [**ITConferenceBlob**](itconferenceblob.md) viene ottenuto eseguendo un QueryInterface in [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span><span class="sxs-lookup"><span data-stu-id="541df-111">A pointer to the [**ITConferenceBlob**](itconferenceblob.md) interface blob is obtained by doing a QueryInterface on [**ITDirectoryObjectConference**](/windows/desktop/api/Rend/nn-rend-itdirectoryobjectconference).</span></span> <span data-ttu-id="541df-112">L'interfaccia **ITConferenceBlob** fornisce metodi per la manipolazione di base di un BLOB di conferenze generiche.</span><span class="sxs-lookup"><span data-stu-id="541df-112">The **ITConferenceBlob** interface provides methods for basic manipulation of a generic conference blob.</span></span> <span data-ttu-id="541df-113">Un'applicazione che usa BLOB di conferenze non SDP deve implementare i propri metodi per la manipolazione dei dettagli.</span><span class="sxs-lookup"><span data-stu-id="541df-113">An application using non-SDP conference blobs must implement its own methods for detail manipulation.</span></span>

<span data-ttu-id="541df-114">Rendezvous fornisce l'interfaccia [**ITSdp**](itsdp.md) per la manipolazione dei BLOB delle conferenze SDP.</span><span class="sxs-lookup"><span data-stu-id="541df-114">Rendezvous provides the [**ITSdp**](itsdp.md) interface for manipulating SDP conference blobs.</span></span> <span data-ttu-id="541df-115">SDP è un protocollo per la descrizione delle sessioni multimediali e delle relative informazioni di pianificazione.</span><span class="sxs-lookup"><span data-stu-id="541df-115">The SDP is a protocol for describing multimedia sessions and their related scheduling information.</span></span> <span data-ttu-id="541df-116">Per ulteriori informazioni sul protocollo SDP, individuare Internet Engineering Task Force (IETF) RFC 2327 denominato "SDP: Session Description Protocol".</span><span class="sxs-lookup"><span data-stu-id="541df-116">For additional information on the SDP protocol, locate Internet Engineering Task Force (IETF) RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="541df-117">Se l'interfaccia **ITSDP** esiste per un BLOB di conferenza specifico, è possibile ottenere un puntatore a tale BLOB eseguendo un **QueryInterface** in [**ITConferenceBlob**](itconferenceblob.md).</span><span class="sxs-lookup"><span data-stu-id="541df-117">If the **ITSDP** interface exists for a given conference blob, you can obtain a pointer to it by doing a **QueryInterface** on [**ITConferenceBlob**](itconferenceblob.md).</span></span>

<span data-ttu-id="541df-118">Per i BLOB di conferenze SDP, le interfacce [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md)e [**ITmedia**](itmedia.md) consentono un controllo dettagliato delle caratteristiche dei supporti e dei tempi delle conferenze SDP.</span><span class="sxs-lookup"><span data-stu-id="541df-118">For SDP conference blobs, the [**ITTimeCollection**](ittimecollection.md), [**ITTime**](ittime.md), [**ITMediaCollection**](itmediacollection.md), and [**ITMedia**](itmedia.md) interfaces allow detailed control of SDP conference time and media characteristics.</span></span>

 

 



