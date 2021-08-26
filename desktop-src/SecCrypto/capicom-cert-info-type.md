---
description: Definisce le informazioni su cui eseguire query da un certificato.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: CAPICOM_CERT_INFO_TYPE di controllo (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERT_INFO_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 480238556fce0470c51f00c394dd8566160686561342ec91da2e136c44a43cfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879421"
---
# <a name="capicom_cert_info_type-enumeration"></a>Enumerazione CAPICOM \_ CERT \_ INFO \_ TYPE

Il **tipo di enumerazione CAPICOM \_ CERT INFO \_ \_ TYPE** definisce le informazioni su cui eseguire query da un certificato.

## <a name="members"></a>Membri



| Membro                                         | Descrizione                                                                                  | Valore |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ SIMPLE \_ NAME** | Restituisce il nome visualizzato del soggetto del certificato.<br/>                              | 0     |
| **CAPICOM \_ CERT \_ INFO \_ ISSUER \_ SIMPLE \_ NAME**  | Restituisce il nome visualizzato dell'autorità emittente del certificato.<br/>                        | 1     |
| **CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ EMAIL \_ NAME**  | Restituisce l'indirizzo di posta elettronica del soggetto del certificato.<br/>                             | 2     |
| **CAPICOM \_ CERT \_ INFO \_ ISSUER \_ EMAIL \_ NAME**   | Restituisce l'indirizzo di posta elettronica dell'autorità emittente del certificato.<br/>                       | 3     |
| **CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ UPN**          | Restituisce l'UPN del soggetto del certificato. Introdotto in CAPICOM 2.0.<br/>            | 4     |
| **CAPICOM \_ CERT \_ INFO \_ ISSUER \_ UPN**           | Restituisce l'UPN dell'autorità emittente del certificato. Introdotto in CAPICOM 2.0.<br/>      | 5     |
| **CAPICOM \_ CERT \_ INFO \_ SUBJECT \_ DNS \_ NAME**    | Restituisce il nome DNS del soggetto del certificato. Introdotto in CAPICOM 2.0.<br/>       | 6     |
| **CAPICOM \_ CERT \_ INFO \_ ISSUER \_ DNS \_ NAME**     | Restituisce il nome DNS dell'autorità emittente del certificato. Introdotto in CAPICOM 2.0.<br/> | 7     |



## <a name="remarks"></a>Commenti

Il **tipo di enumerazione CAPICOM \_ CERT INFO \_ \_ TYPE** viene usato dal [**metodo Certificate.GetInfo.**](certificate-getinfo.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




