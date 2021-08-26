---
title: DNS-Tombstoned attributo
description: True se l'oggetto è stato contrassegnato per la rimozione definitiva. Questo attributo è disponibile per semplificare e velocizzare la ricerca dei record contrassegnati per la rimozione definitiva. Gli oggetti contrassegnati per la rimozione definitiva sono oggetti che sono stati eliminati ma non ancora rimossi dalla directory.
ms.assetid: d876a6d7-d5bc-4fe2-af03-1fff3381708f
ms.tgt_platform: multiple
keywords:
- DNS-Tombstoned schema AD dell'attributo
- Schema AD dell'attributo dNSTombstoned
topic_type:
- apiref
api_name:
- DNS-Tombstoned
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ef8f1b61d8d12fc1725fd695467058ac93277a7aab0977ccaed128a74da79d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077861"
---
# <a name="dns-tombstoned-attribute"></a>DNS-Tombstoned attributo

True se l'oggetto è stato contrassegnato per la rimozione definitiva. Questo attributo è disponibile per semplificare e velocizzare la ricerca dei record contrassegnati per la rimozione definitiva. Gli oggetti contrassegnati per la rimozione definitiva sono oggetti che sono stati eliminati ma non ancora rimossi dalla directory.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | DNS-Tombstoned                       |
| Ldap-Display-Name | dNSTombstoned                        |
| Dimensione              | 4 byte                              |
| Aggiorna privilegio  | Questo valore viene impostato dal sistema.     |
| Frequenza di aggiornamento  | Ogni volta che viene eliminato un oggetto.       |
| Attribute-Id      | 1.2.840.113556.1.4.1414              |
| System-Id-Guid    | d5eb2eb7-be4e-463b-a214-634a44d7392e |
| Sintassi            | [**Boolean**](s-boolean.md)         |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| Is-Single-Valued       | Vero                                     |
| Indicizzato             | Vero                                     |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| Is-Single-Valued       | Vero                                     |
| Indicizzato             | Vero                                     |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| Is-Single-Valued       | Vero                                     |
| Indicizzato             | Vero                                     |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| A valore singolo       | Vero                                     |
| Indicizzato             | Vero                                     |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| A valore singolo       | Vero                                     |
| Indicizzato             | Vero                                     |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------|
| ID collegamento                | \-                                       |
| MAPI-Id                | \-                                       |
| System-Only            | Falso                                    |
| A valore singolo       | Vero                                     |
| Indicizzato             | Vero                                     |
| Nel catalogo globale      | Falso                                    |
| NT-Security-Descriptor | O:BAG:BAD:S:                             |
| Range-Lower            | \-                                       |
| Range-Upper            | \-                                       |
| Search-Flags           | 0x00000001                               |
| System-Flags           | 0x00000010                               |
| Classi usate in        | [**Nodo DNS**](c-dnsnode.md)<br/> |



 

 





