---
description: I provider WMI per la sicurezza possono essere utilizzati per gli script WMI e per creare un provider di sicurezza gestito.
ms.assetid: c3f7bd91-6cea-43ee-b8a7-1506dbd7926d
title: Provider WMI per la sicurezza
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0206e337e5fa23470f015a0264bd77d53e8c4e14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306376"
---
# <a name="security-wmi-providers"></a><span data-ttu-id="ebb2b-103">Provider WMI per la sicurezza</span><span class="sxs-lookup"><span data-stu-id="ebb2b-103">Security WMI Providers</span></span>

## <a name="purpose"></a><span data-ttu-id="ebb2b-104">Scopo</span><span class="sxs-lookup"><span data-stu-id="ebb2b-104">Purpose</span></span>

<span data-ttu-id="ebb2b-105">I provider WMI per la sicurezza consentono agli amministratori e ai programmatori di configurare Crittografia unità BitLocker (BDE) e il Trusted Platform Module (TPM) utilizzando Strumentazione gestione Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="ebb2b-105">The Security WMI providers enable administrators and programmers to configure BitLocker Drive Encryption (BDE) and the Trusted Platform Module (TPM) using Windows Management Instrumentation (WMI).</span></span>

## <a name="developer-audience"></a><span data-ttu-id="ebb2b-106">Sviluppatori</span><span class="sxs-lookup"><span data-stu-id="ebb2b-106">Developer audience</span></span>

<span data-ttu-id="ebb2b-107">In questo documento viene specificata l'interfaccia del provider WMI per la gestione e la configurazione di Crittografia unità BitLocker (BDE) e Trusted Platform Module (TPM) in Windows Server 2008 R2 e Windows Server 2008 per i server e Windows 7 e Windows Vista per i computer client.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-107">This document specifies the WMI provider interface for managing and configuring BitLocker Drive Encryption (BDE) and Trusted Platform Module (TPM) on Windows Server 2008 R2 and Windows Server 2008 for servers, and Windows 7 and Windows Vista for client computers.</span></span> <span data-ttu-id="ebb2b-108">È concepita per essere letta da quelli che scrivono script, elementi dell'interfaccia utente o altri strumenti di amministrazione per BDE o TPM.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-108">It is intended to be read by those writing scripts, user interface elements, or other administrative tools for BDE or the TPM.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="ebb2b-109">Requisiti di runtime</span><span class="sxs-lookup"><span data-stu-id="ebb2b-109">Run-time requirements</span></span>

<span data-ttu-id="ebb2b-110">Per i provider WMI di sicurezza è necessario specificare il file con estensione MOF con ogni provider e un sistema operativo supportato.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-110">The Security WMI Providers require the .mof file specified with each provider and a supported operating system.</span></span> <span data-ttu-id="ebb2b-111">Il sistema operativo minimo è Windows Server 2008 o Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-111">The minimum operating system is either Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ebb2b-112">Crittografia unità BitLocker è disponibile solo per le versioni Windows Vista Enterprise e Windows Vista Ultimate di Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-112">BitLocker Drive Encryption is only available for the Windows Vista Enterprise and Windows Vista Ultimate versions of Windows Vista.</span></span> <span data-ttu-id="ebb2b-113">Per informazioni sui requisiti della fase di esecuzione per un particolare elemento di programmazione, vedere la sezione requisiti della pagina di riferimento per tale elemento.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-113">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="ebb2b-114">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="ebb2b-114">In this section</span></span>



| <span data-ttu-id="ebb2b-115">Argomento</span><span class="sxs-lookup"><span data-stu-id="ebb2b-115">Topic</span></span>                                                                               | <span data-ttu-id="ebb2b-116">Descrizione</span><span class="sxs-lookup"><span data-stu-id="ebb2b-116">Description</span></span>                                                        |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="ebb2b-117">Informazioni sui provider WMI per la sicurezza</span><span class="sxs-lookup"><span data-stu-id="ebb2b-117">About Security WMI Providers</span></span>](about-security-wmi-providers.md)<br/>         | <span data-ttu-id="ebb2b-118">Breve panoramica dei provider WMI per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-118">Brief overview of the Security WMI Providers.</span></span><br/>           |
| [<span data-ttu-id="ebb2b-119">Guida di riferimento ai provider WMI di sicurezza</span><span class="sxs-lookup"><span data-stu-id="ebb2b-119">Security WMI Providers Reference</span></span>](security-wmi-providers-reference.md)<br/> | <span data-ttu-id="ebb2b-120">Documentazione di riferimento per i provider WMI per la sicurezza.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-120">Reference documentation for the Security WMI Providers.</span></span><br/> |



 

## <a name="additional-resources"></a><span data-ttu-id="ebb2b-121">Risorse aggiuntive</span><span class="sxs-lookup"><span data-stu-id="ebb2b-121">Additional resources</span></span>

<span data-ttu-id="ebb2b-122">Di seguito sono riportate altre risorse.</span><span class="sxs-lookup"><span data-stu-id="ebb2b-122">The following are additional resources.</span></span>



|                    |                                                                                                                                                                        |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebb2b-123">Classi</span><span class="sxs-lookup"><span data-stu-id="ebb2b-123">Classes</span></span><br/> | <span data-ttu-id="ebb2b-124">Per ulteriori informazioni sui provider WMI per la sicurezza, vedere [**Win32 \_ EncryptableVolume**](win32-encryptablevolume.md) e [**Win32 \_ TPM**](win32-tpm.md).</span><span class="sxs-lookup"><span data-stu-id="ebb2b-124">For more information about the Security WMI providers, see [**Win32\_EncryptableVolume**](win32-encryptablevolume.md) and [**Win32\_Tpm**](win32-tpm.md).</span></span><br/> |



 

 

 




