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
# <a name="creating-a-new-computer-account"></a>Creazione di un nuovo account computer

Nell'esempio di codice riportato di seguito viene illustrato come creare un nuovo account computer utilizzando la funzione [**NetUserAdd**](/windows/desktop/api/Lmaccess/nf-lmaccess-netuseradd) .

Di seguito sono riportate alcune considerazioni sulla gestione degli account computer:

-   Il nome dell'account del computer deve essere tutti in maiuscolo per coerenza con le utilità di gestione degli account.
-   Il nome di un account computer ha sempre un segno di dollaro finale ($). Qualsiasi funzione utilizzata per gestire gli account computer deve compilare il nome del computer in modo che l'ultimo carattere del nome dell'account del computer sia un segno di dollaro ($). Per l'attendibilità tra domini, il nome dell'account è NomeDominioTrusting $.
-   La lunghezza massima del nome del computer è la lunghezza massima del \_ ComputerName \_ (15). Questa lunghezza non include il segno di dollaro finale ($).
-   La password di un nuovo account computer deve essere la rappresentazione in caratteri minuscoli del nome dell'account computer, senza il simbolo del dollaro finale ($). Per l'attendibilità tra domini, la password può essere un valore arbitrario che corrisponde al valore specificato sul lato trust della relazione.
-   La lunghezza massima della password è LM20 \_ PWLEN (14). Se il nome dell'account del computer supera questa lunghezza, la password deve essere troncata.
-   La password specificata al momento della creazione dell'account computer è valida solo fino a quando l'account computer non diventa attivo nel dominio. Viene stabilita una nuova password durante l'attivazione della relazione di trust.


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



L'utente che chiama le funzioni di gestione degli account deve disporre dei privilegi di amministratore nel computer di destinazione. Nel caso di account computer esistenti, l'autore dell'account può gestire l'account, indipendentemente dall'appartenenza amministrativa. Per ulteriori informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).

SeMachineAccountPrivilege può essere concesso nel computer di destinazione per consentire agli utenti specifici di creare account computer. In questo modo gli amministratori non sono in grado di creare account computer. Il chiamante deve abilitare questo privilegio prima di aggiungere l'account computer. Per ulteriori informazioni sui privilegi dell'account, vedere [privilegi](/windows/desktop/SecAuthZ/privileges) e [costanti di autorizzazione](/windows/desktop/SecAuthZ/authorization-constants).

 

 