---
title: Registrazione (piattaforma filtro Windows)
description: Windows Filtering Platform (WFP) consente di registrare le gocce di pacchetti e gli errori IKE/AuthIP.
ms.assetid: 607b7664-6be4-4ae6-991b-58ac9175405a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a27868c76a643a8e1b7b478152c100a2026bfc20
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/10/2020
ms.locfileid: "106300813"
---
# <a name="logging-windows-filtering-platform"></a><span data-ttu-id="9b0ad-103">Registrazione (piattaforma filtro Windows)</span><span class="sxs-lookup"><span data-stu-id="9b0ad-103">Logging (Windows Filtering Platform)</span></span>

<span data-ttu-id="9b0ad-104">Windows Filtering Platform (WFP) consente di registrare le gocce di pacchetti e gli errori IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-104">The Windows Filtering Platform (WFP) provides logging of packet drops and IKE/AuthIP failures.</span></span>

<span data-ttu-id="9b0ad-105">Gli eventi registrati vengono definiti nel tipo enumerato di [**\_ \_ \_ tipo evento NET FWPM**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) e sono i seguenti.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-105">The logged events are defined in the [**FWPM\_NET\_EVENT\_TYPE**](/windows/desktop/api/Fwpmtypes/ne-fwpmtypes-fwpm_net_event_type) enumerated type and are as follows.</span></span>

-   <span data-ttu-id="9b0ad-106">Errori in modalità principale IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-106">IKE/AuthIP main mode failures.</span></span>
-   <span data-ttu-id="9b0ad-107">Errori in modalità rapida IKE/AuthIP.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-107">IKE/AuthIP quick mode failures.</span></span>
-   <span data-ttu-id="9b0ad-108">Errori della modalità estesa AuthIP.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-108">AuthIP extended mode failures.</span></span>
-   <span data-ttu-id="9b0ad-109">Pacchetti eliminati durante la classificazione.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-109">Packets dropped during classification.</span></span>
-   <span data-ttu-id="9b0ad-110">Pacchetti eliminati da IPsec.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-110">Packets dropped by IPsec.</span></span>

<span data-ttu-id="9b0ad-111">Per impostazione predefinita, la registrazione per WFP è abilitata per i pacchetti in ingresso unicast e per tutti i pacchetti in uscita (unicast, multicast e broadcast).</span><span class="sxs-lookup"><span data-stu-id="9b0ad-111">By default, logging for WFP is enabled for unicast inbound packets and for all outbound packets (unicast, multicast, and broadcast).</span></span> <span data-ttu-id="9b0ad-112">La registrazione può essere abilitata per il resto dei pacchetti o disabilitata per tutti i pacchetti tramite la funzione di gestione [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) .</span><span class="sxs-lookup"><span data-stu-id="9b0ad-112">Logging can be enabled for the rest of the packets, or disabled for all packets, through the [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0) management function.</span></span> <span data-ttu-id="9b0ad-113">Le impostazioni degli eventi vengono mantenute tra i riavvii.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-113">Event settings persist across reboots.</span></span>

<span data-ttu-id="9b0ad-114">Gli eventi registrati vengono archiviati in un log circolare, ovvero i nuovi eventi eseguono l'override di quelli obsoleti quando il log raggiunge le dimensioni massime e possono essere analizzati utilizzando le funzioni di [gestione degli eventi](fwp-mgmt-functions.md) fornite da WFP.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-114">Logged events are stored in a circular log, that is new events override old ones when the log reaches its maximum size, and can be analyzed using the [event management](fwp-mgmt-functions.md) functions provided by WFP.</span></span> <span data-ttu-id="9b0ad-115">Il registro eventi ha una dimensione massima di 128 KB e può avere circa 100 a 150 eventi.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-115">The event log has a maximum size of 128 KB and it can hold about 100 to 150 events.</span></span>

<span data-ttu-id="9b0ad-116">Le funzioni di enumerazione in generale e [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0) / [**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) in particolare creano uno snapshot del log al momento della creazione dell'handle di enumerazione.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-116">Enumeration functions in general, and [**FwpmNetEventEnum0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum0)/[**FwpmNetEventEnum1**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmneteventenum1) in particular, take a snapshot of the log at the time the enumeration handle is created.</span></span> <span data-ttu-id="9b0ad-117">Le chiamate successive che usano lo stesso handle di enumerazione restituiscono il set successivo di elementi che seguono quelli nell'ultimo buffer di output.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-117">Subsequent calls using the same enumeration handle return the next set of items following those in the last output buffer.</span></span>

<span data-ttu-id="9b0ad-118">Quando un'applicazione Disabilita la registrazione di WFP (chiamando [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)), tutte le applicazioni sono interessate.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-118">When an application disables WFP logging (by calling [**FwpmEngineSetOptions0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0)) all applications are affected.</span></span> <span data-ttu-id="9b0ad-119">Il registro eventi non viene pulito fino a quando un'applicazione non Abilita nuovamente la registrazione di WFP, ma non è possibile eseguire query sul registro eventi prima.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-119">The event log is not cleaned up until an application re-enables WFP logging, but the event log cannot be queried before then.</span></span>

<span data-ttu-id="9b0ad-120">Il registro eventi di WFP viene svuotato dopo un riavvio.</span><span class="sxs-lookup"><span data-stu-id="9b0ad-120">The WFP event log is emptied after a reboot.</span></span>

 

 




