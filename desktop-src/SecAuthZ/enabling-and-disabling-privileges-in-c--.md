---
description: L'abilitazione di un privilegio in un token di accesso consente al processo di eseguire azioni a livello di sistema che non è stato possibile eseguire in precedenza.
ms.assetid: aa2d3fe7-01ee-4243-b72c-3e8b90068e22
title: Abilitazione e disabilitazione dei privilegi in C++
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 354f3ac2b27a7c027bd7c48e753263c43b676dd3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104058031"
---
# <a name="enabling-and-disabling-privileges-in-c"></a><span data-ttu-id="2d94a-103">Abilitazione e disabilitazione dei privilegi in C++</span><span class="sxs-lookup"><span data-stu-id="2d94a-103">Enabling and Disabling Privileges in C++</span></span>

<span data-ttu-id="2d94a-104">L'abilitazione di un privilegio in un token di accesso consente al processo di eseguire azioni a livello di sistema che non è stato possibile eseguire in precedenza.</span><span class="sxs-lookup"><span data-stu-id="2d94a-104">Enabling a privilege in an access token allows the process to perform system-level actions that it could not previously.</span></span> <span data-ttu-id="2d94a-105">L'applicazione deve verificare accuratamente che i privilegi siano appropriati per il tipo di account, specialmente per i seguenti privilegi avanzati.</span><span class="sxs-lookup"><span data-stu-id="2d94a-105">Your application should thoroughly verify that the privilege is appropriate to the type of account, especially for the following powerful privileges.</span></span>



| <span data-ttu-id="2d94a-106">Costante Privilege</span><span class="sxs-lookup"><span data-stu-id="2d94a-106">Privilege constant</span></span>           | <span data-ttu-id="2d94a-107">Valore stringa</span><span class="sxs-lookup"><span data-stu-id="2d94a-107">String value</span></span>                  | <span data-ttu-id="2d94a-108">Nome visualizzato</span><span class="sxs-lookup"><span data-stu-id="2d94a-108">Display name</span></span>                        |
|------------------------------|-------------------------------|-------------------------------------|
| <span data-ttu-id="2d94a-109">\_nome ASSIGNPRIMARYTOKEN \_ se</span><span class="sxs-lookup"><span data-stu-id="2d94a-109">SE\_ASSIGNPRIMARYTOKEN\_NAME</span></span> | <span data-ttu-id="2d94a-110">SeAssignPrimaryTokenPrivilege</span><span class="sxs-lookup"><span data-stu-id="2d94a-110">SeAssignPrimaryTokenPrivilege</span></span> | <span data-ttu-id="2d94a-111">Sostituzione di token a livello di processo</span><span class="sxs-lookup"><span data-stu-id="2d94a-111">Replace a process-level token</span></span>       |
| <span data-ttu-id="2d94a-112">\_nome backup \_ se</span><span class="sxs-lookup"><span data-stu-id="2d94a-112">SE\_BACKUP\_NAME</span></span>             | <span data-ttu-id="2d94a-113">SeBackupPrivilege</span><span class="sxs-lookup"><span data-stu-id="2d94a-113">SeBackupPrivilege</span></span>             | <span data-ttu-id="2d94a-114">Ripristino di file e directory</span><span class="sxs-lookup"><span data-stu-id="2d94a-114">Back up files and directories</span></span>       |
| <span data-ttu-id="2d94a-115">\_nome debug \_ se</span><span class="sxs-lookup"><span data-stu-id="2d94a-115">SE\_DEBUG\_NAME</span></span>              | <span data-ttu-id="2d94a-116">SeDebugPrivilege</span><span class="sxs-lookup"><span data-stu-id="2d94a-116">SeDebugPrivilege</span></span>              | <span data-ttu-id="2d94a-117">Debug di programmi</span><span class="sxs-lookup"><span data-stu-id="2d94a-117">Debug programs</span></span>                      |
| <span data-ttu-id="2d94a-118">SE \_ aumenta \_ il \_ nome della quota</span><span class="sxs-lookup"><span data-stu-id="2d94a-118">SE\_INCREASE\_QUOTA\_NAME</span></span>    | <span data-ttu-id="2d94a-119">SeIncreaseQuotaPrivilege</span><span class="sxs-lookup"><span data-stu-id="2d94a-119">SeIncreaseQuotaPrivilege</span></span>      | <span data-ttu-id="2d94a-120">Regolazione limite risorse memoria per un processo</span><span class="sxs-lookup"><span data-stu-id="2d94a-120">Adjust memory quotas for a process</span></span>  |
| <span data-ttu-id="2d94a-121">\_nome TCB \_ se</span><span class="sxs-lookup"><span data-stu-id="2d94a-121">SE\_TCB\_NAME</span></span>                | <span data-ttu-id="2d94a-122">SeTcbPrivilege</span><span class="sxs-lookup"><span data-stu-id="2d94a-122">SeTcbPrivilege</span></span>                | <span data-ttu-id="2d94a-123">Agisci come parte del sistema operativo</span><span class="sxs-lookup"><span data-stu-id="2d94a-123">Act as part of the operating system</span></span> |



 

