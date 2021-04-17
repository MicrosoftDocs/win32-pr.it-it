---
title: Classi e server
description: Classi e server
ms.assetid: cc88be56-0d96-47d2-b23b-6a6ad376bdae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d319fd985b812692e6d0bfc421c4bb9da2a2605c
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104399775"
---
# <a name="classes-and-servers"></a><span data-ttu-id="91327-103">Classi e server</span><span class="sxs-lookup"><span data-stu-id="91327-103">Classes and Servers</span></span>

<span data-ttu-id="91327-104">COM utilizza **la \_ \_ radice delle classi HKEY** per le impostazioni a livello di computer, ma consente anche la configurazione per utente dei CLSID per una maggiore sicurezza e flessibilità.</span><span class="sxs-lookup"><span data-stu-id="91327-104">COM uses **HKEY\_CLASSES\_ROOT** for computer-wide settings but also allows per-user configuration of CLSIDS for greater security and flexibility.</span></span> <span data-ttu-id="91327-105">COM innanzitutto consulta **\_ \_ \\ \\ le classi del software utente corrente di HKEY** prima di cercare nella **\_ \_ radice delle classi HKEY**.</span><span class="sxs-lookup"><span data-stu-id="91327-105">COM first consults **HKEY\_CURRENT\_USER\\Software\\Classes** before looking under **HKEY\_CLASSES\_ROOT**.</span></span> <span data-ttu-id="91327-106">COM mantiene le informazioni a livello di computer correlate ai CLSID **nel \_ \_ \\ CLSID radice delle classi HKEY** e mantiene le informazioni sulle classi per utente in **HKEY \_ \_ \\ classi software utente correnti \\ \\ CLSID**.</span><span class="sxs-lookup"><span data-stu-id="91327-106">COM keeps computer-wide information related to CLSIDs under **HKEY\_CLASSES\_ROOT\\CLSID** and keeps per-user class information under **HKEY\_CURRENT\_USER\\Software\\Classes\\CLSID**.</span></span>

<span data-ttu-id="91327-107">I server COM supportano la registrazione automatica.</span><span class="sxs-lookup"><span data-stu-id="91327-107">COM servers support self-registration.</span></span> <span data-ttu-id="91327-108">Per un server in-process, significa che la DLL deve esportare le funzioni seguenti:</span><span class="sxs-lookup"><span data-stu-id="91327-108">For an in-process server, this means that the DLL must export the following functions:</span></span>

-   [<span data-ttu-id="91327-109">**DllRegisterServer**</span><span class="sxs-lookup"><span data-stu-id="91327-109">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)
-   [<span data-ttu-id="91327-110">**DllUnregisterServer**</span><span class="sxs-lookup"><span data-stu-id="91327-110">**DllUnregisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllunregisterserver)

<span data-ttu-id="91327-111">È necessario esportare in modo esplicito queste funzioni utilizzando un file di definizione del modulo, commutatori del linker o direttive del compilatore.</span><span class="sxs-lookup"><span data-stu-id="91327-111">You must explicitly export these functions by using a module definition file, linker switches, or compiler directives.</span></span> <span data-ttu-id="91327-112">L'archivio classi utilizza queste funzioni per configurare il registro di sistema locale dopo il download del file nel computer client.</span><span class="sxs-lookup"><span data-stu-id="91327-112">The class store uses these functions to configure the local registry after downloading the file to the client machine.</span></span> <span data-ttu-id="91327-113">Oltre all'archivio classi, queste funzioni vengono usate anche da altri ambienti per installare i server nei computer host.</span><span class="sxs-lookup"><span data-stu-id="91327-113">In addition to class store, these functions are also used by other environments to install servers on host computers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="91327-114">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="91327-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91327-115">Registrazione di applicazioni COM</span><span class="sxs-lookup"><span data-stu-id="91327-115">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 