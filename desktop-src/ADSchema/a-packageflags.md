---
title: Attributo Package-Flags
description: Oggetto bit che contiene i flag di stato della distribuzione per un'applicazione.
ms.assetid: 5b6cfed5-db04-438e-912b-60dce7a16409
ms.tgt_platform: multiple
keywords:
- Schema AD Package-Flags attribute
- Schema AD dell'attributo packageFlags
topic_type:
- apiref
api_name:
- Package-Flags
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7202124bdeac22347d727638dc564a145599e9c7
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/14/2020
ms.locfileid: "103744970"
---
# <a name="package-flags-attribute"></a>Attributo Package-Flags

Oggetto bit che contiene i flag di stato della distribuzione per un'applicazione.

Questo attributo può essere zero o una combinazione di uno o più dei valori seguenti.

| Valore                 | Descrizione                                                                                                                                                                                                                                                                                                    |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x00000004<br/> | La versione non gestita di questa applicazione deve essere disinstallata prima dell'assegnazione. **Windows XP con SP1 e versioni successive:** Questo flag non è supportato.<br/> <br/>                                                                                                                                          |
| 0x00000008<br/> | Si tratta di un'applicazione pubblicata.<br/>                                                                                                                                                                                                                                                                    |
| 0x00000010<br/> | Questo pacchetto è stato distribuito dopo la versione beta 3 di Windows 2000.<br/>                                                                                                                                                                                                                                             |
| 0x00000020<br/> | Questa applicazione può essere installata con la funzionalità **Installazione applicazioni** del pannello di controllo.<br/>                                                                                                                                                                                                 |
| 0x00000040<br/> | Questa applicazione può essere installata automaticamente su richiesta.<br/>                                                                                                                                                                                                                                                   |
| 0x00000080<br/> | Questa applicazione è orfana. Un'applicazione pubblicata può diventare orfana se l'amministratore rimuove l'applicazione dall'elenco di applicazioni distribuibili.<br/>                                                                                                                                    |
| 0x00000100<br/> | Questa applicazione deve essere trattata come disinstallata.<br/>                                                                                                                                                                                                                                                  |
| 0x00000200<br/> | Questa applicazione è disponibile solo come pilota.<br/>                                                                                                                                                                                                                                                      |
| 0x00000400<br/> | Si tratta di un'applicazione assegnata. Un'applicazione assegnata non può essere completamente rimossa dall'utente. Se l'utente tenta di disinstallare l'applicazione con la funzionalità **installazione** applicazioni del pannello di controllo, l'applicazione verrà nuovamente annunciata nel computer al termine della rimozione.<br/> |
| 0x00000800<br/> | Questa applicazione è orfana quando i criteri vengono rimossi. Se l'amministratore rimuove i criteri correlati a questa applicazione, l'amministratore non controllerà più la distribuzione dell'applicazione, ma l'applicazione installata continuerà a funzionare.<br/>                          |
| 0x00001000<br/> | Questa applicazione viene disinstallata quando i criteri di distribuzione vengono rimossi.<br/>                                                                                                                                                                                                                              |
| 0x00002000<br/> | Verrà eseguita un'installazione completa delle applicazioni assegnate dall'utente.<br/>                                                                                                                                                                                                                                |
| 0x00004000<br/> | Le versioni precedenti dell'applicazione devono essere aggiornate a questa versione.<br/>                                                                                                                                                                                                                                |
| 0x00008000<br/> | Questo pacchetto supporta solo un'interfaccia utente minima con un indicatore di stato per il processo di installazione.<br/>                                                                                                                                                                                               |
| 0x00010000<br/> | Si tratta di un pacchetto per le versioni di Windows a 32 bit che non deve essere eseguito in Windows XP Professional x64 Edition o nelle versioni a 64 bit di Windows Server 2003.<br/>                                                                                                                                      |
| 0x00020000<br/> | Questo pacchetto è adatto per qualsiasi lingua.<br/>                                                                                                                                                                                                                                                          |
| 0x00040000<br/> | Questo pacchetto include aggiornamenti.<br/>                                                                                                                                                                                                                                                                          |
| 0x00080000<br/> | Il pacchetto dispone di un'interfaccia utente completa per il processo di installazione.<br/>                                                                                                                                                                                                                                |
| 0x00100000<br/> | Le classi per questa applicazione vengono mantenute durante un'operazione di ridistribuzione se l'applicazione viene ridistribuita in una ridenominazione del dominio.<br/>                                                                                                                                                                       |



 



| Voce | Valore |
|-------------------|--------------------------------------|
| CN                | Package-Flags                        |
| LDAP-Display-Name | packageFlags                         |
| Dimensione              | \-                                   |
| Privilegio aggiornamento  | \-                                   |
| Frequenza di aggiornamento  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.327               |
| System-ID-GUID    | 7d6c0e99-7e20-11d0-afd6-00c04fd930c9 |
| Sintassi            | [**Enumerazione**](s-enumeration.md) |



## <a name="implementations"></a>Implementazioni

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| È a valore singolo       | Vero                                                             |
| Indicizzato             | Vero                                                             |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi utilizzate in        | [**Registrazione pacchetto**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| È a valore singolo       | Vero                                                             |
| Indicizzato             | Vero                                                             |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi utilizzate in        | [**Registrazione pacchetto**](c-packageregistration.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| È a valore singolo       | Vero                                                             |
| Indicizzato             | Vero                                                             |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi utilizzate in        | [**Registrazione pacchetto**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| È a valore singolo       | Vero                                                             |
| Indicizzato             | Vero                                                             |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi utilizzate in        | [**Registrazione pacchetto**](c-packageregistration.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| È a valore singolo       | Vero                                                             |
| Indicizzato             | Vero                                                             |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi utilizzate in        | [**Registrazione pacchetto**](c-packageregistration.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Voce | Valore |
|------------------------|------------------------------------------------------------------|
| ID collegamento                | \-                                                               |
| MAPI-Id                | \-                                                               |
| System-Only            | Falso                                                            |
| È a valore singolo       | Vero                                                             |
| Indicizzato             | Vero                                                             |
| Nel catalogo globale      | Falso                                                            |
| NT-Security-descrittore | O:BAG: NON VALIDO: S:                                                     |
| Range-Lower            | \-                                                               |
| Range-Upper            | \-                                                               |
| Search-Flags           | 0x00000001                                                       |
| System-Flags           | 0x00000010                                                       |
| Classi utilizzate in        | [**Registrazione pacchetto**](c-packageregistration.md)<br/> |



 

 





