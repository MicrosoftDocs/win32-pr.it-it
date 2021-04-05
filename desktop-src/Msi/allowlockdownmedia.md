---
description: L'impostazione del valore di questo criterio di sistema per computer su &\# 0034; 1&\# 0034; consente agli utenti non amministratori di installare applicazioni gestite da origini archiviate in supporti, ad esempio un CD-ROM.
ms.assetid: 9eac7520-0ba3-4529-a80b-010447a5b5e7
title: AllowLockdownMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5be1a5ba06db0a484a55a6e18e5419dee951fc38
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "103886030"
---
# <a name="allowlockdownmedia"></a><span data-ttu-id="26cd9-103">AllowLockdownMedia</span><span class="sxs-lookup"><span data-stu-id="26cd9-103">AllowLockdownMedia</span></span>

<span data-ttu-id="26cd9-104">L'impostazione del valore di questo criterio di [sistema](system-policy.md) per computer su "1" consente agli utenti non amministratori di installare [*applicazioni gestite*](m-gly.md) da origini archiviate su supporti, ad esempio un CD-ROM.</span><span class="sxs-lookup"><span data-stu-id="26cd9-104">Setting the value of this per-machine [system policy](system-policy.md) to "1", enables nonadministrative users to install [*managed applications*](m-gly.md) from sources stored on media, such as a CD-ROM.</span></span> <span data-ttu-id="26cd9-105">Vedere [resilienza del codice sorgente](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="26cd9-105">See [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="26cd9-106">Se, ad esempio, questo criterio è impostato, un utente non amministratore può utilizzare un'origine multimediale per installare le applicazioni assegnate o pubblicate o installate per tutti gli utenti.</span><span class="sxs-lookup"><span data-stu-id="26cd9-106">For example, if this policy is set, a nonadministrative user may use a media source to install assigned or published applications or applications being installed for all users.</span></span> <span data-ttu-id="26cd9-107">L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi con privilegi LocalSystem durante un'installazione con privilegi elevati.</span><span class="sxs-lookup"><span data-stu-id="26cd9-107">Setting this policy also enables nonadministrative users to run programs at LocalSystem privileges during an elevated installation.</span></span>

<span data-ttu-id="26cd9-108">Il valore predefinito di questo criterio è 1 solo nei computer che eseguono Windows Vista e che non sono aggiunti a un dominio.</span><span class="sxs-lookup"><span data-stu-id="26cd9-108">The default value of this policy is 1 only on computers running Windows Vista and that are not joined to a domain.</span></span> <span data-ttu-id="26cd9-109">Il valore predefinito di altri computer è che gli utenti non amministratori non possono installare le applicazioni gestite da un'origine situata nei supporti.</span><span class="sxs-lookup"><span data-stu-id="26cd9-109">The default on other computers is that nonadministrative users cannot install managed applications from a source located on media.</span></span>

<span data-ttu-id="26cd9-110">Poiché questo criterio consente agli utenti che non sono amministratori di installare con privilegi che non dispongono per impostazione predefinita, prima di impostare questo criterio è necessario valutare se fornisce un livello di sicurezza appropriato per l'utente.</span><span class="sxs-lookup"><span data-stu-id="26cd9-110">Because this policy enables users that are not an administrator to install with privileges they do not have by default, before setting this policy you should consider whether it provides an appropriate level of security for your user.</span></span> <span data-ttu-id="26cd9-111">L'impostazione predefinita è consigliata per garantire un ambiente protetto.</span><span class="sxs-lookup"><span data-stu-id="26cd9-111">The default setting is recommended to ensure a secure environment.</span></span>

<span data-ttu-id="26cd9-112">Per ulteriori informazioni sulla protezione delle installazioni e sull'utilizzo di certificati digitali, vedere [linee guida per la creazione di installazioni protette](guidelines-for-authoring-secure-installations.md) e [firme digitali e Windows Installer](digital-signatures-and-windows-installer.md) e [il download di un'installazione da Internet](downloading-an-installation-from-the-internet.md).</span><span class="sxs-lookup"><span data-stu-id="26cd9-112">For more information about securing installations and using digital certificates see [Guidelines for Authoring Secure Installations](guidelines-for-authoring-secure-installations.md) and [Digital Signatures and Windows Installer](digital-signatures-and-windows-installer.md) and [Downloading an Installation from the Internet](downloading-an-installation-from-the-internet.md).</span></span>

## <a name="registry-key"></a><span data-ttu-id="26cd9-113">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="26cd9-113">Registry Key</span></span>

<span data-ttu-id="26cd9-114">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="26cd9-114">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="26cd9-115">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="26cd9-115">Data Type</span></span>

<span data-ttu-id="26cd9-116">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="26cd9-116">**REG\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="26cd9-117">Commenti</span><span class="sxs-lookup"><span data-stu-id="26cd9-117">Remarks</span></span>

<span data-ttu-id="26cd9-118">L'impostazione di questo criterio consente inoltre agli utenti non amministratori di eseguire programmi arbitrari con privilegi LocalSystem se dispongono di un pacchetto di Windows Installer per l'installazione o l'avvio di tali programmi.</span><span class="sxs-lookup"><span data-stu-id="26cd9-118">Setting this policy also enables nonadministrative users to run arbitrary programs at LocalSystem privileges if they have a Windows Installer package that installs or launches those programs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="26cd9-119">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="26cd9-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="26cd9-120">Resilienza di origine</span><span class="sxs-lookup"><span data-stu-id="26cd9-120">Source Resiliency</span></span>](source-resiliency.md)
</dt> <dt>

[<span data-ttu-id="26cd9-121">AllowLockdownBrowse</span><span class="sxs-lookup"><span data-stu-id="26cd9-121">AllowLockdownBrowse</span></span>](allowlockdownbrowse.md)
</dt> </dl>

 

 



