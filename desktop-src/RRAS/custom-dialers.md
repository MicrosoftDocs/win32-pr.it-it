---
title: Dialer personalizzati
description: I sistemi operativi Windows 2000 e versioni successive consentono agli sviluppatori di fornire i propri dialers personalizzati che funzionano con il servizio di accesso remoto (RAS).
ms.assetid: ad94f38d-812f-4329-8055-6274a21a3242
keywords:
- Dialer personalizzati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 35293de408a2a0faa146b93f9b5d5ebccf447acc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104223973"
---
# <a name="custom-dialers"></a><span data-ttu-id="908e2-104">Dialer personalizzati</span><span class="sxs-lookup"><span data-stu-id="908e2-104">Custom Dialers</span></span>

<span data-ttu-id="908e2-105">I sistemi operativi Windows 2000 e versioni successive consentono agli sviluppatori di fornire i propri dialers personalizzati che funzionano con il servizio di accesso remoto (RAS).</span><span class="sxs-lookup"><span data-stu-id="908e2-105">Windows 2000 and later operating systems enable developers to provide their own custom dialers that work with the Remote Access Service (RAS).</span></span> <span data-ttu-id="908e2-106">Il dialer personalizzato viene implementato come una singola libreria di collegamento dinamico (DLL) che esporta i punti di ingresso seguenti:</span><span class="sxs-lookup"><span data-stu-id="908e2-106">The custom dialer is implemented as a single dynamic-link library (DLL) that exports the following entry points:</span></span>

-   [<span data-ttu-id="908e2-107">**RasCustomDial**</span><span class="sxs-lookup"><span data-stu-id="908e2-107">**RasCustomDial**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdialfn)
-   [<span data-ttu-id="908e2-108">**RasCustomDialDlg**</span><span class="sxs-lookup"><span data-stu-id="908e2-108">**RasCustomDialDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomdialdlgfn)
-   [<span data-ttu-id="908e2-109">**RasCustomHangup**</span><span class="sxs-lookup"><span data-stu-id="908e2-109">**RasCustomHangup**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomhangupfn)
-   [<span data-ttu-id="908e2-110">**RasCustomEntryDlg**</span><span class="sxs-lookup"><span data-stu-id="908e2-110">**RasCustomEntryDlg**</span></span>](/windows/desktop/api/Rasdlg/nc-rasdlg-rascustomentrydlgfn)
-   [<span data-ttu-id="908e2-111">**RasCustomDeleteEntryNotify**</span><span class="sxs-lookup"><span data-stu-id="908e2-111">**RasCustomDeleteEntryNotify**</span></span>](/windows/desktop/api/Ras/nc-ras-rascustomdeleteentrynotifyfn)

<span data-ttu-id="908e2-112">La DLL di connessione personalizzata deve esportare tutti questi punti di ingresso e deve implementare i punti di ingresso come funzioni Unicode.</span><span class="sxs-lookup"><span data-stu-id="908e2-112">The custom-dial DLL must export all of these entry points, and it must implement the entry points as Unicode functions.</span></span> <span data-ttu-id="908e2-113">Per ulteriori informazioni su queste funzioni, vedere la pagina di riferimento per ogni funzione nel riferimento al servizio Windows SDK Remote Access.</span><span class="sxs-lookup"><span data-stu-id="908e2-113">For more information about these functions, see the reference page for each function in the Windows SDK Remote Access Service Reference.</span></span>

<span data-ttu-id="908e2-114">Per consentire a una connessione RAS di utilizzare il dialer personalizzato, è necessario che la voce del libro telefonico per la connessione contenga il percorso della DLL di composizione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="908e2-114">In order for a RAS connection to use the custom dialer, the phone-book entry for the connection must contain the path to the custom-dial DLL.</span></span> <span data-ttu-id="908e2-115">Usare le funzioni API RAS [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) e [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) per impostare questo percorso nel membro **szCustomDialDll** della struttura [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) per la voce della rubrica telefonica.</span><span class="sxs-lookup"><span data-stu-id="908e2-115">Use the RAS API functions [**RasGetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rasgetentrypropertiesa) and [**RasSetEntryProperties**](/windows/desktop/api/Ras/nf-ras-rassetentrypropertiesa) to set this path in the **szCustomDialDll** member of the [**RASENTRY**](/previous-versions/windows/desktop/legacy/aa377274(v=vs.85)) structure for the phone-book entry.</span></span>

## <a name="updating-the-registry-for-custom-dialers"></a><span data-ttu-id="908e2-116">Aggiornamento del registro di sistema per i dialer personalizzati</span><span class="sxs-lookup"><span data-stu-id="908e2-116">Updating the Registry for Custom Dialers</span></span>

<span data-ttu-id="908e2-117">Per consentire al sistema di comporre una connessione che utilizza un dialer personalizzato, è necessario che il percorso della DLL della connessione personalizzata esista nel seguente valore del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="908e2-117">In order for the system to dial a connection that uses a custom dialer, the path to the custom-dial DLL must exist in the following registry value.</span></span>

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               Parameters
                  CustomDLL<dl>
<dt>

                  Data type
