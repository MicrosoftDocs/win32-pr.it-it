---
title: Display-Name attributo
description: Nome visualizzato per un oggetto .
ms.assetid: 0ecf5ede-0351-4d59-bdbf-44baf729f2e2
ms.tgt_platform: multiple
keywords:
- Display-Name schema AD dell'attributo
- Attributo displayName Schema di ACTIVE Directory
topic_type:
- apiref
api_name:
- Display-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4d4be2c6823fa068f07a14ab478a797c0db92e4f91b25656439319da5a25db1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120049591"
---
# <a name="display-name-attribute"></a>Display-Name attributo

Nome visualizzato per un oggetto . Si tratta in genere della combinazione di nome, secondo nome e cognome degli utenti.



| Voce | Valore |
|-------------------|------------------------------------------------------------------------------|
| CN                | Display-Name                                                                 |
| Ldap-Display-Name | displayName                                                                  |
| Dimensione              | \-                                                                           |
| Aggiorna privilegio  | Amministratore di dominio o proprietario dell'account.                                       |
| Frequenza di aggiornamento  | Quando viene creato il record dell'utente e quando è necessario modificare il nome visualizzato. |
| Attribute-Id      | 1.2.840.113556.1.2.13                                                        |
| System-Id-Guid    | bf967953-0de6-11d0-a285-00aa003049e2                                         |
| Sintassi            | [**String(Unicode)**](s-string-unicode.md)                                  |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Adam**](#adam)
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
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                             |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                             |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                             |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                     |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                              |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                       |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                       |
| Classi usate in        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Modello di indirizzo**](c-addresstemplate.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classi usate in        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Modello di indirizzo**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | \-                              |
| System-Only            | Falso                           |
| Is-Single-Valued       | Vero                            |
| Indicizzato             | Vero                            |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | 0                               |
| Range-Upper            | 256                             |
| Search-Flags           | 0x00000005                      |
| System-Flags           | 0x00000010                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classi usate in        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Modello di indirizzo**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classi usate in        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Modello di indirizzo**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| Is-Single-Valued       | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classi usate in        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Modello di indirizzo**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| MAPI-Id                | \-                                                                                                                                                                                                                                                                                                                                                                                                   |
| System-Only            | Falso                                                                                                                                                                                                                                                                                                                                                                                                |
| A valore singolo       | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Indicizzato             | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| Nel catalogo globale      | Vero                                                                                                                                                                                                                                                                                                                                                                                                 |
| NT-Security-Descriptor | O:BAG:BAD:S:                                                                                                                                                                                                                                                                                                                                                                                         |
| Range-Lower            | 0                                                                                                                                                                                                                                                                                                                                                                                                    |
| Range-Upper            | 256                                                                                                                                                                                                                                                                                                                                                                                                  |
| Search-Flags           | 0x00000005                                                                                                                                                                                                                                                                                                                                                                                           |
| System-Flags           | 0x00000010                                                                                                                                                                                                                                                                                                                                                                                           |
| Classi usate in        | [**Address-Book-Container**](c-addressbookcontainer.md)<br/> [**Modello di indirizzo**](c-addresstemplate.md)<br/> [**inetOrgPerson**](c-inetorgperson.md)<br/> [**PKI-Certificate-Template**](c-pkicertificatetemplate.md)<br/> [**Classe di servizio**](c-serviceclass.md)<br/> [**Istanza del servizio**](c-serviceinstance.md)<br/> [**In alto**](c-top.md)<br/> |



 

 





