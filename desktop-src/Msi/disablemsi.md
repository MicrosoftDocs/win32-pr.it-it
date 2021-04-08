---
description: Se il valore di questo criterio del sistema per computer è impostato su &\# 0034; 2&\# 0034; il programma di installazione è sempre disabilitato per tutte le applicazioni. Se il valore di questo criterio è impostato su &\# 0034; 1&\# 0034;, il programma di installazione è disabilitato per le applicazioni non gestite, ma è ancora abilitato per le applicazioni gestite.
ms.assetid: 7f941559-54c3-4802-b827-5954bd4669f8
title: DisableMSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dbf8a784f5e8090bf6ba2007091c22cf4bc070c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104050151"
---
# <a name="disablemsi"></a><span data-ttu-id="3ce39-104">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="3ce39-104">DisableMSI</span></span>

<span data-ttu-id="3ce39-105">Se il valore di questo [criterio di sistema](system-policy.md) per computer è impostato su "2", il programma di installazione è sempre disabilitato per tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3ce39-105">If the value of this per-machine [system policy](system-policy.md) is set to "2" the installer is always disabled for all applications.</span></span> <span data-ttu-id="3ce39-106">Se il valore di questo criterio è impostato su "1", il programma di installazione viene disabilitato per le applicazioni non gestite, ma è ancora abilitato per le applicazioni gestite.</span><span class="sxs-lookup"><span data-stu-id="3ce39-106">If this policy value is set to "1", the installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span>

<span data-ttu-id="3ce39-107">Nella tabella seguente sono elencate le configurazioni possibili.</span><span class="sxs-lookup"><span data-stu-id="3ce39-107">The following table lists the possible configurations.</span></span>



| <span data-ttu-id="3ce39-108">DisableMSI</span><span class="sxs-lookup"><span data-stu-id="3ce39-108">DisableMSI</span></span> | <span data-ttu-id="3ce39-109">Descrizione</span><span class="sxs-lookup"><span data-stu-id="3ce39-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ce39-110">*Default*</span><span class="sxs-lookup"><span data-stu-id="3ce39-110">*Default*</span></span>  | <span data-ttu-id="3ce39-111">In Windows Server 2003, Windows Server 2003 R2, Windows Server 2008 e Windows Server 2008 R2, se il valore dei criteri è null, assente o un numero diverso da 1 o 2, il Windows Installer è abilitato per le applicazioni gestite.</span><span class="sxs-lookup"><span data-stu-id="3ce39-111">On Windows Server 2003, Windows Server 2003 R2, Windows Server 2008, and Windows Server 2008 R2, if the policy value is Null, absent, or any number other than 1 or 2, the Windows Installer is enabled for managed applications.</span></span> <span data-ttu-id="3ce39-112">Le installazioni di applicazioni non gestite sono bloccate.</span><span class="sxs-lookup"><span data-stu-id="3ce39-112">Unmanaged application installs are blocked.</span></span><br/> <span data-ttu-id="3ce39-113">In Windows XP, Windows Vista e Windows 7, il Windows Installer è abilitato per tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3ce39-113">On Windows XP, Windows Vista, and Windows 7, the Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="3ce39-114">Sono consentite tutte le operazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="3ce39-114">All install operations are allowed.</span></span><br/> |
| <span data-ttu-id="3ce39-115">0</span><span class="sxs-lookup"><span data-stu-id="3ce39-115">0</span></span>          | <span data-ttu-id="3ce39-116">Windows Installer è abilitato per tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3ce39-116">Windows Installer is enabled for all applications.</span></span> <span data-ttu-id="3ce39-117">Sono consentite tutte le operazioni di installazione.</span><span class="sxs-lookup"><span data-stu-id="3ce39-117">All install operations are allowed.</span></span>                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="3ce39-118">1</span><span class="sxs-lookup"><span data-stu-id="3ce39-118">1</span></span>          | <span data-ttu-id="3ce39-119">Il Windows Installer è disabilitato per le applicazioni non gestite, ma è ancora abilitato per le applicazioni gestite.</span><span class="sxs-lookup"><span data-stu-id="3ce39-119">The Windows Installer is disabled for unmanaged applications but is still enabled for managed applications.</span></span> <span data-ttu-id="3ce39-120">Le installazioni per utente non elevate sono bloccate.</span><span class="sxs-lookup"><span data-stu-id="3ce39-120">Non-elevated per-user installations are blocked.</span></span> <span data-ttu-id="3ce39-121">Sono consentite installazioni con privilegi elevati e computer per utente.</span><span class="sxs-lookup"><span data-stu-id="3ce39-121">Per-user elevated and per-machine installs are allowed.</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="3ce39-122">2</span><span class="sxs-lookup"><span data-stu-id="3ce39-122">2</span></span>          | <span data-ttu-id="3ce39-123">Windows Installer è sempre disabilitato per tutte le applicazioni.</span><span class="sxs-lookup"><span data-stu-id="3ce39-123">Windows Installer is always disabled for all applications.</span></span> <span data-ttu-id="3ce39-124">Non sono consentite installazioni, tra cui riparazioni, reinstallazioni o installazioni su richiesta.</span><span class="sxs-lookup"><span data-stu-id="3ce39-124">No installs are allowed including repairs, reinstalls, or on-demand installations.</span></span>                                                                                                                                                                                                                                                                                               |



 

## <a name="registry-key"></a><span data-ttu-id="3ce39-125">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="3ce39-125">Registry Key</span></span>

<span data-ttu-id="3ce39-126">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="3ce39-126">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="3ce39-127">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="3ce39-127">Data Type</span></span>

<span data-ttu-id="3ce39-128">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="3ce39-128">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ce39-129">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="3ce39-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ce39-130">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="3ce39-130">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