</dt>
<dd>                  REG_MULTI_SZ</dd>
</dl>
```

<span data-ttu-id="908e2-118">Poiché **CustomDLL** è di tipo **reg \_ multi \_ SZ**, può mantenere i percorsi di più DLL di composizione personalizzata.</span><span class="sxs-lookup"><span data-stu-id="908e2-118">Because **CustomDLL** is of type **REG\_MULTI\_SZ**, it can hold paths to multiple custom-dial DLLs.</span></span> <span data-ttu-id="908e2-119">È necessario impostare il percorso della DLL di composizione personalizzata in questo valore del registro di sistema, oltre alla voce della Rubrica per la connessione.</span><span class="sxs-lookup"><span data-stu-id="908e2-119">You need to set the path to the custom-dial DLL in this registry value, in addition to the phone-book entry for the connection.</span></span>

<span data-ttu-id="908e2-120">Per impostazione predefinita, questo valore del registro di sistema è scrivibile solo da un utente con privilegi di amministratore o di sistema.</span><span class="sxs-lookup"><span data-stu-id="908e2-120">By default, this registry value is writeable only by a user with Administrator or System privileges.</span></span> <span data-ttu-id="908e2-121">Per motivi di sicurezza, non modificare le autorizzazioni per questa chiave del registro di sistema.</span><span class="sxs-lookup"><span data-stu-id="908e2-121">For security reasons, do not change the permissions on this registry key.</span></span>

## <a name="using-custom-dialers-at-system-logon"></a><span data-ttu-id="908e2-122">Uso di dialer personalizzati all'accesso al sistema</span><span class="sxs-lookup"><span data-stu-id="908e2-122">Using Custom Dialers at System Logon</span></span>

<span data-ttu-id="908e2-123">I sistemi operativi Windows 2000 e versioni successive consentono a un utente di stabilire una connessione RAS al momento dell'accesso.</span><span class="sxs-lookup"><span data-stu-id="908e2-123">Windows 2000 and later operating systems allow a user to establish a RAS connection at the time of logon.</span></span> <span data-ttu-id="908e2-124">A tale scopo, l'utente controlla l' **accesso tramite la rete remota** nella finestra di dialogo **informazioni di accesso** .</span><span class="sxs-lookup"><span data-stu-id="908e2-124">To do so, the user checks **Logon using Dial-up Networking** in the **Logon Information** dialog box.</span></span> <span data-ttu-id="908e2-125">Quando l'utente fa clic sul pulsante OK, il sistema Visualizza le connessioni disponibili.</span><span class="sxs-lookup"><span data-stu-id="908e2-125">After the user clicks the Okay button, the system displays the available connections.</span></span>

## <a name="security-considerations"></a><span data-ttu-id="908e2-126">Considerazioni relative alla sicurezza</span><span class="sxs-lookup"><span data-stu-id="908e2-126">Security Considerations</span></span>

<span data-ttu-id="908e2-127">Nella maggior parte dei casi, un dialer personalizzato opera con i privilegi di sicurezza dell'utente che lo richiama.</span><span class="sxs-lookup"><span data-stu-id="908e2-127">In most cases, a custom dialer operates with the security privileges of the user that invokes it.</span></span> <span data-ttu-id="908e2-128">Tuttavia, se il dialer personalizzato viene richiamato al momento dell'accesso, agisce con i privilegi di sistema.</span><span class="sxs-lookup"><span data-stu-id="908e2-128">However, if the custom dialer is invoked at logon, it operates with system privileges.</span></span> <span data-ttu-id="908e2-129">Pertanto, progettare il dialer personalizzato in modo che non possa essere utilizzato per violare la sicurezza del sistema.</span><span class="sxs-lookup"><span data-stu-id="908e2-129">Therefore, design the custom dialer so that it cannot be used to violate system security.</span></span> <span data-ttu-id="908e2-130">Il dialer, ad esempio, non deve presentare un'interfaccia utente che consente all'utente di accedere in scrittura al file system del computer.</span><span class="sxs-lookup"><span data-stu-id="908e2-130">For example, the dialer should not present a user interface that allows the user write access to the computer's file system.</span></span> <span data-ttu-id="908e2-131">Le interfacce utente che forniscono tali accessi includono la finestra di dialogo **Trova file** , la finestra di dialogo **file-Apri** comune e la **Guida** di Windows.</span><span class="sxs-lookup"><span data-stu-id="908e2-131">User interfaces that provide such access include the **Find-File** dialog, the **File-Open** common dialog, and Windows **Help**.</span></span>

## <a name="custom-dialer-user-interface-must-support-idcancel"></a><span data-ttu-id="908e2-132">L'interfaccia utente del dialer personalizzato deve supportare IDCANCEL</span><span class="sxs-lookup"><span data-stu-id="908e2-132">Custom Dialer User Interface Must Support IDCANCEL</span></span>

<span data-ttu-id="908e2-133">Se il dialer personalizzato Visualizza un'interfaccia utente, l'interfaccia utente deve supportare \_ i messaggi di comando WM in cui LOWORD (*wParam*) è uguale a IDCANCEL.</span><span class="sxs-lookup"><span data-stu-id="908e2-133">If the custom dialer displays a user interface, the user interface must support WM\_COMMAND messages where LOWORD(*wParam*) equals IDCANCEL.</span></span>

 

 