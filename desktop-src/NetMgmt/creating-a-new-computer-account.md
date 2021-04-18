---
title: Creazione di un nuovo account computer
description: Nell'esempio di codice riportato di seguito viene illustrato come creare un nuovo account computer utilizzando la funzione NetUserAdd.
ms.assetid: 1e180b8e-b948-4836-b789-cb9dff0829e8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cfd02a9d2053310c50e40957e6afee6e3a4a5ab1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299924"
---
# <a name="creating-a-new-computer-account"></a><span data-ttu-id="43ae5-103">Creazione di un nuovo account computer</span><span class="sxs-lookup"><span data-stu-id="43ae5-103">Creating a New Computer Account</span></span>

<span data-ttu-id="43ae5-104">Nell'esempio di codice riportato di seguito viene illustrato come creare un nuovo account computer utilizzando la funzione [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) .</span><span class="sxs-lookup"><span data-stu-id="43ae5-104">The following code sample demonstrates how to create a new computer account using the [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) function.</span></span>

<span data-ttu-id="43ae5-105">Di seguito sono riportate alcune considerazioni sulla gestione degli account computer:</span><span class="sxs-lookup"><span data-stu-id="43ae5-105">The following are considerations for managing computer accounts:</span></span>

-   <span data-ttu-id="43ae5-106">Il nome dell'account del computer deve essere tutti in maiuscolo per coerenza con le utilità di gestione degli account.</span><span class="sxs-lookup"><span data-stu-id="43ae5-106">The computer account name should be all uppercase for consistency with account management utilities.</span></span>
-   <span data-ttu-id="43ae5-107">Il nome di un account computer ha sempre un segno di dollaro finale ($).</span><span class="sxs-lookup"><span data-stu-id="43ae5-107">A computer account name always has a trailing dollar sign ($).</span></span> <span data-ttu-id="43ae5-108">Qualsiasi funzione utilizzata per gestire gli account computer deve compilare il nome del computer in modo che l'ultimo carattere del nome dell'account del computer sia un segno di dollaro ($).</span><span class="sxs-lookup"><span data-stu-id="43ae5-108">Any functions used to manage computer accounts must build the computer name such that the last character of the computer account name is a dollar sign ($).</span></span> <span data-ttu-id="43ae5-109">Per l'attendibilità tra domini, il nome dell'account è NomeDominioTrusting $.</span><span class="sxs-lookup"><span data-stu-id="43ae5-109">For interdomain trust, the account name is TrustingDomainName$.</span></span>
-   <span data-ttu-id="43ae5-110">La lunghezza massima del nome del computer è la lunghezza massima del \_ ComputerName \_ (15).</span><span class="sxs-lookup"><span data-stu-id="43ae5-110">The maximum computer name length is MAX\_COMPUTERNAME\_LENGTH (15).</span></span> <span data-ttu-id="43ae5-111">Questa lunghezza non include il segno di dollaro finale ($).</span><span class="sxs-lookup"><span data-stu-id="43ae5-111">This length does not include the trailing dollar sign ($).</span></span>
-   <span data-ttu-id="43ae5-112">La password di un nuovo account computer deve essere la rappresentazione in caratteri minuscoli del nome dell'account computer, senza il simbolo del dollaro finale ($).</span><span class="sxs-lookup"><span data-stu-id="43ae5-112">The password for a new computer account should be the lowercase representation of the computer account name, without the trailing dollar sign ($).</span></span> <span data-ttu-id="43ae5-113">Per l'attendibilità tra domini, la password può essere un valore arbitrario che corrisponde al valore specificato sul lato trust della relazione.</span><span class="sxs-lookup"><span data-stu-id="43ae5-113">For interdomain trust, the password can be an arbitrary value that matches the value specified on the trust side of the relationship.</span></span>
-   <span data-ttu-id="43ae5-114">La lunghezza massima della password è LM20 \_ PWLEN (14).</span><span class="sxs-lookup"><span data-stu-id="43ae5-114">The maximum password length is LM20\_PWLEN (14).</span></span> <span data-ttu-id="43ae5-115">Se il nome dell'account del computer supera questa lunghezza, la password deve essere troncata.</span><span class="sxs-lookup"><span data-stu-id="43ae5-115">The password should be truncated to this length if the computer account name exceeds this length.</span></span>
-   <span data-ttu-id="43ae5-116">La password specificata al momento della creazione dell'account computer è valida solo fino a quando l'account computer non diventa attivo nel dominio.</span><span class="sxs-lookup"><span data-stu-id="43ae5-116">The password provided at computer-account-creation time is valid only until the computer account becomes active on the domain.</span></span> <span data-ttu-id="43ae5-117">Viene stabilita una nuova password durante l'attivazione della relazione di trust.</span><span class="sxs-lookup"><span data-stu-id="43ae5-117">A new password is established during trust relationship activation.</span></span>


