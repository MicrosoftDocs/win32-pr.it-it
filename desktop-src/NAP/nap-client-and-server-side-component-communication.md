---
title: Comunicazione tra client NAP e componenti lato server
description: Comunicazione tra client NAP e componenti lato server
ms.assetid: 7658cf0c-607b-44ba-b579-72082d0d1f51
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07597ac80a1e02c4f8528b3c99050aefb5963988
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396679"
---
# <a name="nap-client-and-server-side-component-communication"></a><span data-ttu-id="4a48a-103">Comunicazione tra client NAP e componenti lato server</span><span class="sxs-lookup"><span data-stu-id="4a48a-103">NAP Client and Server-side Component Communication</span></span>

> [!Note]  
> <span data-ttu-id="4a48a-104">La piattaforma protezione accesso alla rete non è disponibile a partire da Windows 10</span><span class="sxs-lookup"><span data-stu-id="4a48a-104">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="4a48a-105">Il componente agente NAP è in grado di comunicare con il componente server di amministrazione NAP tramite il processo seguente:</span><span class="sxs-lookup"><span data-stu-id="4a48a-105">The NAP Agent component can communicate with the NAP Administration Server component through the following process:</span></span>

1.  <span data-ttu-id="4a48a-106">L'agente NAP passa il SSoH di protezione accesso alla rete EC.</span><span class="sxs-lookup"><span data-stu-id="4a48a-106">The NAP Agent passes the SSoH to the NAP EC.</span></span>
2.  <span data-ttu-id="4a48a-107">NAP EC passa il SSoH di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="4a48a-107">The NAP EC passes the SSoH to the NAP ES.</span></span>
3.  <span data-ttu-id="4a48a-108">NAP ES passa il SSoH al servizio Server dei criteri di rete (NPS).</span><span class="sxs-lookup"><span data-stu-id="4a48a-108">The NAP ES passes the SSoH to the Network Policy Server (NPS) service.</span></span>
4.  <span data-ttu-id="4a48a-109">Il servizio NPS passa il SSoH al server di amministrazione NAP.</span><span class="sxs-lookup"><span data-stu-id="4a48a-109">The NPS service passes the SSoH to the NAP Administration Server.</span></span>

<span data-ttu-id="4a48a-110">Un SHA può comunicare con l'integrità di sistema corrispondente tramite il processo seguente:</span><span class="sxs-lookup"><span data-stu-id="4a48a-110">An SHA can communicate with its corresponding SHV through the following process:</span></span>

1.  <span data-ttu-id="4a48a-111">SHA passa il rapporto di integrità all'agente NAP.</span><span class="sxs-lookup"><span data-stu-id="4a48a-111">The SHA passes its SoH to the NAP Agent.</span></span>
2.  <span data-ttu-id="4a48a-112">L'agente NAP passa il rapporto di integrità, contenuto all'interno di SSoH, alla rete di protezione accesso alla rete (EC).</span><span class="sxs-lookup"><span data-stu-id="4a48a-112">The NAP Agent passes the SoH, contained within the SSoH, to the NAP EC.</span></span>
3.  <span data-ttu-id="4a48a-113">La protezione accesso alla rete EC passa il rapporto di integrità al NAP.</span><span class="sxs-lookup"><span data-stu-id="4a48a-113">The NAP EC passes the SoH to the NAP ES.</span></span>
4.  <span data-ttu-id="4a48a-114">NAP ES passa il rapporto di integrità al server di amministrazione NAP.</span><span class="sxs-lookup"><span data-stu-id="4a48a-114">The NAP ES passes the SoH to the NAP Administration Server.</span></span>
5.  <span data-ttu-id="4a48a-115">Il server di amministrazione NAP passa il rapporto di integrità al servizio di convalida dell'integrità.</span><span class="sxs-lookup"><span data-stu-id="4a48a-115">The NAP Administration Server passes the SoH to the SHV.</span></span>

