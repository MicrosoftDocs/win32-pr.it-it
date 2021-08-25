---
title: Modifica degli elementi delle informazioni utente
description: Le funzioni di gestione della rete forniscono un'ampia gamma di livelli di informazioni che consentono di modificare le informazioni degli utenti.
ms.assetid: dc126431-57b0-467b-9f56-1e66a647c7b1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd3161bb4d689b70f85f6c20c7c302779d0f685e8bcace43cffdee68b2cda2d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912501"
---
# <a name="changing-elements-of-user-information"></a>Modifica degli elementi delle informazioni utente

Le funzioni di gestione della rete forniscono un'ampia gamma di livelli di informazioni che consentono di modificare le informazioni degli utenti. Alcuni livelli richiedono privilegi amministrativi per l'esecuzione corretta. Per altre informazioni sulla chiamata di funzioni che richiedono privilegi di amministratore, vedere [Esecuzione con privilegi speciali](/windows/desktop/SecBP/running-with-special-privileges).

Il codice di esempio in questo argomento illustra come modificare diversi elementi di informazioni utente chiamando la [**funzione NetUserSetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) Il codice usa varie strutture di informazioni sulla gestione della rete.

Quando si modificano le informazioni utente, è meglio usare il livello specifico per tale informazione. Ciò impedisce la reimpostazione accidentale di informazioni non correlate quando si usano i valori di livello inferiore.

L'impostazione di alcuni dei livelli più usati è illustrata negli esempi di codice seguenti:

-   [Impostazione della password utente, livello 1003](#setting-the-user-password-level-1003)
-   [Impostazione del privilegio utente, livello 1005](#setting-the-user-privilege-level-1005)
-   [Impostazione della home directory utente, livello 1006](#setting-the-user-home-directory-level-1006)
-   [Impostazione del campo Commento utente, livello 1007](#setting-the-user-comment-field-level-1007)
-   [Impostazione dei flag utente, livello 1008](#setting-the-user-flags-level-1008)
-   [Impostazione del percorso dello script utente, livello 1009](#setting-the-user-script-path-level-1009)
-   [Impostazione dei flag dell'autorità utente, livello 1010](#setting-the-user-authority-flags-level-1010)
-   [Impostazione del nome completo dell'utente, livello 1011](#setting-the-user-full-name-level-1011)

Tutti i frammenti di codice presuppongono che l'utente abbia definito la direttiva di compilazione UNICODE e abbia incluso i file di intestazione SDK appropriati, come indicato di seguito:


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



## <a name="setting-the-user-password-level-1003"></a>Impostazione della password utente, livello 1003

Il frammento di codice seguente illustra come impostare la password di un utente su un valore noto con una chiamata alla [**funzione NetUserSetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) [**\_ L'argomento USER INFO \_ 1003**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1003) contiene informazioni aggiuntive.


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



## <a name="setting-the-user-privilege-level-1005"></a>Impostazione del privilegio utente, livello 1005

Il frammento di codice seguente illustra come specificare il livello di privilegio assegnato a un utente con una chiamata alla [**funzione NetUserSetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) [**\_ L'argomento USER INFO \_ 1005**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1005) contiene informazioni aggiuntive. Per altre informazioni sui privilegi dell'account, vedere [Privilegi](/windows/desktop/SecAuthZ/privileges) e [costanti di autorizzazione](/windows/desktop/SecAuthZ/authorization-constants).


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



## <a name="setting-the-user-home-directory-level-1006"></a>Impostazione della home directory utente, livello 1006

Il frammento di codice seguente illustra come specificare il percorso della home directory di un utente con una chiamata alla [**funzione NetUserSetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) La directory può essere un percorso hard-coded o un percorso Unicode valido. [**\_ L'argomento USER INFO \_ 1006**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1006) contiene informazioni aggiuntive.


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



## <a name="setting-the-user-comment-field-level-1007"></a>Impostazione del campo Commento utente, livello 1007

Il frammento di codice seguente illustra come associare un commento a un utente chiamando la [**funzione NetUserSetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) [**\_ L'argomento USER INFO \_ 1007**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1007) contiene informazioni aggiuntive.


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



## <a name="setting-the-user-flags-level-1008"></a>Impostazione dei flag utente, livello 1008

Il frammento di codice seguente illustra come impostare i flag utente con una chiamata alla [**funzione NetUserSetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) [**\_ L'argomento USER INFO \_ 1008**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1008) contiene un elenco di valori validi per i flag e una descrizione di ogni flag.

Si noti che il flag UF SCRIPT deve essere impostato per le reti \_ Windows NT, Windows 2000, Windows XP e LAN Manager. Se si tenta di impostare altri flag senza impostare UF SCRIPT su queste reti, la funzione \_ [**NetUserSetInfo**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) avrà esito negativo.


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



## <a name="setting-the-user-script-path-level-1009"></a>Impostazione del percorso dello script utente, livello 1009

Il frammento di codice seguente illustra come impostare il percorso del file script di accesso di un determinato utente con una chiamata alla [**funzione NetUserSetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) Il file di script può essere un oggetto . CMD, un .EXE o un file .BAT file. La stringa può anche essere Null. [**\_ L'argomento USER INFO \_ 1009**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1009) contiene informazioni aggiuntive.


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



## <a name="setting-the-user-authority-flags-level-1010"></a>Impostazione dei flag dell'autorità utente, livello 1010

Il frammento di codice seguente illustra come impostare i flag di privilegi dell'operatore per un utente con una chiamata alla [**funzione NetUserSetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) [**\_ L'argomento USER INFO \_ 1010**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1010) contiene un elenco di valori validi per i flag e una descrizione di ogni flag.


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



## <a name="setting-the-user-full-name-level-1011"></a>Impostazione del nome completo dell'utente, livello 1011

Il frammento di codice seguente illustra come impostare il nome completo di un utente con una chiamata alla [**funzione NetUserSetInfo.**](/windows/desktop/api/Lmaccess/nf-lmaccess-netusersetinfo) [**\_ L'argomento USER INFO \_ 1011**](/windows/desktop/api/Lmaccess/ns-lmaccess-user_info_1011) contiene informazioni aggiuntive.


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



 

 