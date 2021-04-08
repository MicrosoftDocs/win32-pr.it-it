---
title: Attributo Display-Name
description: Nome visualizzato di un oggetto.
ms.assetid: 0ecf5ede-0351-4d59-bdbf-44baf729f2e2
ms.tgt_platform: multiple
keywords:
- Schema AD Display-Name attribute
- Schema AD dell'attributo displayName
topic_type:
- apiref
api_name:
- Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b4fe662ccbdf2157c7ed51a311739cf7d16273b
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744258"
---
# <a name="display-name-attribute"></a>Attributo Display-Name

Nome visualizzato di un oggetto. Si tratta in genere della combinazione del nome, dell'iniziale e del cognome degli utenti.



| Voce | Valore |
|-------------------|------------------------------------------------------------------------------|
| CN                | Display-Name                                                                 |
| LDAP-Display-Name | displayName                                                                  |
| Dimensione              | \-                                                                           |
| Privilegio aggiornamento  | Amministratore di dominio o proprietario dell'account.                                       |
| Frequenza di aggiornamento  | Quando il record dell'utente viene creato e quando il nome visualizzato deve essere modificato. |
| Attribute-Id      | 1.2.840.113556.1.2.13                                                        |
| System-ID-GUID    | bf967953-0de6-11d0-a285-00aa003049e2                                         |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                  |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                               |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                               |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                            |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                             |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                             |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                       |
| Classi utilizzate in        | [**Address-Book-container**](c-addressbookcontainer.md)<br/> [**Address-template**](c-addresstemplate.md)<br/> [**PKI-certificate-template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classi utilizzate in        | [**Address-Book-container**](c-addressbookcontainer.md)<br/> [**Address-template**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-certificate-template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>ADAM



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| È a valore singolo       | Vero                            |
| Indicizzato             | Vero                            |
| Nel catalogo globale      | Vero                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 256                             |
| Search-Flags           | 0x00000005                      |
| System-Flags           | 0x00000010                      |
| Classi utilizzate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classi utilizzate in        | [**Address-Book-container**](c-addressbookcontainer.md)<br/> [**Address-template**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-certificate-template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classi utilizzate in        | [**Address-Book-container**](c-addressbookcontainer.md)<br/> [**Address-template**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-certificate-template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classi utilizzate in        | [**Address-Book-container**](c-addressbookcontainer.md)<br/> [**Address-template**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-certificate-template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| È a valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classi utilizzate in        | [**Address-Book-container**](c-addressbookcontainer.md)<br/> [**Address-template**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-certificate-template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



 

 





