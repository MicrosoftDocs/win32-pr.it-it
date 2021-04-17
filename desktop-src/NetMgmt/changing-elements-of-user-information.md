---
title: Modifica degli elementi delle informazioni utente
description: Le funzioni di gestione della rete forniscono diversi livelli di informazioni per facilitare la modifica delle informazioni utente.
ms.assetid: dc126431-57b0-467b-9f56-1e66a647c7b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e1aa6ec8d7fed30d38d25adc67974d8bad8ab1f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106299872"
---
# <a name="changing-elements-of-user-information"></a><span data-ttu-id="89ad4-103">Modifica degli elementi delle informazioni utente</span><span class="sxs-lookup"><span data-stu-id="89ad4-103">Changing Elements of User Information</span></span>

<span data-ttu-id="89ad4-104">Le funzioni di gestione della rete forniscono diversi livelli di informazioni per facilitare la modifica delle informazioni utente.</span><span class="sxs-lookup"><span data-stu-id="89ad4-104">The network management functions provide a variety of information levels to assist in changing user information.</span></span> <span data-ttu-id="89ad4-105">Per eseguire correttamente alcuni livelli, è necessario disporre di privilegi amministrativi.</span><span class="sxs-lookup"><span data-stu-id="89ad4-105">Some levels require administrative privileges to execute successfully.</span></span> <span data-ttu-id="89ad4-106">Per ulteriori informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="89ad4-106">For more information about calling functions that require administrator privileges, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span>

