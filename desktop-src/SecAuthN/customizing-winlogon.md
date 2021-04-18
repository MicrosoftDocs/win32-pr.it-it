---
description: Personalizzare il comportamento di Winlogon implementando un provider di credenziali.
ms.assetid: 70b47e29-c755-4c59-a493-d7fcbbc94b83
title: Personalizzazione di Winlogon
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64da4baae9b52dd53e288c631f35d33ea5a3085
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106308153"
---
# <a name="customizing-winlogon"></a><span data-ttu-id="9cb01-103">Personalizzazione di Winlogon</span><span class="sxs-lookup"><span data-stu-id="9cb01-103">Customizing Winlogon</span></span>

<span data-ttu-id="9cb01-104">Personalizzare il comportamento di [*Winlogon*](/windows/desktop/SecGloss/w-gly) implementando un provider di credenziali.</span><span class="sxs-lookup"><span data-stu-id="9cb01-104">Customize [*Winlogon*](/windows/desktop/SecGloss/w-gly) behavior by implementing a Credential Provider.</span></span> <span data-ttu-id="9cb01-105">Per informazioni sui provider di credenziali, vedere [**interfaccia ICredentialProvider**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span><span class="sxs-lookup"><span data-stu-id="9cb01-105">For information about Credential Providers, see [**ICredentialProvider Interface**](/windows/win32/api/credentialprovider/nn-credentialprovider-icredentialprovider).</span></span>

<span data-ttu-id="9cb01-106">**Windows Server 2003 e Windows XP:** I provider di credenziali non sono supportati.</span><span class="sxs-lookup"><span data-stu-id="9cb01-106">**Windows Server 2003 and Windows XP:** Credential Providers are not supported.</span></span>

<span data-ttu-id="9cb01-107">Nelle sezioni seguenti vengono descritte le modalità di personalizzazione di Winlogon nelle versioni di Windows precedenti a Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9cb01-107">The following sections describe ways to customize Winlogon in Windows versions prior to Windows Vista.</span></span>

> [!Note]  
> <span data-ttu-id="9cb01-108">Le DLL GINA e i pacchetti di notifica Winlogon vengono ignorati in Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="9cb01-108">GINA DLLs and Winlogon notification packages are ignored in Windows Vista.</span></span>

 

-   [<span data-ttu-id="9cb01-109">Pacchetti di notifica di Winlogon</span><span class="sxs-lookup"><span data-stu-id="9cb01-109">Winlogon Notification Packages</span></span>](#winlogon-notification-packages)
-   [<span data-ttu-id="9cb01-110">Stub GINA</span><span class="sxs-lookup"><span data-stu-id="9cb01-110">GINA Stubs</span></span>](#gina-stubs)
-   [<span data-ttu-id="9cb01-111">Hook GINA</span><span class="sxs-lookup"><span data-stu-id="9cb01-111">GINA Hooks</span></span>](#gina-hooks)

## <a name="winlogon-notification-packages"></a><span data-ttu-id="9cb01-112">Pacchetti di notifica di Winlogon</span><span class="sxs-lookup"><span data-stu-id="9cb01-112">Winlogon Notification Packages</span></span>

<span data-ttu-id="9cb01-113">Un pacchetto di notifica Winlogon è una DLL che esporta funzioni che gestiscono gli eventi Winlogon.</span><span class="sxs-lookup"><span data-stu-id="9cb01-113">A Winlogon notification package is a DLL that exports functions that handle Winlogon events.</span></span> <span data-ttu-id="9cb01-114">Ad esempio, quando un utente accede al sistema, Winlogon chiama ogni pacchetto di notifica per fornire informazioni sull'evento.</span><span class="sxs-lookup"><span data-stu-id="9cb01-114">For example, when a user logs onto the system, Winlogon calls each notification package to provide information about the event.</span></span> <span data-ttu-id="9cb01-115">Per altre informazioni, vedere [pacchetti di notifica di Winlogon](winlogon-notification-packages.md).</span><span class="sxs-lookup"><span data-stu-id="9cb01-115">For more information, see [Winlogon Notification Packages](winlogon-notification-packages.md).</span></span>

## <a name="gina-stubs"></a><span data-ttu-id="9cb01-116">Stub GINA</span><span class="sxs-lookup"><span data-stu-id="9cb01-116">GINA Stubs</span></span>

<span data-ttu-id="9cb01-117">Uno Stub [*Gina*](/windows/desktop/SecGloss/g-gly) è una DLL personalizzata Gina che usa le implementazioni delle funzioni di esportazione di una DLL GINA installata in precedenza (in genere MsGina.dll).</span><span class="sxs-lookup"><span data-stu-id="9cb01-117">A [*GINA*](/windows/desktop/SecGloss/g-gly) stub is a custom GINA DLL that uses the export function implementations of a previously installed GINA DLL (typically MsGina.dll).</span></span> <span data-ttu-id="9cb01-118">Uno stub GINA ottiene i puntatori a ogni funzione esportata dalla DLL GINA installata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9cb01-118">A GINA stub gets pointers to each function exported by the previously installed GINA DLL.</span></span> <span data-ttu-id="9cb01-119">Ogni funzione stub GINA usa quindi il puntatore a funzione appropriato per chiamare la funzione corrispondente nella DLL GINA installata in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9cb01-119">Each GINA stub function then uses the appropriate function pointer to call the corresponding function in the previously installed GINA DLL.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9cb01-120">Ogni funzione stub GINA deve chiamare la funzione corrispondente nell'oggetto GINA installato in precedenza.</span><span class="sxs-lookup"><span data-stu-id="9cb01-120">Each GINA stub function must call the corresponding function in the previously installed GINA.</span></span>

 

<span data-ttu-id="9cb01-121">Una funzione stub GINA può implementare funzionalità aggiuntive in una o più funzioni di esportazione.</span><span class="sxs-lookup"><span data-stu-id="9cb01-121">A GINA stub function can implement additional functionality in one or more of its export functions.</span></span> <span data-ttu-id="9cb01-122">Ad esempio, la funzione [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) di uno stub GINA potrebbe controllare l'ora corrente prima di chiamare la funzione **WlxLoggedOutSAS** della MsGina.dll.</span><span class="sxs-lookup"><span data-stu-id="9cb01-122">For example, the [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas) function of a GINA stub might check the current time before calling the **WlxLoggedOutSAS** function of the MsGina.dll.</span></span> <span data-ttu-id="9cb01-123">Se l'ora corrente si trovava in un intervallo specifico, la funzione stub potrebbe visualizzare un messaggio che indica che l'accesso non è consentito durante tale periodo di tempo e restituire l' **\_ \_ azione \_ Nessuna** firma di accesso condiviso di WLX a Winlogon.</span><span class="sxs-lookup"><span data-stu-id="9cb01-123">If the current time was within a specific range, the stub function could display a message that indicates logon is disallowed during that time period and return **WLX\_SAS\_ACTION\_NONE** to Winlogon.</span></span> <span data-ttu-id="9cb01-124">La funzione **WlxLoggedOutSAS** del MsGina.dll verrebbe quindi chiamata solo durante il periodo di tempo consentito.</span><span class="sxs-lookup"><span data-stu-id="9cb01-124">The **WlxLoggedOutSAS** function of the MsGina.dll would then be called only during the allowed time period.</span></span>

<span data-ttu-id="9cb01-125">L'applicazione GINA Stub ottiene una tabella dispatch per le funzioni di supporto di Winlogon tramite il parametro *pWinlogonFunctions* della funzione [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) .</span><span class="sxs-lookup"><span data-stu-id="9cb01-125">The GINA stub application gets a dispatch table to Winlogon support functions through the *pWinlogonFunctions* parameter of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function.</span></span> <span data-ttu-id="9cb01-126">L'applicazione GINA stub può usare questa tabella dispatch per chiamare le funzioni di supporto di Winlogon.</span><span class="sxs-lookup"><span data-stu-id="9cb01-126">The GINA stub application can use this dispatch table to call Winlogon support functions.</span></span> <span data-ttu-id="9cb01-127">Ad esempio, un'applicazione stub GINA può chiamare la funzione [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) per generare un evento di firma di [*attenzione sicura*](/windows/desktop/SecGloss/s-gly) quando una [*Smart Card*](/windows/desktop/SecGloss/s-gly) viene inserita in un [*lettore*](/windows/desktop/SecGloss/r-gly).</span><span class="sxs-lookup"><span data-stu-id="9cb01-127">For example, A GINA stub application can call the [**WlxSasNotify**](/windows/win32/api/winwlx/nc-winwlx-pwlx_sas_notify) function to cause a [*secure attention sequence*](/windows/desktop/SecGloss/s-gly) (SAS) event when a [*smart card*](/windows/desktop/SecGloss/s-gly) is inserted into a [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="9cb01-128">Per ulteriori informazioni sulla creazione di uno stub GINA, vedere l'esempio Gina Stub nella \\ directory Samples \\ Security \\ Gina \\ GinaStub di un'installazione di Platform Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="9cb01-128">For more information about creating a GINA stub, see the Gina Stubs sample in the \\Samples\\Security\\Gina\\GinaStub directory of a Platform Software Development Kit (SDK) installation.</span></span>

> [!Note]  
> <span data-ttu-id="9cb01-129">Tutte le chiamate tra un oggetto GINA e Winlogon devono trovarsi all'interno di un singolo thread.</span><span class="sxs-lookup"><span data-stu-id="9cb01-129">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

## <a name="gina-hooks"></a><span data-ttu-id="9cb01-130">Hook GINA</span><span class="sxs-lookup"><span data-stu-id="9cb01-130">GINA Hooks</span></span>

<span data-ttu-id="9cb01-131">Un hook GINA è uno stub GINA che, nell'implementazione della funzione [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) , sostituisce il puntatore alla funzione di supporto [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) nella tabella dispatch con un puntatore alla propria implementazione della funzione **WlxDialogBoxParam** .</span><span class="sxs-lookup"><span data-stu-id="9cb01-131">A GINA hook is a GINA stub that, in its implementation of the [**WlxInitialize**](/windows/desktop/api/Winwlx/nf-winwlx-wlxinitialize) function, replaces the pointer to the [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) support function in the dispatch table with a pointer to its own implementation of the **WlxDialogBoxParam** function.</span></span> <span data-ttu-id="9cb01-132">Di conseguenza, ogni volta che l'oggetto GINA precedentemente installato (in genere MsGina.dll) chiama la funzione **WlxDialogBoxParam** , viene chiamata la funzione implementata dall'hook Gina.</span><span class="sxs-lookup"><span data-stu-id="9cb01-132">As a result, each time the previously installed GINA (typically MsGina.dll) calls the **WlxDialogBoxParam** function, the function implemented by the GINA hook is called.</span></span>

<span data-ttu-id="9cb01-133">La funzione [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) implementata dall'hook Gina può sostituire la routine di callback [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) che risponde a un evento specifico della finestra di dialogo.</span><span class="sxs-lookup"><span data-stu-id="9cb01-133">The [**WlxDialogBoxParam**](/windows/win32/api/winwlx/nc-winwlx-pwlx_dialog_box_param) function implemented by the GINA hook can replace the [**DialogProc**](/windows/win32/api/winuser/nc-winuser-dlgproc) callback procedure that responds to a specific dialog box event.</span></span>

<span data-ttu-id="9cb01-134">Questo consente all'hook GINA di controllare completamente l'aspetto e il comportamento di tutte le finestre di dialogo create da MsGina.dll.</span><span class="sxs-lookup"><span data-stu-id="9cb01-134">This gives the GINA hook full control over the appearance and behavior of all of the dialog boxes that MsGina.dll creates.</span></span>

<span data-ttu-id="9cb01-135">Per ulteriori informazioni sulla creazione di un hook GINA, vedere l'esempio relativo a Gina hook \\ nella \\ directory Samples Security \\ Gina \\ GinaHook dell'installazione di Platform SDK.</span><span class="sxs-lookup"><span data-stu-id="9cb01-135">For more information about creating a GINA hook, see the Gina Hooks sample in the \\Samples\\Security\\Gina\\GinaHook directory of a Platform SDK installation.</span></span>

> [!Note]  
> <span data-ttu-id="9cb01-136">Tutte le chiamate tra un oggetto GINA e Winlogon devono trovarsi all'interno di un singolo thread.</span><span class="sxs-lookup"><span data-stu-id="9cb01-136">All calls between a GINA and Winlogon must be within a single thread.</span></span>

 

 

 
