---
title: Attributo Home-Directory
description: La Home Directory per l'account.
ms.assetid: 7fd431f2-f2e0-476f-82ed-04f776c234eb
ms.tgt_platform: multiple
keywords:
- Schema AD Home-Directory attribute
- Schema AD dell'attributo homeDirectory
topic_type:
- apiref
api_name:
- Home-Directory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 070285336284e6d07b6333d28eff5c85c4dc6c5a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744850"
---
# <a name="home-directory-attribute"></a>Attributo Home-Directory

La Home Directory per l'account. Se [**homeDrive**](a-homedrive.md) è impostato e specifica una lettera di unità, **HomeDirectory** deve essere un percorso UNC. In caso contrario, **HomeDirectory** è un percorso locale completo, inclusa la lettera di unità (ad esempio, *LetteraUnità ***\\ :*** _\\_ * _cartella_ directory). Questo valore può essere una stringa null.



| Voce | Valore |
|-------------------|------------------------------------------------------------------------------------|
| CN                | Home-Directory                                                                     |
| LDAP-Display-Name | homeDirectory                                                                      |
| Dimensione              | \-                                                                                 |
| Privilegio aggiornamento  | Amministratore di dominio                                                               |
| Frequenza di aggiornamento  | Quando viene creato il record dell'utente e ogni volta che la home directory deve cambiare. |
| Attribute-Id      | 1.2.840.113556.1.4.44                                                              |
| System-ID-GUID    | bf967985-0de6-11d0-a285-00aa003049e2                                               |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                        |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-----------------------------------|
| ID collegamento                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Falso                             |
| È a valore singolo       | Vero                              |
| Indicizzato             | Falso                             |
| Nel catalogo globale      | Falso                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000010                        |
| System-Flags           | 0x00000010                        |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| È a valore singolo       | Vero                                                                                |
| Indicizzato             | Falso                                                                               |
| Nel catalogo globale      | Falso                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| È a valore singolo       | Vero                                                                                |
| Indicizzato             | Falso                                                                               |
| Nel catalogo globale      | Falso                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| È a valore singolo       | Vero                                                                                |
| Indicizzato             | Falso                                                                               |
| Nel catalogo globale      | Falso                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                  |
| MAPI-Id                | \-                                                                                  |
| System-Only            | Falso                                                                               |
| È a valore singolo       | Vero                                                                                |
| Indicizzato             | Falso                                                                               |
| Nel catalogo globale      | Falso                                                                               |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                        |
| Range-Lower            | \-                                                                                  |
| Range-Upper            | \-                                                                                  |
| Search-Flags           | 0x00000010                                                                          |
| System-Flags           | 0x00000010                                                                          |
| Classi utilizzate in        | [**Utente**](c-user.md)<br/> [**posixAccount**](c-posixaccount.md)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**homeDrive**](a-homedrive.md)
</dt> </dl>

 

 





