---
description: Definisce il formato di un file contenente informazioni sul certificato.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: CAPICOM_CERTIFICATE_SAVE_AS_TYPE enumerazione (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATE_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 2000bd582475a227fdb638649ee1a634e488a21a7c09d84dd6e21dafc5e9aa42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772642"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>Enumerazione CAPICOM \_ CERTIFICATE \_ SAVE AS \_ \_ TYPE

Il **tipo di enumerazione CAPICOM CERTIFICATE SAVE AS \_ \_ \_ \_ TYPE** definisce il formato di un file contenente informazioni sul certificato. Questo tipo di enumerazione è stato introdotto da CAPICOM 2.0.

## <a name="members"></a>Membri



| Membro                                  | Descrizione                                                                                                                                   | Valore |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **SALVATAGGIO \_ DEL CERTIFICATO CAPICOM \_ \_ COME \_ PFX** | Il file di output verrà formattato come file PFX (PKCS 12) e verranno salvate anche le chiavi private associate esportabili.<br/> | 0     |
| **SALVATAGGIO \_ DEL CERTIFICATO CAPICOM \_ \_ COME \_ CER** | Il file di output verrà formattato come file CER senza chiavi private salvate.<br/>                                                        | 1     |



## <a name="remarks"></a>Commenti

Il **tipo di enumerazione CAPICOM CERTIFICATE SAVE AS \_ \_ \_ \_ TYPE** viene usato dal [**metodo Certificate.Save.**](certificate-save.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




