---
description: Nelle finestre a 64 bit, le parti delle voci del registro di sistema vengono archiviate separatamente per le applicazioni a 32 bit e a 64 bit e sono mappate in visualizzazioni del registro di sistema logiche separate usando il redirector del registro di sistema e la reflection del registro di sistema, perché la versione a 64 bit di un'applicazione può usare chiavi e valori del registro di sistema diversi dalla versione a 32 Sono inoltre disponibili chiavi del registro di sistema condivise che non vengono reindirizzate o riflesse.
ms.assetid: 08dc034c-15ce-41d9-8e74-a49b61ad40a6
title: Dati dell'applicazione a 32 bit e a 64 bit nel registro di sistema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bc82dfbf9b22cf90866e13109aeea2bcdb10e27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882041"
---
# <a name="32-bit-and-64-bit-application-data-in-the-registry"></a><span data-ttu-id="2d066-104">Dati dell'applicazione a 32 bit e a 64 bit nel registro di sistema</span><span class="sxs-lookup"><span data-stu-id="2d066-104">32-bit and 64-bit Application Data in the Registry</span></span>

<span data-ttu-id="2d066-105">Nelle finestre a 64 bit, le parti delle voci del registro di sistema vengono archiviate separatamente per le applicazioni a 32 bit e a 64 bit e sono mappate in visualizzazioni del registro di sistema logiche separate usando il [redirector del registro di sistema](/windows/desktop/WinProg64/registry-redirector) e la [Reflection del registro](/windows/desktop/WinProg64/registry-reflection)di sistema, perché la versione a 64 bit di un'applicazione può usare chiavi e valori del registro di sistema diversi dalla versione a 32</span><span class="sxs-lookup"><span data-stu-id="2d066-105">On 64-bit Windows, portions of the registry entries are stored separately for 32-bit application and 64-bit applications and mapped into separate logical registry views using the [registry redirector](/windows/desktop/WinProg64/registry-redirector) and [registry reflection](/windows/desktop/WinProg64/registry-reflection), because the 64-bit version of an application may use different registry keys and values than the 32-bit version.</span></span> <span data-ttu-id="2d066-106">Sono inoltre disponibili [chiavi del registro di sistema condivise](/windows/desktop/WinProg64/shared-registry-keys) che non vengono reindirizzate o riflesse.</span><span class="sxs-lookup"><span data-stu-id="2d066-106">There are also [shared registry keys](/windows/desktop/WinProg64/shared-registry-keys) that are not redirected or reflected.</span></span>

<span data-ttu-id="2d066-107">L'elemento padre di ogni nodo del registro di sistema a 64 bit è il nodo Image-Specific o ISN.</span><span class="sxs-lookup"><span data-stu-id="2d066-107">The parent of each 64-bit registry node is the Image-Specific Node or ISN.</span></span> <span data-ttu-id="2d066-108">Il redirector del registro di sistema indirizza in modo trasparente l'accesso del registro di sistema di un'applicazione al sottonodo ISN appropriato.</span><span class="sxs-lookup"><span data-stu-id="2d066-108">The registry redirector transparently directs an application's registry access to the appropriate ISN subnode.</span></span> <span data-ttu-id="2d066-109">I sottonodi di reindirizzamento nell'albero del registro di sistema vengono creati automaticamente dal componente WOW64 usando il nome **Wow6432Node**.</span><span class="sxs-lookup"><span data-stu-id="2d066-109">Redirection subnodes in the registry tree are created automatically by the WOW64 component using the name **Wow6432Node**.</span></span> <span data-ttu-id="2d066-110">Di conseguenza, è essenziale non assegnare un nome alla chiave del registro di sistema creata **Wow6432Node**.</span><span class="sxs-lookup"><span data-stu-id="2d066-110">As a result, it is essential not to name any registry key you create **Wow6432Node**.</span></span>

<span data-ttu-id="2d066-111">I \_ \_ flag 64KEY WOW64 32KEY e chiave \_ WOW64 \_ abilitano l'accesso esplicito alla visualizzazione del registro di sistema a 64 bit e rispettivamente alla visualizzazione a 32 bit.</span><span class="sxs-lookup"><span data-stu-id="2d066-111">The KEY\_WOW64\_64KEY and KEY\_WOW64\_32KEY flags enable explicit access to the 64-bit registry view and the 32-bit view, respectively.</span></span> <span data-ttu-id="2d066-112">Per ulteriori informazioni, vedere [accesso a una visualizzazione del registro di sistema alternativa](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span><span class="sxs-lookup"><span data-stu-id="2d066-112">For more information, see [Accessing an Alternate Registry View](/windows/desktop/WinProg64/accessing-an-alternate-registry-view).</span></span>

<span data-ttu-id="2d066-113">Per disabilitare e abilitare la reflection del registro di sistema per una chiave specifica, usare le funzioni [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) e [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) .</span><span class="sxs-lookup"><span data-stu-id="2d066-113">To disable and enable registry reflection for a particular key, use the [**RegDisableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regdisablereflectionkey) and [**RegEnableReflectionKey**](/windows/desktop/api/Winreg/nf-winreg-regenablereflectionkey) functions.</span></span> <span data-ttu-id="2d066-114">Le applicazioni devono disabilitare la reflection solo per le chiavi del registro di sistema create e non tentare di disabilitare la reflection per le chiavi predefinite, ad esempio il **\_ \_ computer locale HKEY** o l' **\_ \_ utente corrente di HKEY**.</span><span class="sxs-lookup"><span data-stu-id="2d066-114">Applications should disable reflection only for the registry keys that they create and not attempt to disable reflection for the predefined keys such as **HKEY\_LOCAL\_MACHINE** or **HKEY\_CURRENT\_USER**.</span></span> <span data-ttu-id="2d066-115">Per determinare quali chiavi si trovano nell'elenco Reflection, usare la funzione [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) .</span><span class="sxs-lookup"><span data-stu-id="2d066-115">To determine which keys are on the reflection list, use the [**RegQueryReflectionKey**](/windows/desktop/api/WinReg/nf-winreg-regqueryreflectionkey) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2d066-116">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="2d066-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2d066-117">redirector del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="2d066-117">registry redirector</span></span>](/windows/desktop/WinProg64/registry-redirector)
</dt> <dt>

[<span data-ttu-id="2d066-118">Reflection del registro di sistema</span><span class="sxs-lookup"><span data-stu-id="2d066-118">registry reflection</span></span>](/windows/desktop/WinProg64/registry-reflection)
</dt> </dl>

 

 
