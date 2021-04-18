---
title: Attributo Lockout-Duration
description: La quantità di tempo per cui un account è bloccato a causa del superamento del Lockout-Threshold.
ms.assetid: 6a26ef80-86ed-433f-9032-cdd1aaf00388
ms.tgt_platform: multiple
keywords:
- Schema AD Lockout-Duration attribute
- Schema AD dell'attributo lockoutDuration
topic_type:
- apiref
api_name:
- Lockout-Duration
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 526fedef47bea20148a591259dbc7ec1702b5a15
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "106303009"
---
# <a name="lockout-duration-attribute"></a>Attributo Lockout-Duration

La quantità di tempo per cui un account è bloccato a causa del superamento della [**soglia di blocco**](a-lockoutthreshold.md) . Questo valore viene archiviato come intero grande che rappresenta il negativo del numero di intervalli di 100 nanosecondi dal momento in cui viene superata la [**soglia di blocco**](a-lockoutthreshold.md) che deve trascorrere prima che l'account venga sbloccato.



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Lockout-Duration                     |
| LDAP-Display-Name | lockoutDuration                      |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | Amministratore di dominio                 |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.60                |
| System-ID-GUID    | bf9679a5-0de6-11d0-a285-00aa003049e2 |
| Sintassi            | [**Interval**](s-interval.md)       |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| È a valore singolo       | Vero                                                                                                                                                  |
| Indicizzato             | Falso                                                                                                                                                 |
| Nel catalogo globale      | Falso                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| È a valore singolo       | Vero                                                                                                                                                  |
| Indicizzato             | Falso                                                                                                                                                 |
| Nel catalogo globale      | Falso                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| È a valore singolo       | Vero                                                                                                                                                  |
| Indicizzato             | Falso                                                                                                                                                 |
| Nel catalogo globale      | Falso                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| È a valore singolo       | Vero                                                                                                                                                  |
| Indicizzato             | Falso                                                                                                                                                 |
| Nel catalogo globale      | Falso                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| È a valore singolo       | Vero                                                                                                                                                  |
| Indicizzato             | Falso                                                                                                                                                 |
| Nel catalogo globale      | Falso                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| ID collegamento                | \-                                                                                                                                                    |
| MAPI-Id                | \-                                                                                                                                                    |
| System-Only            | Falso                                                                                                                                                 |
| È a valore singolo       | Vero                                                                                                                                                  |
| Indicizzato             | Falso                                                                                                                                                 |
| Nel catalogo globale      | Falso                                                                                                                                                 |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                                                                                                          |
| Range-Lower            | \-                                                                                                                                                    |
| Range-Upper            | \-                                                                                                                                                    |
| Search-Flags           | 0x00000000                                                                                                                                            |
| System-Flags           | 0x00000010                                                                                                                                            |
| Classi utilizzate in        | [**Criteri di dominio**](c-domainpolicy.md)<br/> [**Sam-dominio**](c-samdomain.md)<br/> [**Sam-dominio-base**](c-samdomainbase.md)<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Soglia di blocco**](a-lockoutthreshold.md)
</dt> </dl>

 

 





