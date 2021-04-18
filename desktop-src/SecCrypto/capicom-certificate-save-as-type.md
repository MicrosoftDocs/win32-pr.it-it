---
description: Definisce il formato di un file contenente le informazioni sul certificato.
ms.assetid: 417a6d1b-6329-418c-823c-d82b94207fd6
title: Enumerazione CAPICOM_CERTIFICATE_SAVE_AS_TYPE (CAPICOM. h)
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
ms.openlocfilehash: 1e5365594a5a1cf1f06691c63b37c04f38530575
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328134"
---
# <a name="capicom_certificate_save_as_type-enumeration"></a>\_ \_ \_ Enumerazione di tipo Salva come certificato \_ CAPICOM

Il tipo di enumerazione **\_ \_ Save \_ As \_ del certificato capicot** definisce il formato di un file contenente le informazioni sul certificato. Questo tipo di enumerazione è stato introdotto da capicol 2,0.

## <a name="members"></a>Membri



| Membro                                  | Descrizione                                                                                                                                   | Valore |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **certificato capicol \_ \_ Salva \_ come \_ PFX** | Il file di output verrà formattato come file PFX (PKCS 12) e verranno salvate anche tutte le chiavi private associate esportabili.<br/> | 0     |
| **\_certificato CAPICOM \_ Salva \_ come \_ CER** | Il file di output verrà formattato come file con estensione CER senza chiavi private salvate.<br/>                                                        | 1     |



## <a name="remarks"></a>Commenti

Il tipo di enumerazione del **certificato CApicol \_ \_ Salva \_ come \_** tipo viene usato dal metodo [**Certificate. Save**](certificate-save.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




