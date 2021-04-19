---
description: Indica il tipo di codifica utilizzato.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: Enumerazione CAPICOM_ENCODING_TYPE (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ENCODING_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: a546831d6e88b3e35706df59adabe0627ad9fccb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332160"
---
# <a name="capicom_encoding_type-enumeration"></a>\_Enumerazione del tipo di codifica CAPICOM \_

Il tipo di enumerazione del **\_ \_ tipo di codifica capicol** indica il tipo di codifica utilizzato.

## <a name="members"></a>Membri



| Membro                      | Descrizione                                                                                                                                                                                 | Valore      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ Encode \_ any**    | I dati vengono salvati come stringa con codifica Base64 o come sequenza binaria pura. Questo tipo di codifica viene utilizzato solo per i dati di input con un tipo di codifica sconosciuto. Introdotta in capicol 2,0.<br/> | 0xFFFFFFFF |
| **\_Codifica Base64 per CAPICOM \_** | I dati vengono salvati come stringa con codifica Base64.<br/>                                                                                                                                        | 0          |
| **\_codificare il \_ file binario di CAPICOM** | I dati vengono salvati come una sequenza binaria pura.<br/>                                                                                                                                         | 1          |



## <a name="remarks"></a>Commenti

Questo tipo di enumerazione viene usato dai metodi e dalle proprietà di CAPICOM seguenti:

-   Metodo [**Certificate. Export**](certificate-export.md)
-   Proprietà [**EncodedData. Value**](encodeddata-value.md)
-   Metodo [**EncryptedData. Encrypt**](encrypteddata-encrypt.md)
-   Metodo [**EnvelopedData. Encrypt**](envelopeddata-encrypt.md)
-   Proprietà [**ExtendedProperty. Value**](extendedproperty-value.md)
-   Metodo [**SignedData. Sign**](signeddata-sign.md)
-   Metodo [**SignedData. cosign**](signeddata-cosign.md)
-   [**Store. Export**](store-export.md) (metodo)
-   [**Utilities. GetRandom,**](utilities-getrandom.md) metodo

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




