---
title: Requisiti di sistema per le applicazioni di Accodamento RPC-Message
description: Per utilizzare il trasporto di Accodamento messaggi in un'applicazione client/server RPC, è necessario che nei computer server e client siano installate la piattaforma del sistema operativo e il software di Accodamento messaggi appropriati.
ms.assetid: f90318a6-0be6-4e1a-a1a5-1709808b5d3b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1274c888506a6868eb7ded5ba96c5f1ea8dc8b2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399538"
---
# <a name="system-requirements-for-rpc-message-queuing-applications"></a><span data-ttu-id="79aec-103">Requisiti di sistema per le applicazioni di Accodamento RPC-Message</span><span class="sxs-lookup"><span data-stu-id="79aec-103">System Requirements for RPC-Message Queuing Applications</span></span>

<span data-ttu-id="79aec-104">Per utilizzare il trasporto di Accodamento messaggi in un'applicazione client/server RPC, è necessario che nei computer server e client siano installate la piattaforma del sistema operativo e il software di Accodamento messaggi appropriati.</span><span class="sxs-lookup"><span data-stu-id="79aec-104">To use the message-queuing transport in an RPC client/server application, the server and client computers must have the appropriate operating system platform and Message Queuing software installed.</span></span>

<span data-ttu-id="79aec-105">I requisiti per i computer server sono:</span><span class="sxs-lookup"><span data-stu-id="79aec-105">Requirements for server computers are:</span></span>

-   <span data-ttu-id="79aec-106">Microsoft Windows Server 2003, Windows XP o Windows 2000 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="79aec-106">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="79aec-107">SQL Server versione 6,5 o successiva.</span><span class="sxs-lookup"><span data-stu-id="79aec-107">SQL Server version 6.5 or later.</span></span>
-   <span data-ttu-id="79aec-108">Controller aziendale primario di Accodamento messaggi o controller del sito primario.</span><span class="sxs-lookup"><span data-stu-id="79aec-108">Message Queuing Primary Enterprise Controller or Primary Site Controller.</span></span>
-   <span data-ttu-id="79aec-109">DLL di trasporto lato server RPC (RpcMqSvr.dll).</span><span class="sxs-lookup"><span data-stu-id="79aec-109">RPC server-side transport DLL (RpcMqSvr.dll).</span></span>

<span data-ttu-id="79aec-110">I requisiti per i computer client sono:</span><span class="sxs-lookup"><span data-stu-id="79aec-110">Requirements for client computers are:</span></span>

-   <span data-ttu-id="79aec-111">Microsoft Windows Server 2003, Windows XP o Windows 2000 o versione successiva.</span><span class="sxs-lookup"><span data-stu-id="79aec-111">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later.</span></span>
-   <span data-ttu-id="79aec-112">Microsoft Message Queuing client.</span><span class="sxs-lookup"><span data-stu-id="79aec-112">Microsoft Message Queuing Client.</span></span>
-   <span data-ttu-id="79aec-113">DLL di trasporto lato client RPC (RpcMqCl.dll).</span><span class="sxs-lookup"><span data-stu-id="79aec-113">RPC client-side transport DLL (RpcMqCl.dll).</span></span>

<span data-ttu-id="79aec-114">Quando i componenti MSMQ sono installati nei computer client e server, i registri di sistema vengono automaticamente configurati per includere il protocollo di trasporto di Accodamento messaggi di [ncadg \_ mq](/windows/desktop/Midl/ncadg-mq) per le chiamate di procedure remote.</span><span class="sxs-lookup"><span data-stu-id="79aec-114">When the MSMQ components are installed on the client and server computers, the system registries are automatically configured to include the [ncadg\_mq](/windows/desktop/Midl/ncadg-mq) message-queuing transport protocol for remote procedure calls.</span></span>

<span data-ttu-id="79aec-115">Per compilare l'applicazione RPC-MSMQ, è necessario quanto segue:</span><span class="sxs-lookup"><span data-stu-id="79aec-115">To build your RPC-MSMQ application you need the following:</span></span>

-   <span data-ttu-id="79aec-116">Microsoft Windows Server 2003, Windows XP o Windows 2000 o versione successiva</span><span class="sxs-lookup"><span data-stu-id="79aec-116">Microsoft Windows Server 2003, Windows XP, or Windows 2000 or later</span></span>
-   <span data-ttu-id="79aec-117">MIDL versione 3.1.76 o successiva.</span><span class="sxs-lookup"><span data-stu-id="79aec-117">MIDL version 3.1.76 or later.</span></span>

 

 