<span data-ttu-id="4a48a-116">Nella figura seguente viene illustrato il processo di comunicazione tra i componenti client NAP e i componenti lato server di NAP.</span><span class="sxs-lookup"><span data-stu-id="4a48a-116">The figure below shows the communication process from NAP client components to NAP server-side components.</span></span>

![architettura della comunicazione da client a server nella piattaforma NAP](images/nap-client-to-server-comm.png)

<span data-ttu-id="4a48a-118">Il server di amministrazione NAP è in grado di comunicare con l'agente NAP tramite il processo seguente:</span><span class="sxs-lookup"><span data-stu-id="4a48a-118">The NAP Administration Server can communicate with the NAP Agent through the following process:</span></span>

1.  <span data-ttu-id="4a48a-119">Il server di amministrazione NAP passa il SoHRs al servizio Server dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="4a48a-119">The NAP Administration Server passes the SoHRs to the NPS service.</span></span>
2.  <span data-ttu-id="4a48a-120">Il servizio NPS passa il risposta al rapporto di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="4a48a-120">The NPS service passes the SSoHR to the NAP ES.</span></span>
3.  <span data-ttu-id="4a48a-121">NAP ES passa il risposta al rapporto di protezione accesso alla rete EC.</span><span class="sxs-lookup"><span data-stu-id="4a48a-121">The NAP ES passes the SSoHR to the NAP EC.</span></span>
4.  <span data-ttu-id="4a48a-122">Il risposta al rapporto di protezione accesso alla rete EC passa l'agente protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="4a48a-122">The NAP EC passes the SSoHR to the NAP Agent.</span></span>

<span data-ttu-id="4a48a-123">Il servizio di convalida dell'integrità di sistema può comunicare con l'SHA corrispondente tramite il processo seguente:</span><span class="sxs-lookup"><span data-stu-id="4a48a-123">The SHV can communicate with its corresponding SHA through the following process:</span></span>

1.  <span data-ttu-id="4a48a-124">Il servizio di convalida dell'integrità di sistema passa il relativo SoHR al server di amministrazione NAP.</span><span class="sxs-lookup"><span data-stu-id="4a48a-124">The SHV passes its SoHR to the NAP Administration Server.</span></span>
2.  <span data-ttu-id="4a48a-125">Il server di amministrazione NAP passa il SoHR al servizio Server dei criteri di rete.</span><span class="sxs-lookup"><span data-stu-id="4a48a-125">The NAP Administration Server passes the SoHR to the NPS service.</span></span>
3.  <span data-ttu-id="4a48a-126">Il servizio Server dei criteri di rete passa il SoHR, contenuto all'interno di risposta al rapporto, all'ES NAP.</span><span class="sxs-lookup"><span data-stu-id="4a48a-126">The NPS service passes the SoHR, contained within the SSoHR, to the NAP ES.</span></span>
4.  <span data-ttu-id="4a48a-127">NAP ES passa il SoHR di protezione accesso alla rete EC.</span><span class="sxs-lookup"><span data-stu-id="4a48a-127">The NAP ES passes the SoHR to the NAP EC.</span></span>
5.  <span data-ttu-id="4a48a-128">Il SoHR di protezione accesso alla rete EC passa l'agente protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="4a48a-128">The NAP EC passes the SoHR to the NAP Agent.</span></span>
6.  <span data-ttu-id="4a48a-129">L'agente NAP passa il SoHR all'SHA.</span><span class="sxs-lookup"><span data-stu-id="4a48a-129">The NAP Agent passes the SoHR to the SHA.</span></span>

<span data-ttu-id="4a48a-130">Nella figura seguente viene illustrato il processo di comunicazione tra i componenti lato server di NAP e i componenti client di protezione accesso alla rete.</span><span class="sxs-lookup"><span data-stu-id="4a48a-130">The figure below shows the communication process from NAP server-side components to NAP client components.</span></span>

![architettura della comunicazione da server a client nella piattaforma NAP](images/nap-server-to-client-comm.png)

 

 




