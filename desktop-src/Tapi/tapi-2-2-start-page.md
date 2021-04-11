---
description: Microsoft Telephony Application Programming Interface (TAPI) versione 2,2 (TAPI/C) consente l'implementazione di applicazioni di comunicazione che variano da controllo modem di base a Call Center con più agenti e commutatori.
ms.assetid: 02bfe923-9915-439e-ac7c-a570416d054a
title: Telephony Application Programming Interface versione 2,2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e0dc158210350979105d765dc939f600f61d8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104231834"
---
# <a name="telephony-application-programming-interface-version-22"></a><span data-ttu-id="f667f-103">Telephony Application Programming Interface versione 2,2</span><span class="sxs-lookup"><span data-stu-id="f667f-103">Telephony Application Programming Interface Version 2.2</span></span>

## <a name="purpose"></a><span data-ttu-id="f667f-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="f667f-104">Purpose</span></span>

<span data-ttu-id="f667f-105">Microsoft Telephony Application Programming Interface (TAPI) versione 2,2 (TAPI/C) consente l'implementazione di applicazioni di comunicazione che variano da controllo modem di base a Call Center con più agenti e commutatori.</span><span class="sxs-lookup"><span data-stu-id="f667f-105">The Microsoft Telephony Application Programming Interface (TAPI) version 2.2 (TAPI/C) enables implementation of communications applications ranging from basic modem control to call centers with multiple agents and switches.</span></span>

## <a name="where-applicable"></a><span data-ttu-id="f667f-106">Se applicabile</span><span class="sxs-lookup"><span data-stu-id="f667f-106">Where applicable</span></span>

<span data-ttu-id="f667f-107">Le applicazioni TAPI 2,2 possibili includono:</span><span class="sxs-lookup"><span data-stu-id="f667f-107">Possible TAPI 2.2 applications include:</span></span>

-   <span data-ttu-id="f667f-108">Chiamate vocali di base sulla rete telefonica a commutazione pubblica (PSTN)</span><span class="sxs-lookup"><span data-stu-id="f667f-108">Basic voice calls on the Public Switched Telephone Network (PSTN)</span></span>
-   <span data-ttu-id="f667f-109">Applicazioni del Call Center per il rilevamento di più agenti</span><span class="sxs-lookup"><span data-stu-id="f667f-109">Call center applications for tracking multiple agents</span></span>
-   <span data-ttu-id="f667f-110">Controllo modem</span><span class="sxs-lookup"><span data-stu-id="f667f-110">Modem control</span></span>
-   <span data-ttu-id="f667f-111">Controllo PBX</span><span class="sxs-lookup"><span data-stu-id="f667f-111">PBX control</span></span>
-   <span data-ttu-id="f667f-112">Sistemi IVR (Interactive Voice Response)</span><span class="sxs-lookup"><span data-stu-id="f667f-112">Interactive voice response (IVR) systems</span></span>
-   <span data-ttu-id="f667f-113">Messaggi vocali</span><span class="sxs-lookup"><span data-stu-id="f667f-113">Voice mail</span></span>
-   <span data-ttu-id="f667f-114">Controllo dettagliato del dispositivo telefonico</span><span class="sxs-lookup"><span data-stu-id="f667f-114">Detailed phone device control</span></span>

## <a name="developer-audience"></a><span data-ttu-id="f667f-115">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="f667f-115">Developer audience</span></span>

<span data-ttu-id="f667f-116">TAPI/C è progettato per l'uso da programmatori C/C++.</span><span class="sxs-lookup"><span data-stu-id="f667f-116">TAPI/C is designed for use by C/C++ programmers.</span></span> <span data-ttu-id="f667f-117">L'esperienza di sviluppo con le telecomunicazioni o altre applicazioni di telefonia è utile, ma non necessaria.</span><span class="sxs-lookup"><span data-stu-id="f667f-117">Development experience with telecommunications or other telephony applications is helpful, but not necessary.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="f667f-118">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="f667f-118">Run-time requirements</span></span>

<span data-ttu-id="f667f-119">La versione 2,2 di TAPI consente lo sviluppo di applicazioni di comunicazione per i sistemi operativi Windows Server 2003, Windows XP, Windows 2000, Windows NT, Windows me, Windows 98 e Windows 95.</span><span class="sxs-lookup"><span data-stu-id="f667f-119">TAPI version 2.2 enables development of communications applications for the Windows Server 2003 operating systems, Windows XP, Windows 2000, Windows NT, Windows Me, Windows 98, and Windows 95.</span></span> <span data-ttu-id="f667f-120">Per ulteriori informazioni sui sistemi operativi che supportano una particolare funzione, vedere la sezione requisiti della documentazione relativa a tale funzione.</span><span class="sxs-lookup"><span data-stu-id="f667f-120">For more information about which operating systems support a particular function, see the Requirements section of the documentation for that function.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f667f-121">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="f667f-121">In this section</span></span>



| <span data-ttu-id="f667f-122">Argomento</span><span class="sxs-lookup"><span data-stu-id="f667f-122">Topic</span></span>                                          | <span data-ttu-id="f667f-123">Descrizione</span><span class="sxs-lookup"><span data-stu-id="f667f-123">Description</span></span>                                                                                                       |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f667f-124">Overview</span><span class="sxs-lookup"><span data-stu-id="f667f-124">Overview</span></span>](tapi-2-2-overview.md)<br/>   | <span data-ttu-id="f667f-125">Informazioni generali sull'architettura e i componenti TAPI.</span><span class="sxs-lookup"><span data-stu-id="f667f-125">General information about TAPI architecture and components.</span></span><br/>                                            |
| [<span data-ttu-id="f667f-126">Riferimento</span><span class="sxs-lookup"><span data-stu-id="f667f-126">Reference</span></span>](tapi-2-2-reference.md)<br/> | <span data-ttu-id="f667f-127">Documentazione di funzioni, strutture, messaggi, costanti e classi di dispositivi disponibili in TAPI 2,2.</span><span class="sxs-lookup"><span data-stu-id="f667f-127">Documentation of functions, structures, messages, constants, and device classes available in TAPI 2.2.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="f667f-128">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="f667f-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f667f-129">TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="f667f-129">TAPI 3.1</span></span>](./tapi-3-1-start-page.md)
</dt> <dt>

[<span data-ttu-id="f667f-130">Provider di servizi TAPI</span><span class="sxs-lookup"><span data-stu-id="f667f-130">TAPI Service Providers</span></span>](./tapi-service-providers.md)
</dt> </dl>

 

