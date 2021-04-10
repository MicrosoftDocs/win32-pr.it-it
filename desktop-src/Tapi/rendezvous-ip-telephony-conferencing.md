---
description: I controlli di Rendezvous TAPI 3 consentono a un programmatore di creare applicazioni in grado di creare e individuare conferenze IP multicast multimediali.
ms.assetid: 4da2046c-00fd-46a8-805f-503729cfa531
title: Conferenza telefonica IP Rendezvous
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d1cbfc3a1e07fdc245af0ae6b93277c90083a75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227483"
---
# <a name="rendezvous-ip-telephony-conferencing"></a><span data-ttu-id="e4488-103">Conferenza telefonica IP Rendezvous</span><span class="sxs-lookup"><span data-stu-id="e4488-103">Rendezvous IP Telephony Conferencing</span></span>

<span data-ttu-id="e4488-104">\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="e4488-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="e4488-105">L'API del client RTC fornisce funzionalità simili.\]</span><span class="sxs-lookup"><span data-stu-id="e4488-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="e4488-106">I controlli di Rendezvous TAPI 3 consentono a un programmatore di creare applicazioni in grado di creare e individuare conferenze IP multicast multimediali.</span><span class="sxs-lookup"><span data-stu-id="e4488-106">The TAPI 3 Rendezvous controls enable a programmer to create applications that can create and discover multimedia multicast IP conferences.</span></span>

<span data-ttu-id="e4488-107">Componenti chiave di Rendezvous:</span><span class="sxs-lookup"><span data-stu-id="e4488-107">The key components of Rendezvous:</span></span>

<span data-ttu-id="e4488-108">I [controlli directory](directory-controls.md) sono un'astrazione degli elenchi di conferenze in un server ILS o NTDS.</span><span class="sxs-lookup"><span data-stu-id="e4488-108">[Directory Controls](directory-controls.md) are an abstraction of conference listings on an ILS or NTDS server.</span></span>

<span data-ttu-id="e4488-109">I [controlli BLOB della conferenza](conference-blob-controls.md) rappresentano informazioni specifiche per la conferenza, ad esempio l'ora di inizio e di fine.</span><span class="sxs-lookup"><span data-stu-id="e4488-109">[Conference Blob Controls](conference-blob-controls.md) represent conference-specific information such as start and stop time.</span></span> <span data-ttu-id="e4488-110">Sono disponibili interfacce speciali per i BLOB del protocollo SDP.</span><span class="sxs-lookup"><span data-stu-id="e4488-110">Special interfaces are provided for SDP protocol blobs.</span></span> <span data-ttu-id="e4488-111">Per informazioni dettagliate, vedere il documento RFC 2327 denominato "SDP: Session Description Protocol".</span><span class="sxs-lookup"><span data-stu-id="e4488-111">For detailed information, see RFC 2327 entitled "SDP: Session Description Protocol."</span></span> <span data-ttu-id="e4488-112">Una copia corrente di questa RFC può essere individuata tramite un motore di ricerca Internet.</span><span class="sxs-lookup"><span data-stu-id="e4488-112">A current copy of this RFC can be located using an Internet search engine.</span></span>

<span data-ttu-id="e4488-113">Le [interfacce com multicast](multicast-com-interfaces.md) sono wrapper com per le funzioni MADCAP, noto in precedenza come mdhcp.</span><span class="sxs-lookup"><span data-stu-id="e4488-113">[Multicast COM Interfaces](multicast-com-interfaces.md) are COM wrappers for the MADCAP functions, formerly know as MDHCP.</span></span> <span data-ttu-id="e4488-114">Queste interfacce consentono a un'applicazione di ottenere indirizzi multicast da un server di allocazione indirizzi multicast.</span><span class="sxs-lookup"><span data-stu-id="e4488-114">These interfaces allow an application to get multicast addresses from a multicast address allocation server.</span></span>

<span data-ttu-id="e4488-115">Il materiale seguente fornisce una panoramica generale e alcuni esempi di utilizzo dei controlli Rendezvous per la telefonia IP e la conferenza.</span><span class="sxs-lookup"><span data-stu-id="e4488-115">The following material provides a general overview and some usage examples of the Rendezvous controls for IP telephony and conferencing.</span></span>

 

 