<span data-ttu-id="89ad4-107">Il codice di esempio in questo argomento illustra come modificare diversi elementi delle informazioni utente chiamando la funzione [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="89ad4-107">The sample code in this topic demonstrates how to change several elements of user information by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="89ad4-108">Il codice usa varie strutture di informazioni di gestione della rete.</span><span class="sxs-lookup"><span data-stu-id="89ad4-108">The code uses various network management information structures.</span></span>

<span data-ttu-id="89ad4-109">Quando si modificano le informazioni utente, è preferibile utilizzare il livello specifico per tali informazioni.</span><span class="sxs-lookup"><span data-stu-id="89ad4-109">When changing user information, it is best to use the specific level for that piece of information.</span></span> <span data-ttu-id="89ad4-110">In questo modo si evita la reimpostazione accidentale di informazioni non correlate quando si utilizzano i valori di livello inferiore.</span><span class="sxs-lookup"><span data-stu-id="89ad4-110">This prevents the accidental resetting of unrelated information when using the lower level values.</span></span>

<span data-ttu-id="89ad4-111">Gli esempi di codice seguenti illustrano come impostare alcuni dei livelli di utilizzo più comuni:</span><span class="sxs-lookup"><span data-stu-id="89ad4-111">Setting some of the more commonly used levels is illustrated in the following code samples:</span></span>

-   [<span data-ttu-id="89ad4-112">Impostazione della password utente, livello 1003</span><span class="sxs-lookup"><span data-stu-id="89ad4-112">Setting the User Password, Level 1003</span></span>](#setting-the-user-password-level-1003)
-   [<span data-ttu-id="89ad4-113">Impostazione del privilegio utente, livello 1005</span><span class="sxs-lookup"><span data-stu-id="89ad4-113">Setting the User Privilege, Level 1005</span></span>](#setting-the-user-privilege-level-1005)
-   [<span data-ttu-id="89ad4-114">Impostazione della Home directory dell'utente, livello 1006</span><span class="sxs-lookup"><span data-stu-id="89ad4-114">Setting the User Home Directory, Level 1006</span></span>](#setting-the-user-home-directory-level-1006)
-   [<span data-ttu-id="89ad4-115">Impostazione del campo dei commenti utente, livello 1007</span><span class="sxs-lookup"><span data-stu-id="89ad4-115">Setting the User Comment Field, Level 1007</span></span>](#setting-the-user-comment-field-level-1007)
-   [<span data-ttu-id="89ad4-116">Impostazione dei flag utente, livello 1008</span><span class="sxs-lookup"><span data-stu-id="89ad4-116">Setting the User Flags, Level 1008</span></span>](#setting-the-user-flags-level-1008)
-   [<span data-ttu-id="89ad4-117">Impostazione del percorso dello script utente, livello 1009</span><span class="sxs-lookup"><span data-stu-id="89ad4-117">Setting the User Script Path, Level 1009</span></span>](#setting-the-user-script-path-level-1009)
-   [<span data-ttu-id="89ad4-118">Impostazione dei flag dell'autorità utente, livello 1010</span><span class="sxs-lookup"><span data-stu-id="89ad4-118">Setting The User Authority Flags, Level 1010</span></span>](#setting-the-user-authority-flags-level-1010)
-   [<span data-ttu-id="89ad4-119">Impostazione del nome completo dell'utente, livello 1011</span><span class="sxs-lookup"><span data-stu-id="89ad4-119">Setting The User Full Name, Level 1011</span></span>](#setting-the-user-full-name-level-1011)

<span data-ttu-id="89ad4-120">Tutti i frammenti di codice presuppongono che l'utente abbia definito la direttiva di compilazione UNICODE e includa i file di intestazione SDK appropriati, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="89ad4-120">All code fragments assume that the user has defined the UNICODE compile directive and included the appropriate SDK header files, as follows:</span></span>


```C++
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#define INCL_NET
#include <lm.h>
#include <stdio.h>

#pragma comment(lib, "netapi32.lib")

#define SERVER L"test_server_name"
#define USERNAME L"test_user_name"

DWORD netRet = 0;
```



## <a name="setting-the-user-password-level-1003"></a><span data-ttu-id="89ad4-121">Impostazione della password utente, livello 1003</span><span class="sxs-lookup"><span data-stu-id="89ad4-121">Setting the User Password, Level 1003</span></span>

<span data-ttu-id="89ad4-122">Nel frammento di codice seguente viene illustrato come impostare la password di un utente su un valore noto con una chiamata alla funzione [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="89ad4-122">The following code fragment illustrates how to set a user's password to a known value with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="89ad4-123">L' [**argomento \_ informazioni utente \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) contiene informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="89ad4-123">The [**USER\_INFO\_1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) topic contains additional information.</span></span>


```C++
#define PASSWORD L"new_password"

USER_INFO_1003 usriSetPassword;
//
// Set the usri1003_password member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriSetPassword.usri1003_password = PASSWORD;
    
netRet = NetUserSetInfo( SERVER, USERNAME, 1003, (LPBYTE)&usriSetPassword, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1003!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1003\n", netRet);
```



## <a name="setting-the-user-privilege-level-1005"></a><span data-ttu-id="89ad4-124">Impostazione del privilegio utente, livello 1005</span><span class="sxs-lookup"><span data-stu-id="89ad4-124">Setting the User Privilege, Level 1005</span></span>

<span data-ttu-id="89ad4-125">Nel frammento di codice seguente viene illustrato come specificare il livello di privilegio assegnato a un utente con una chiamata alla funzione [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="89ad4-125">The following code fragment illustrates how to specify the level of privilege assigned to a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="89ad4-126">L' [**argomento \_ informazioni utente \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) contiene informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="89ad4-126">The [**USER\_INFO\_1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) topic contains additional information.</span></span> <span data-ttu-id="89ad4-127">Per ulteriori informazioni sui privilegi dell'account, vedere [privilegi](/windows/desktop/SecAuthZ/privileges) e [costanti di autorizzazione](/windows/desktop/SecAuthZ/authorization-constants).</span><span class="sxs-lookup"><span data-stu-id="89ad4-127">For more information about account privileges, see [Privileges](/windows/desktop/SecAuthZ/privileges) and [Authorization Constants](/windows/desktop/SecAuthZ/authorization-constants).</span></span>


```C++
USER_INFO_1005 usriPriv;
//
// Set the usri1005_priv member to the appropriate value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriPriv.usri1005_priv = USER_PRIV_USER;

netRet = NetUserSetInfo( SERVER, USERNAME, 1005, (LPBYTE)&usriPriv, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1005!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1005\n", netRet);
```



## <a name="setting-the-user-home-directory-level-1006"></a><span data-ttu-id="89ad4-128">Impostazione della Home directory dell'utente, livello 1006</span><span class="sxs-lookup"><span data-stu-id="89ad4-128">Setting the User Home Directory, Level 1006</span></span>

<span data-ttu-id="89ad4-129">Il frammento di codice seguente illustra come specificare il percorso della Home directory di un utente con una chiamata alla funzione [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="89ad4-129">The following code fragment illustrates how to specify the path of a user's home directory with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="89ad4-130">La directory può essere un percorso hardcoded o un percorso Unicode valido.</span><span class="sxs-lookup"><span data-stu-id="89ad4-130">The directory can be a hard-coded path or a valid Unicode path.</span></span> <span data-ttu-id="89ad4-131">L' [**argomento \_ informazioni utente \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) contiene informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="89ad4-131">The [**USER\_INFO\_1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) topic contains additional information.</span></span>


```C++
#define HOMEDIR L"C:\\USER\USER_PATH"
USER_INFO_1006 usriHomeDir;
//
// Set the usri1006_home_dir member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriHomeDir.usri1006_home_dir = HOMEDIR;

netRet = NetUserSetInfo( SERVER, USERNAME, 1006, (LPBYTE)&usriHomeDir, NULL );

if( netRet == NERR_Success ) 
    printf("Success with level 1006!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1006\n", netRet);
```



## <a name="setting-the-user-comment-field-level-1007"></a><span data-ttu-id="89ad4-132">Impostazione del campo dei commenti utente, livello 1007</span><span class="sxs-lookup"><span data-stu-id="89ad4-132">Setting the User Comment Field, Level 1007</span></span>

<span data-ttu-id="89ad4-133">Nel frammento di codice seguente viene illustrato come associare un commento a un utente chiamando la funzione [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="89ad4-133">The following code fragment illustrates how to associate a comment with a user by calling the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="89ad4-134">L' [**argomento \_ informazioni utente \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) contiene informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="89ad4-134">The [**USER\_INFO\_1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) topic contains additional information.</span></span>


```C++
#define COMMENT L"This is my Comment Text for the user"
USER_INFO_1007 usriComment;
//
// Set the usri1007_comment member to point to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriComment.usri1007_comment = COMMENT;

netRet = NetUserSetInfo( SERVER, USERNAME, 1007, (LPBYTE)&usriComment, NULL );

if( netRet == NERR_Success )
    printf("Success with level 1007!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1007\n", netRet);
```



## <a name="setting-the-user-flags-level-1008"></a><span data-ttu-id="89ad4-135">Impostazione dei flag utente, livello 1008</span><span class="sxs-lookup"><span data-stu-id="89ad4-135">Setting the User Flags, Level 1008</span></span>

<span data-ttu-id="89ad4-136">Nel frammento di codice seguente viene illustrato come impostare i flag utente con una chiamata alla funzione [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="89ad4-136">The following code fragment illustrates how to set user flags with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="89ad4-137">L'argomento [**User \_ info \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) contiene un elenco di valori validi per i flag e una descrizione di ogni flag.</span><span class="sxs-lookup"><span data-stu-id="89ad4-137">The [**USER\_INFO\_1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) topic contains a list of valid values for the flags and a description of each flag.</span></span>

<span data-ttu-id="89ad4-138">Si noti che è \_ necessario impostare il flag di script UF per le reti Windows NT, windows 2000, Windows XP e LAN Manager.</span><span class="sxs-lookup"><span data-stu-id="89ad4-138">Note that the UF\_SCRIPT flag must be set for Windows NT, Windows 2000, Windows XP, and LAN Manager networks.</span></span> <span data-ttu-id="89ad4-139">Se si tenta di impostare altri flag senza impostare \_ lo script UF in queste reti, la funzione [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) avrà esito negativo.</span><span class="sxs-lookup"><span data-stu-id="89ad4-139">Trying to set other flags without setting UF\_SCRIPT on these networks will cause the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function to fail.</span></span>


```C++
#define USR_FLAGS UF_SCRIPT | UF_NORMAL_ACCOUNT
USER_INFO_1008 usriFlags;
//
// Set the usri1008_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFlags.usri1008_flags = USR_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1008, (LPBYTE)&usriFlags, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1008!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1008\n", netRet);
```



## <a name="setting-the-user-script-path-level-1009"></a><span data-ttu-id="89ad4-140">Impostazione del percorso dello script utente, livello 1009</span><span class="sxs-lookup"><span data-stu-id="89ad4-140">Setting the User Script Path, Level 1009</span></span>

<span data-ttu-id="89ad4-141">Nel frammento di codice seguente viene illustrato come impostare il percorso per il file di script di accesso di un determinato utente con una chiamata alla funzione [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="89ad4-141">The following code fragment illustrates how to set the path for the logon script file of a particular user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="89ad4-142">Il file di script può essere. File CMD, un. File EXE o. File BAT.</span><span class="sxs-lookup"><span data-stu-id="89ad4-142">The script file can be a .CMD file, an .EXE file, or a .BAT file.</span></span> <span data-ttu-id="89ad4-143">Anche la stringa può essere null.</span><span class="sxs-lookup"><span data-stu-id="89ad4-143">The string can also be null.</span></span> <span data-ttu-id="89ad4-144">L' [**argomento \_ informazioni utente \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) contiene informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="89ad4-144">The [**USER\_INFO\_1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) topic contains additional information.</span></span>


```C++
#define SCRIPT_PATH L"C:\\BIN\\MYSCRIPT.BAT"
USER_INFO_1009 usriScrPath;
//
// Set the usri1009_script_path member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriScrPath.usri1009_script_path = SCRIPT_PATH;
netRet = NetUserSetInfo( SERVER, USERNAME, 1009, (LPBYTE)&usriScrPath, NULL );
if( netRet == NERR_Success ) 
    printf("Success with level 1009!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo level 1009\n", netRet);
```



## <a name="setting-the-user-authority-flags-level-1010"></a><span data-ttu-id="89ad4-145">Impostazione dei flag dell'autorità utente, livello 1010</span><span class="sxs-lookup"><span data-stu-id="89ad4-145">Setting The User Authority Flags, Level 1010</span></span>

<span data-ttu-id="89ad4-146">Nel frammento di codice seguente viene illustrato come impostare i flag dei privilegi dell'operatore per un utente con una chiamata alla funzione [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="89ad4-146">The following code fragment illustrates how to set the operator privilege flags for a user with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="89ad4-147">L'argomento [**User \_ info \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) contiene un elenco di valori validi per i flag e una descrizione di ogni flag.</span><span class="sxs-lookup"><span data-stu-id="89ad4-147">The [**USER\_INFO\_1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) topic contains a list of valid values for the flags and a description of each flag.</span></span>


```C++
#define AUTHORITY_FLAGS AF_OP_ACCOUNTS
USER_INFO_1010 usriAuthFlags;
//
// Set the usri1010_auth_flags member to the appropriate constant value.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriAuthFlags.usri1010_auth_flags = AUTHORITY_FLAGS;
netRet = NetUserSetInfo( SERVER, USERNAME, 1010, (LPBYTE)&usriAuthFlags, NULL);
if( netRet == NERR_Success )
    printf("Success with level 1010!\n");
else
    printf( "ERROR: %d returned from NetUserSetInfo level 1010\n", netRet);
```



## <a name="setting-the-user-full-name-level-1011"></a><span data-ttu-id="89ad4-148">Impostazione del nome completo dell'utente, livello 1011</span><span class="sxs-lookup"><span data-stu-id="89ad4-148">Setting The User Full Name, Level 1011</span></span>

<span data-ttu-id="89ad4-149">Il frammento di codice seguente illustra come impostare il nome completo di un utente con una chiamata alla funzione [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) .</span><span class="sxs-lookup"><span data-stu-id="89ad4-149">The following code fragment illustrates how to set a user's full name with a call to the [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) function.</span></span> <span data-ttu-id="89ad4-150">L' [**argomento \_ informazioni utente \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) contiene informazioni aggiuntive.</span><span class="sxs-lookup"><span data-stu-id="89ad4-150">The [**USER\_INFO\_1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) topic contains additional information.</span></span>


```C++
#define USER_FULL_NAME L"Joe B. User"
USER_INFO_1011 usriFullName;
//
// Set the usri1011_full_name member to a valid Unicode string.
//
// SERVER and USERNAME can be hard-coded strings or pointers to Unicode strings.
//
usriFullName.usri1011_full_name = USER_FULL_NAME;
netRet = NetUserSetInfo( SERVER, USERNAME, 1011, (LPBYTE)&usriFullName, NULL);
if( netRet == NERR_Success ) 
    printf("Success with level 1011!\n");
else 
    printf( "ERROR: %d returned from NetUserSetInfo\n", netRet);
```



 

 