---
description: Il Windows SDK contiene un'utilità da riga di comando, Sc.exe, che può essere utilizzata per eseguire query o modificare il database dei servizi installati. I relativi comandi corrispondono alle funzioni fornite da SCM. La sintassi è la seguente.
ms.assetid: d304922c-86fb-4c62-9bfa-c827df4aecd8
title: Configurazione di un servizio con SC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f65669a3a7daa7e0d02731e6423adfbb3806f11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306339"
---
# <a name="configuring-a-service-using-sc"></a><span data-ttu-id="32c25-105">Configurazione di un servizio con SC</span><span class="sxs-lookup"><span data-stu-id="32c25-105">Configuring a Service Using SC</span></span>

<span data-ttu-id="32c25-106">Il Windows SDK contiene un'utilità da riga di comando, Sc.exe, che può essere utilizzata per eseguire query o modificare il database dei servizi installati.</span><span class="sxs-lookup"><span data-stu-id="32c25-106">The Windows SDK contains a command-line utility, Sc.exe, that can be used to query or modify the database of installed services.</span></span> <span data-ttu-id="32c25-107">I relativi comandi corrispondono alle funzioni fornite da SCM.</span><span class="sxs-lookup"><span data-stu-id="32c25-107">Its commands correspond to the functions provided by the SCM.</span></span> <span data-ttu-id="32c25-108">La sintassi è la seguente.</span><span class="sxs-lookup"><span data-stu-id="32c25-108">The syntax is as follows.</span></span>

## <a name="syntax"></a><span data-ttu-id="32c25-109">Sintassi</span><span class="sxs-lookup"><span data-stu-id="32c25-109">Syntax</span></span>

<span data-ttu-id="32c25-110">**SC** \[ *Nomeserver* \] *Comando* \[ *ServiceName* \] \[  \] opzione1 \[ *opzione2* \] ...</span><span class="sxs-lookup"><span data-stu-id="32c25-110">**sc** \[*ServerName*\] *Command* \[*ServiceName*\]\[*option1*\]\[*option2*\]...</span></span>

<dl> <dt>

<span data-ttu-id="32c25-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*Nomeserver*</span><span class="sxs-lookup"><span data-stu-id="32c25-111"><span id="ServerName"></span><span id="servername"></span><span id="SERVERNAME"></span>*ServerName*</span></span>
</dt> <dd>

<span data-ttu-id="32c25-112">Nome del server facoltativo.</span><span class="sxs-lookup"><span data-stu-id="32c25-112">Optional server name.</span></span> <span data-ttu-id="32c25-113">Utilizzare il formato \\ \\ *ServerName*.</span><span class="sxs-lookup"><span data-stu-id="32c25-113">Use the form \\\\*ServerName*.</span></span>

</dd> <dt>

<span data-ttu-id="32c25-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Comando*</span><span class="sxs-lookup"><span data-stu-id="32c25-114"><span id="Command"></span><span id="command"></span><span id="COMMAND"></span>*Command*</span></span>
</dt> <dd>

<span data-ttu-id="32c25-115">Uno dei comandi seguenti:</span><span class="sxs-lookup"><span data-stu-id="32c25-115">One of the following commands:</span></span>

