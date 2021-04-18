---
description: La sostituzione delle risorse protette è supportata tramite i meccanismi seguenti.
ms.assetid: a757e6cf-59df-4894-a0dc-40174b0aa147
title: Meccanismi di sostituzione delle risorse supportati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2aaaa1d9cc8d24d8cd172be71ee40790bf8161a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106317022"
---
# <a name="supported-resource-replacement-mechanisms"></a><span data-ttu-id="029ab-103">Meccanismi di sostituzione delle risorse supportati</span><span class="sxs-lookup"><span data-stu-id="029ab-103">Supported Resource Replacement Mechanisms</span></span>

<span data-ttu-id="029ab-104">La sostituzione delle risorse protette è supportata tramite i meccanismi seguenti.</span><span class="sxs-lookup"><span data-stu-id="029ab-104">Replacement of protected resources is supported through the following mechanisms.</span></span>

<span data-ttu-id="029ab-105">L'autorizzazione per l'accesso completo per la modifica di risorse protette da WRP in Windows Vista e Windows Server 2008 è limitata a TrustedInstaller con il servizio Windows Modules Installer usando i meccanismi seguenti:</span><span class="sxs-lookup"><span data-stu-id="029ab-105">Permission for full access to modify WRP-protected resources on Windows Vista and Windows Server 2008 is restricted to TrustedInstaller with the Windows Modules Installer service using the following mechanisms:</span></span>

-   <span data-ttu-id="029ab-106">Service Pack di Windows installati da TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="029ab-106">Windows Service Packs installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="029ab-107">Aggiornamenti rapidi installati da TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="029ab-107">Hotfixes installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="029ab-108">Aggiornamenti del sistema operativo installati da TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="029ab-108">Operating system upgrades installed by TrustedInstaller.</span></span>
-   <span data-ttu-id="029ab-109">Windows Update installato da TrustedInstaller.</span><span class="sxs-lookup"><span data-stu-id="029ab-109">Windows Update installed by TrustedInstaller.</span></span>

<span data-ttu-id="029ab-110">Le applicazioni e i programmi di installazione che tentano di sostituire una risorsa protetta da WRP per mezzo di questi metodi vengono negati per modificare la risorsa e generare un messaggio di errore di accesso negato.</span><span class="sxs-lookup"><span data-stu-id="029ab-110">Applications and installers attempting to replace a WRP-protected resource by means other than these specified methods are denied access to change the resource and generate an access denied error message.</span></span>

<span data-ttu-id="029ab-111">Per i programmi di installazione noti che tentano di sostituire le risorse protette con WRP, l'errore di accesso negato e il messaggio di errore possono essere eliminati.</span><span class="sxs-lookup"><span data-stu-id="029ab-111">For well-known installers attempting to replace WRP-protected resources, the access denied error and error message may be suppressed.</span></span> <span data-ttu-id="029ab-112">In questo caso, l'operazione viene restituita correttamente, i messaggi di errore e di errore vengono eliminati, ma non vengono applicate modifiche alla risorsa protetta da WRP.</span><span class="sxs-lookup"><span data-stu-id="029ab-112">In this case, the operation returns successfully, the error and error message are suppressed, but no changes are applied to the WRP-protected resource.</span></span> <span data-ttu-id="029ab-113">È possibile che l'errore venga eliminato per un programma di installazione noto solo quando vengono soddisfatti tutti i criteri seguenti:</span><span class="sxs-lookup"><span data-stu-id="029ab-113">The error may be suppressed for a well-known installer only when all of the following criteria are satisfied:</span></span>

-   <span data-ttu-id="029ab-114">Si tratta di un'applicazione legacy.</span><span class="sxs-lookup"><span data-stu-id="029ab-114">This is a legacy application.</span></span> <span data-ttu-id="029ab-115">L'applicazione non include un manifesto con un requestedExecutionlevel che identifica l'applicazione come progettata per Windows Vista o Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="029ab-115">The application does not include a manifest with a requestedExecutionlevel that identifies the application as designed for Windows Vista or Windows Server 2008.</span></span>
-   <span data-ttu-id="029ab-116">L'errore di accesso negato è causato solo dal tentativo di modificare una risorsa protetta da WRP.</span><span class="sxs-lookup"><span data-stu-id="029ab-116">The access denied error is caused only by the attempt to modify a WRP-protected resource.</span></span>
-   <span data-ttu-id="029ab-117">L'applicazione viene installata da un amministratore.</span><span class="sxs-lookup"><span data-stu-id="029ab-117">An Administrator is installing the application.</span></span>

<span data-ttu-id="029ab-118">Per informazioni sull'uso della Windows Installer con WRP, vedere [uso di Windows Installer e protezione risorse di Windows](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) in [Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK.</span><span class="sxs-lookup"><span data-stu-id="029ab-118">For information about using the Windows Installer with WRP, see [Using Windows Installer and Windows Resource Protection](/windows/desktop/Msi/windows-resource-protection-on-windows-vista) in the [Windows Installer](/windows/desktop/Msi/windows-installer-portal) SDK.</span></span>

<span data-ttu-id="029ab-119">**Windows Server 2003 e Windows XP:** La sostituzione dei file di sistema protetti da WFP è supportata solo tramite i meccanismi seguenti:</span><span class="sxs-lookup"><span data-stu-id="029ab-119">**Windows Server 2003 and Windows XP:** Replacement of WFP-protected system files is supported only through the following mechanisms:</span></span>

-   <span data-ttu-id="029ab-120">Installazione del Service Pack di Windows con Update.exe</span><span class="sxs-lookup"><span data-stu-id="029ab-120">Windows Service Pack installation using Update.exe</span></span>
-   <span data-ttu-id="029ab-121">Hotfix installati con Hotfix.exe</span><span class="sxs-lookup"><span data-stu-id="029ab-121">Hotfixes installed using Hotfix.exe</span></span>
-   <span data-ttu-id="029ab-122">Aggiornamenti del sistema operativo con Winnt32.exe</span><span class="sxs-lookup"><span data-stu-id="029ab-122">Operating system upgrades using Winnt32.exe</span></span>
-   <span data-ttu-id="029ab-123">Windows Update</span><span class="sxs-lookup"><span data-stu-id="029ab-123">Windows Update</span></span>

<span data-ttu-id="029ab-124">La sostituzione dei file protetti per mezzo di questi metodi diversi comporta l'esecuzione del ripristino dei file originali da parte di WFP.</span><span class="sxs-lookup"><span data-stu-id="029ab-124">Replacing protected files by means other than these specified methods results in the original files being restored by WFP.</span></span>

 

 