<span data-ttu-id="2d94a-124">Prima di abilitare uno di questi privilegi potenzialmente pericolosi, determinare che le funzioni o le operazioni nel codice richiedono effettivamente i privilegi.</span><span class="sxs-lookup"><span data-stu-id="2d94a-124">Before enabling any of these potentially dangerous privileges, determine that functions or operations in your code actually require the privileges.</span></span> <span data-ttu-id="2d94a-125">Alcune funzioni del sistema operativo, ad esempio, richiedono effettivamente **SeTcbPrivilege**.</span><span class="sxs-lookup"><span data-stu-id="2d94a-125">For example, very few functions in the operating system actually require the **SeTcbPrivilege**.</span></span> <span data-ttu-id="2d94a-126">Per un elenco di tutti i privilegi disponibili, vedere [costanti Privilege](authorization-constants.md).</span><span class="sxs-lookup"><span data-stu-id="2d94a-126">For a list of all the available privileges, see [Privilege Constants](authorization-constants.md).</span></span>

<span data-ttu-id="2d94a-127">Nell'esempio seguente viene illustrato come abilitare o disabilitare un privilegio in un [*token di accesso*](/windows/desktop/SecGloss/a-gly).</span><span class="sxs-lookup"><span data-stu-id="2d94a-127">The following example shows how to enable or disable a privilege in an [*access token*](/windows/desktop/SecGloss/a-gly).</span></span> <span data-ttu-id="2d94a-128">Nell'esempio viene chiamata la funzione [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) per ottenere l' [*identificatore univoco locale*](/windows/desktop/SecGloss/l-gly) (LUID) utilizzato dal sistema locale per identificare il privilegio.</span><span class="sxs-lookup"><span data-stu-id="2d94a-128">The example calls the [**LookupPrivilegeValue**](/windows/desktop/api/Winbase/nf-winbase-lookupprivilegevaluea) function to get the [*locally unique identifier*](/windows/desktop/SecGloss/l-gly) (LUID) that the local system uses to identify the privilege.</span></span> <span data-ttu-id="2d94a-129">Viene quindi chiamata la funzione [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) , che Abilita o Disabilita il privilegio che dipende dal valore del parametro *bEnablePrivilege* .</span><span class="sxs-lookup"><span data-stu-id="2d94a-129">Then the example calls the [**AdjustTokenPrivileges**](/windows/win32/api/securitybaseapi/nf-securitybaseapi-adjusttokenprivileges) function, which either enables or disables the privilege that depends on the value of the *bEnablePrivilege* parameter.</span></span>


```C++
#include <windows.h>
#include <stdio.h>
#pragma comment(lib, "cmcfg32.lib")

BOOL SetPrivilege(
    HANDLE hToken,          // access token handle
    LPCTSTR lpszPrivilege,  // name of privilege to enable/disable
    BOOL bEnablePrivilege   // to enable or disable privilege
    ) 
{
    TOKEN_PRIVILEGES tp;
    LUID luid;

    if ( !LookupPrivilegeValue( 
            NULL,            // lookup privilege on local system
            lpszPrivilege,   // privilege to lookup 
            &luid ) )        // receives LUID of privilege
    {
        printf("LookupPrivilegeValue error: %u\n", GetLastError() ); 
        return FALSE; 
    }

    tp.PrivilegeCount = 1;
    tp.Privileges[0].Luid = luid;
    if (bEnablePrivilege)
        tp.Privileges[0].Attributes = SE_PRIVILEGE_ENABLED;
    else
        tp.Privileges[0].Attributes = 0;

    // Enable the privilege or disable all privileges.

    if ( !AdjustTokenPrivileges(
           hToken, 
           FALSE, 
           &tp, 
           sizeof(TOKEN_PRIVILEGES), 
           (PTOKEN_PRIVILEGES) NULL, 
           (PDWORD) NULL) )
    { 
          printf("AdjustTokenPrivileges error: %u\n", GetLastError() ); 
          return FALSE; 
    } 

    if (GetLastError() == ERROR_NOT_ALL_ASSIGNED)

    {
          printf("The token does not have the specified privilege. \n");
          return FALSE;
    } 

    return TRUE;
}

```



 