```C++
#include <windows.h>
#include <lm.h>
#pragma comment(lib, "netapi32.lib")

BOOL AddMachineAccount(
    LPWSTR wTargetComputer,
    LPWSTR MachineAccount,
    DWORD AccountType
    )
{
    LPWSTR wAccount;
    LPWSTR wPassword;
    USER_INFO_1 ui;
    DWORD cbAccount;
    DWORD cbLength;
    DWORD dwError;

    //
    // Ensure a valid computer account type was passed.
    //
    if (AccountType != UF_WORKSTATION_TRUST_ACCOUNT &&
        AccountType != UF_SERVER_TRUST_ACCOUNT &&
        AccountType != UF_INTERDOMAIN_TRUST_ACCOUNT
        ) 
    {
        SetLastError(ERROR_INVALID_PARAMETER);
        return FALSE;
    }

    //
    // Obtain number of chars in computer account name.
    //
    cbLength = cbAccount = lstrlenW(MachineAccount);

    //
    // Ensure computer name doesn't exceed maximum length.
    //
    if(cbLength > MAX_COMPUTERNAME_LENGTH) {
        SetLastError(ERROR_INVALID_ACCOUNT_NAME);
        return FALSE;
    }

    //
    // Allocate storage to contain Unicode representation of
    // computer account name + trailing $ + NULL.
    //
    wAccount=(LPWSTR)HeapAlloc(GetProcessHeap(), 0,
        (cbAccount + 1 + 1) * sizeof(WCHAR)  // Account + '$' + NULL
        );

    if(wAccount == NULL) return FALSE;

    //
    // Password is the computer account name converted to lowercase;
    //  you will convert the passed MachineAccount in place.
    //
    wPassword = MachineAccount;

    //
    // Copy MachineAccount to the wAccount buffer allocated while
    //  converting computer account name to uppercase.
    //  Convert password (in place) to lowercase.
    //
    while(cbAccount--) {
        wAccount[cbAccount] = towupper( MachineAccount[cbAccount] );
        wPassword[cbAccount] = towlower( wPassword[cbAccount] );
    }

    //
    // Computer account names have a trailing Unicode '$'.
    //
    wAccount[cbLength] = L'$';
    wAccount[cbLength + 1] = L'\0'; // terminate the string

    //
    // If the password is greater than the max allowed, truncate.
    //
    if(cbLength > LM20_PWLEN) wPassword[LM20_PWLEN] = L'\0';

    //
    // Initialize the USER_INFO_1 structure.
    //
    ZeroMemory(&ui, sizeof(ui));

    ui.usri1_name = wAccount;
    ui.usri1_password = wPassword;

    ui.usri1_flags = AccountType | UF_SCRIPT;
    ui.usri1_priv = USER_PRIV_USER;

    dwError=NetUserAdd(
                wTargetComputer,    // target computer name
                1,                  // info level
                (LPBYTE) &ui,       // buffer
                NULL
                );

    //
    // Free allocated memory.
    //
    if(wAccount) HeapFree(GetProcessHeap(), 0, wAccount);

    //
    // Indicate whether the function was successful.
    //
    if(dwError == NO_ERROR)
        return TRUE;
    else {
        SetLastError(dwError);
        return FALSE;
    }
}
```



<span data-ttu-id="43ae5-118">L'utente che chiama le funzioni di gestione degli account deve disporre dei privilegi di amministratore nel computer di destinazione.</span><span class="sxs-lookup"><span data-stu-id="43ae5-118">The user that calls the account management functions must have Administrator privilege on the target computer.</span></span> <span data-ttu-id="43ae5-119">Nel caso di account computer esistenti, l'autore dell'account può gestire l'account, indipendentemente dall'appartenenza amministrativa.</span><span class="sxs-lookup"><span data-stu-id="43ae5-119">In the case of existing computer accounts, the creator of the account can manage the account, regardless of administrative membership.</span></span> <span data-ttu-id="43ae5-120">Per ulteriori informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="43ae5-120">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="43ae5-121">SeMachineAccountPrivilege può essere concesso nel computer di destinazione per consentire agli utenti specifici di creare account computer.</span><span class="sxs-lookup"><span data-stu-id="43ae5-121">The SeMachineAccountPrivilege can be granted on the target computer to give specified users the ability to create computer accounts.</span></span> <span data-ttu-id="43ae5-122">In questo modo gli amministratori non sono in grado di creare account computer.</span><span class="sxs-lookup"><span data-stu-id="43ae5-122">This gives non-administrators the ability to create computer accounts.</span></span> <span data-ttu-id="43ae5-123">Il chiamante deve abilitare questo privilegio prima di aggiungere l'account computer.</span><span class="sxs-lookup"><span data-stu-id="43ae5-123">The caller needs to enable this privilege prior to adding the computer account.</span></span> <span data-ttu-id="43ae5-124">Per ulteriori informazioni sui privilegi dell'account, vedere [privilegi](/windows/desktop/SecAuthZ/privileges) e [costanti di autorizzazione](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="43ae5-124">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>

 

 