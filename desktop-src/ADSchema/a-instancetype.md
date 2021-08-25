---
title: Instance-Type attributo
description: Campo di bit che determina come viene creata un'istanza dell'oggetto in un server specifico.
ms.assetid: ed77c302-3d80-4292-8e48-bfc6cb5079ee
ms.tgt_platform: multiple
keywords:
- Instance-Type schema AD dell'attributo
- Schema AD dell'attributo instanceType
topic_type:
- apiref
api_name:
- Instance-Type
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb087afedfb6570c2d25858ca99a53749607f2260f3a6f7a24ae766e22ea3e61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119925281"
---
# <a name="instance-type-attribute"></a>Instance-Type attributo

Campo di bit che determina come viene creata un'istanza dell'oggetto in un server specifico. Il valore di questo attributo può differire in repliche diverse anche se le repliche sono sincronizzate.

Questo attributo può essere zero o una combinazione di uno o più dei valori seguenti.

| Valore      | Descrizione                                                                                        |
|------------|----------------------------------------------------------------------------------------------------|
| 0x00000001 | Responsabile del contesto dei nomi.                                                                        |
| 0x00000002 | Non viene creata un'istanza di questa replica.                                                                  |
| 0x00000004 | L'oggetto è scrivibile in questa directory.                                                          |
| 0x00000008 | Il contesto dei nomi sopra questo in questa directory viene mantenuto.                                       |
| 0x00000010 | Il contesto dei nomi è in fase di costruzione per la prima volta tramite la replica. |
| 0x00000020 | Il contesto dei nomi è in corso di rimozione dal DSA locale.                          |



 



| Voce | Valore |
|-------------------|------------------------------------------------|
| CN                | Instance-Type                                  |
| Ldap-Display-Name | instanceType                                   |
| Dimensione              | 4 byte.                                       |
| Privilegio di aggiornamento  | Questo valore viene impostato dall'amministratore dello schema. |
| Frequenza di aggiornamento  | Quando viene creato l'oggetto .                    |
| Attribute-Id      | 1.2.840.113556.1.2.1                           |
| System-Id-Guid    | bf96798c-0de6-11d0-a285-00aa003049e2           |
| Sintassi            | [**Enumerazione**](s-enumeration.md)           |



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
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| Is-Single-Valued       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| Is-Single-Valued       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="adam"></a>Adam



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| A valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| A valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| A valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| A valore singolo       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|---------------------------------|
| ID collegamento                | \-                              |
| MAPI-Id                | 0x80BD                          |
| System-Only            | Vero                            |
| Is-Single-Valued       | Vero                            |
| Indicizzato             | Falso                           |
| Nel catalogo globale      | Vero                            |
| NT-Security-Descriptor | O:BAG:BAD:S:                    |
| Range-Lower            | \-                              |
| Range-Upper            | \-                              |
| Search-Flags           | 0x00000008                      |
| System-Flags           | 0x00000012                      |
| Classi usate in        | [**In alto**](c-top.md)<br/> |



 

 





