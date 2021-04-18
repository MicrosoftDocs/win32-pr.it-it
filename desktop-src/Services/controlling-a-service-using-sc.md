---
description: Il Windows SDK contiene un'utilità da riga di comando, Sc.exe, che può essere utilizzata per controllare un servizio. I relativi comandi corrispondono alle funzioni fornite da SCM. La sintassi è la seguente.
ms.assetid: 7c3e5c39-ec0f-4174-9ecf-239927de3d39
title: Controllo di un servizio con SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c1aa991395ba2aa55bf05d63176fba59d96dce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316616"
---
# <a name="controlling-a-service-using-sc"></a><span data-ttu-id="62ae1-105">Controllo di un servizio con SC</span><span class="sxs-lookup"><span data-stu-id="62ae1-105">Controlling a Service Using SC</span></span>

<span data-ttu-id="62ae1-106">Il Windows SDK contiene un'utilità da riga di comando, Sc.exe, che può essere utilizzata per controllare un servizio.</span><span class="sxs-lookup"><span data-stu-id="62ae1-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to control a service.</span></span> <span data-ttu-id="62ae1-107">I relativi comandi corrispondono alle funzioni fornite da SCM.</span><span class="sxs-lookup"><span data-stu-id="62ae1-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="62ae1-108">La sintassi è la seguente.</span><span class="sxs-lookup"><span data-stu-id="62ae1-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="62ae1-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="62ae1-109">Syntax</span></span>

<span data-ttu-id="62ae1-110">**SC** \[ *Nomeserver* \] *Comando* \[ *ServiceName* \] \[  \] opzione1 \[ *opzione2* \] ...</span><span class="sxs-lookup"><span data-stu-id="62ae1-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="62ae1-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Nomeserver*</span><span class="sxs-lookup"><span data-stu-id="62ae1-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="62ae1-112">Nome del server facoltativo.</span><span class="sxs-lookup"><span data-stu-id="62ae1-112">Optional server name.</span></span> <span data-ttu-id="62ae1-113">Utilizzare il formato \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="62ae1-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="62ae1-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Comando*</span><span class="sxs-lookup"><span data-stu-id="62ae1-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="62ae1-115">Uno dei comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="62ae1-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="62ae1-116">continue</span><span class="sxs-lookup"><span data-stu-id="62ae1-116">continue</span></span></dd> <dd><span data-ttu-id="62ae1-117">controllo</span><span class="sxs-lookup"><span data-stu-id="62ae1-117">control</span></span></dd> <dd><span data-ttu-id="62ae1-118">interrogare</span><span class="sxs-lookup"><span data-stu-id="62ae1-118">interrogate</span></span></dd> <dd><span data-ttu-id="62ae1-119">Sospendi</span><span class="sxs-lookup"><span data-stu-id="62ae1-119">pause</span></span></dd> <dd><span data-ttu-id="62ae1-120">start</span><span class="sxs-lookup"><span data-stu-id="62ae1-120">start</span></span></dd> <dd><span data-ttu-id="62ae1-121">stop</span><span class="sxs-lookup"><span data-stu-id="62ae1-121">stop</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="62ae1-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span><span class="sxs-lookup"><span data-stu-id="62ae1-122"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="62ae1-123">Nome del servizio, come specificato al momento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="62ae1-123">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="62ae1-124"><span id="option1"></span><span id="OPTION1"></span>*opzione1*</span><span class="sxs-lookup"><span data-stu-id="62ae1-124"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="62ae1-125">Parametro opzionale.</span><span class="sxs-lookup"><span data-stu-id="62ae1-125">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="62ae1-126"><span id="option2"></span><span id="OPTION2"></span>*opzione2*</span><span class="sxs-lookup"><span data-stu-id="62ae1-126"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="62ae1-127">Parametro opzionale.</span><span class="sxs-lookup"><span data-stu-id="62ae1-127">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="62ae1-128">Commenti</span><span class="sxs-lookup"><span data-stu-id="62ae1-128">Remarks</span></span>

<span data-ttu-id="62ae1-129">Per visualizzare la sintassi completa per un comando, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="62ae1-129">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="62ae1-130">**SC** ( *comando* )</span><span class="sxs-lookup"><span data-stu-id="62ae1-130">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="62ae1-131">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="62ae1-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62ae1-132">Richieste di controllo del servizio</span><span class="sxs-lookup"><span data-stu-id="62ae1-132">Service Control Requests</span></span>](service-control-requests.md)
</dt> <dt>

[<span data-ttu-id="62ae1-133">Avvio del servizio</span><span class="sxs-lookup"><span data-stu-id="62ae1-133">Service Startup</span></span>](service-startup.md)
</dt> </dl>

 

 