<dl> <dd><span data-ttu-id="32c25-116">boot</span><span class="sxs-lookup"><span data-stu-id="32c25-116">boot</span></span></dd> <dd><span data-ttu-id="32c25-117">config</span><span class="sxs-lookup"><span data-stu-id="32c25-117">config</span></span></dd> <dd><span data-ttu-id="32c25-118">create</span><span class="sxs-lookup"><span data-stu-id="32c25-118">create</span></span></dd> <dd><span data-ttu-id="32c25-119">eliminare</span><span class="sxs-lookup"><span data-stu-id="32c25-119">delete</span></span></dd> <dd><span data-ttu-id="32c25-120">description</span><span class="sxs-lookup"><span data-stu-id="32c25-120">description</span></span></dd> <dd><span data-ttu-id="32c25-121">EnumDepend</span><span class="sxs-lookup"><span data-stu-id="32c25-121">EnumDepend</span></span></dd> <dd><span data-ttu-id="32c25-122">operazione non riuscita</span><span class="sxs-lookup"><span data-stu-id="32c25-122">failure</span></span></dd> <dd><span data-ttu-id="32c25-123">failureflag</span><span class="sxs-lookup"><span data-stu-id="32c25-123">failureflag</span></span></dd> <dd><span data-ttu-id="32c25-124">GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="32c25-124">GetDisplayName</span></span></dd> <dd><span data-ttu-id="32c25-125">GetKeyName</span><span class="sxs-lookup"><span data-stu-id="32c25-125">GetKeyName</span></span></dd> <dd><span data-ttu-id="32c25-126">Lock</span><span class="sxs-lookup"><span data-stu-id="32c25-126">Lock</span></span></dd> <dd><span data-ttu-id="32c25-127">qc</span><span class="sxs-lookup"><span data-stu-id="32c25-127">qc</span></span></dd> <dd><span data-ttu-id="32c25-128">qdescription</span><span class="sxs-lookup"><span data-stu-id="32c25-128">qdescription</span></span></dd> <dd><span data-ttu-id="32c25-129">qfailure</span><span class="sxs-lookup"><span data-stu-id="32c25-129">qfailure</span></span></dd> <dd><span data-ttu-id="32c25-130">qfailureflag</span><span class="sxs-lookup"><span data-stu-id="32c25-130">qfailureflag</span></span></dd> <dd><span data-ttu-id="32c25-131">qprivs</span><span class="sxs-lookup"><span data-stu-id="32c25-131">qprivs</span></span></dd> <dd><span data-ttu-id="32c25-132">qsidtype</span><span class="sxs-lookup"><span data-stu-id="32c25-132">qsidtype</span></span></dd> <dd><span data-ttu-id="32c25-133">query</span><span class="sxs-lookup"><span data-stu-id="32c25-133">query</span></span></dd> <dd><span data-ttu-id="32c25-134">queryex</span><span class="sxs-lookup"><span data-stu-id="32c25-134">queryex</span></span></dd> <dd><span data-ttu-id="32c25-135">privs</span><span class="sxs-lookup"><span data-stu-id="32c25-135">privs</span></span></dd> <dd><span data-ttu-id="32c25-136">QueryLock</span><span class="sxs-lookup"><span data-stu-id="32c25-136">QueryLock</span></span></dd> <dd><span data-ttu-id="32c25-137">sdset</span><span class="sxs-lookup"><span data-stu-id="32c25-137">sdset</span></span></dd> <dd><span data-ttu-id="32c25-138">sdshow</span><span class="sxs-lookup"><span data-stu-id="32c25-138">sdshow</span></span></dd> <dd><span data-ttu-id="32c25-139">showsid</span><span class="sxs-lookup"><span data-stu-id="32c25-139">showsid</span></span></dd> <dd><span data-ttu-id="32c25-140">SIDType</span><span class="sxs-lookup"><span data-stu-id="32c25-140">sidtype</span></span></dd> </dl> </dd> <dt>

<span data-ttu-id="32c25-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span><span class="sxs-lookup"><span data-stu-id="32c25-141"><span id="ServiceName"></span><span id="servicename"></span><span id="SERVICENAME"></span>*ServiceName*</span></span>
</dt> <dd>

<span data-ttu-id="32c25-142">Nome del servizio, come specificato al momento dell'installazione.</span><span class="sxs-lookup"><span data-stu-id="32c25-142">The name of the service, as specified when it was installed.</span></span>

</dd> <dt>

<span data-ttu-id="32c25-143"><span id="option1"></span><span id="OPTION1"></span>*opzione1*</span><span class="sxs-lookup"><span data-stu-id="32c25-143"><span id="option1"></span><span id="OPTION1"></span>*option1*</span></span>
</dt> <dd>

<span data-ttu-id="32c25-144">Parametro opzionale.</span><span class="sxs-lookup"><span data-stu-id="32c25-144">An optional parameter.</span></span>

</dd> <dt>

<span data-ttu-id="32c25-145"><span id="option2"></span><span id="OPTION2"></span>*opzione2*</span><span class="sxs-lookup"><span data-stu-id="32c25-145"><span id="option2"></span><span id="OPTION2"></span>*option2*</span></span>
</dt> <dd>

<span data-ttu-id="32c25-146">Parametro opzionale.</span><span class="sxs-lookup"><span data-stu-id="32c25-146">An optional parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32c25-147">Commenti</span><span class="sxs-lookup"><span data-stu-id="32c25-147">Remarks</span></span>

<span data-ttu-id="32c25-148">Per visualizzare la sintassi completa per un comando, usare il comando seguente:</span><span class="sxs-lookup"><span data-stu-id="32c25-148">To see complete syntax for a command, use the following command:</span></span>

<span data-ttu-id="32c25-149">**SC** ( *comando* )</span><span class="sxs-lookup"><span data-stu-id="32c25-149">**sc** *Command*</span></span>

## <a name="related-topics"></a><span data-ttu-id="32c25-150">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="32c25-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="32c25-151">Configurazione del servizio</span><span class="sxs-lookup"><span data-stu-id="32c25-151">Service Configuration</span></span>](service-configuration.md)
</dt> <dt>

[<span data-ttu-id="32c25-152">Installazione, rimozione ed enumerazione del servizio</span><span class="sxs-lookup"><span data-stu-id="32c25-152">Service Installation, Removal, and Enumeration</span></span>](service-installation-removal-and-enumeration.md)
</dt> </dl>

 

 



