---
description: L'impostazione del criterio TransformsSecure su 1 informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache localmente nel computer dell'utente in una posizione in cui l'utente non dispone dell'accesso in scrittura.
ms.assetid: 4fe992ed-1e8c-4ee2-a325-138bdc039e44
title: Criteri di TransformsSecure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69180c797008f34755cfa415c7a76fb5f7721f30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878546"
---
# <a name="transformssecure-policy"></a><span data-ttu-id="71380-103">Criteri di TransformsSecure</span><span class="sxs-lookup"><span data-stu-id="71380-103">TransformsSecure Policy</span></span>

<span data-ttu-id="71380-104">L'impostazione del criterio TransformsSecure su 1 informa il programma di installazione che le trasformazioni devono essere memorizzate nella cache localmente nel computer dell'utente in una posizione in cui l'utente non dispone dell'accesso in scrittura.</span><span class="sxs-lookup"><span data-stu-id="71380-104">Setting the TransformsSecure policy to 1 informs the installer that transforms are to be cached locally on the user's computer in a location where the user does not have write access.</span></span> <span data-ttu-id="71380-105">L'impostazione di questo criterio equivale all'impostazione della [Proprietà TRANSFORMSSECURE](transformssecure.md) , ad eccezione del fatto che l'ambito è diverso.</span><span class="sxs-lookup"><span data-stu-id="71380-105">Setting this policy is the same as setting the [TRANSFORMSSECURE property](transformssecure.md) except the scope is different.</span></span> <span data-ttu-id="71380-106">L'impostazione del criterio TransformsSecure si applica a tutti i pacchetti installati in un determinato computer.</span><span class="sxs-lookup"><span data-stu-id="71380-106">Setting TransformsSecure policy applies to all packages installed to a given computer.</span></span> <span data-ttu-id="71380-107">L'impostazione della proprietà TRANSFORMSSECURE si applica al pacchetto indipendentemente dal computer.</span><span class="sxs-lookup"><span data-stu-id="71380-107">Setting the TRANSFORMSSECURE property applies to the package regardless of the computer.</span></span>

<span data-ttu-id="71380-108">Lo scopo di questo criterio è fornire un'archiviazione sicura delle trasformazioni con gli utenti in viaggio di Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="71380-108">The purpose of this policy is to provide for secure transform storage with traveling users of Windows 2000.</span></span> <span data-ttu-id="71380-109">A partire da Windows Server 2003, il valore predefinito di questo criterio è 1.</span><span class="sxs-lookup"><span data-stu-id="71380-109">Beginning with Windows Server 2003, the default value of this policy is 1.</span></span>

<span data-ttu-id="71380-110">Quando questo criterio è impostato, un' [installazione di manutenzione](maintenance-installation.md) può utilizzare la trasformazione solo dalla cache protetta.</span><span class="sxs-lookup"><span data-stu-id="71380-110">When this policy is set, a [maintenance installation](maintenance-installation.md) can only use the transform from the secured cache.</span></span> <span data-ttu-id="71380-111">Nel caso in cui il programma di installazione rilevi che la trasformazione non è presente nel computer locale, il programma di installazione tenta di ripristinare la trasformazione.</span><span class="sxs-lookup"><span data-stu-id="71380-111">In the event that the installer finds that the transform is missing on the local computer, the installer attempts to restore the transform.</span></span> <span data-ttu-id="71380-112">Per consentire al programma di installazione di ripristinare la trasformazione, la trasformazione protetta deve trovarsi in un'origine autorizzata nell'elenco di origine del pacchetto di installazione.</span><span class="sxs-lookup"><span data-stu-id="71380-112">In order for the installer to restore the transform, the secure transform must reside at an authorized source in the installation package's source list.</span></span> <span data-ttu-id="71380-113">Per altre informazioni, vedere [resilienza dell'origine](source-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="71380-113">For more information, see [Source Resiliency](source-resiliency.md).</span></span> <span data-ttu-id="71380-114">L'installazione di manutenzione ha esito negativo se la trasformazione non è disponibile o non può essere caricata.</span><span class="sxs-lookup"><span data-stu-id="71380-114">The maintenance installation fails if the transform is unavailable or cannot be loaded.</span></span>

<span data-ttu-id="71380-115">In Windows Server 2003, se questo criterio non è impostato, il comportamento predefinito consiste nell'archiviare le trasformazioni in una posizione sicura.</span><span class="sxs-lookup"><span data-stu-id="71380-115">On Windows Server 2003, if this policy is not set, the default behavior is to store the transforms in a secure location.</span></span> <span data-ttu-id="71380-116">In tutte le versioni precedenti a Windows Server 2003, se il criterio non è impostato, il comportamento predefinito consiste nell'archiviare le trasformazioni nel profilo utenti.</span><span class="sxs-lookup"><span data-stu-id="71380-116">On all versions prior to Windows Server 2003, if the policy is not set, the default behavior is to store the transforms in the users profile.</span></span>

<span data-ttu-id="71380-117">Per ulteriori informazioni, vedere anche [trasformazioni protette](secured-transforms.md) .</span><span class="sxs-lookup"><span data-stu-id="71380-117">See also [Secured Transforms](secured-transforms.md) for more information.</span></span>

<span data-ttu-id="71380-118">Windows Installer interpreta il [criterio TransformsAtSource](transformsatsource-policy.md) in modo che corrisponda al criterio TRANSFORMSSECURE.</span><span class="sxs-lookup"><span data-stu-id="71380-118">Windows Installer interprets the [TransformsAtSource policy](transformsatsource-policy.md) to be the same as the TransformsSecure policy.</span></span>

## <a name="registry-key"></a><span data-ttu-id="71380-119">Chiave del Registro di sistema</span><span class="sxs-lookup"><span data-stu-id="71380-119">Registry Key</span></span>

<span data-ttu-id="71380-120">**HKEY \_ Criteri software del \_ computer locale** \\  \\  \\ **Microsoft** \\ **Windows** \\ **Installer**</span><span class="sxs-lookup"><span data-stu-id="71380-120">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Policies**\\**Microsoft**\\**Windows**\\**Installer**</span></span>

## <a name="data-type"></a><span data-ttu-id="71380-121">Tipo di dati</span><span class="sxs-lookup"><span data-stu-id="71380-121">Data Type</span></span>

<span data-ttu-id="71380-122">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="71380-122">**REG\_DWORD**</span></span>

## <a name="related-topics"></a><span data-ttu-id="71380-123">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="71380-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="71380-124">Non supportato in Windows Installer 2,0 e versioni precedenti</span><span class="sxs-lookup"><span data-stu-id="71380-124">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



