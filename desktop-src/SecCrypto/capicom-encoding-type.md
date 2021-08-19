---
description: Indica il tipo di codifica utilizzato.
ms.assetid: 13e78a5e-3a31-44de-b249-28e360e1e087
title: CAPICOM_ENCODING_TYPE di controllo (Capicom.h)
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
ms.openlocfilehash: 1ec9a9ea1de4e3f501c94394ec9038d39c9b881c1e2bb1f41322d4f08c2db922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772486"
---
# <a name="capicom_encoding_type-enumeration"></a>Enumerazione CAPICOM \_ ENCODING \_ TYPE

Il **tipo di enumerazione CAPICOM ENCODING \_ \_ TYPE** indica il tipo di codifica utilizzato.

## <a name="members"></a>Membri



| Membro                      | Descrizione                                                                                                                                                                                 | Valore      |
|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------|
| **CAPICOM \_ ENCODE \_ ANY**    | I dati vengono salvati come stringa con codifica Base64 o come sequenza binaria pura. Questo tipo di codifica viene usato solo per i dati di input con un tipo di codifica sconosciuto. Introdotto in CAPICOM 2.0.<br/> | 0xffffffff |
| **CAPICOM \_ ENCODE \_ BASE64** | I dati vengono salvati come stringa con codifica Base64.<br/>                                                                                                                                        | 0          |
| **CAPICOM \_ ENCODE \_ BINARY** | I dati vengono salvati come sequenza binaria pura.<br/>                                                                                                                                         | 1          |



## <a name="remarks"></a>Commenti

Questo tipo di enumerazione viene utilizzato dai metodi e dalle proprietà CAPICOM seguenti:

-   [**Metodo Certificate.Export**](certificate-export.md)
-   [**EncodedData.Value -**](encodeddata-value.md) proprietà
-   [**Metodo EncryptedData.Encrypt**](encrypteddata-encrypt.md)
-   [**Metodo EnvelopedData.Encrypt**](envelopeddata-encrypt.md)
-   [**ExtendedProperty.Value -**](extendedproperty-value.md) proprietà
-   [**Metodo SignedData.Sign**](signeddata-sign.md)
-   [**Metodo SignedData.CoSign**](signeddata-cosign.md)
-   [**Metodo Store.Export**](store-export.md)
-   [**Metodo Utilities.GetRandom**](utilities-getrandom.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




