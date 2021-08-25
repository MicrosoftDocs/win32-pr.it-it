---
description: Definisce il formato di un file contenente informazioni sui certificati.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: CAPICOM_CERTIFICATES_SAVE_AS_TYPE enumerazione (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_CERTIFICATES_SAVE_AS_TYPE
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 70185a7a48b7dc195727991fb0dcc35f4909451fa0e4da5f4100e8385adebc2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879371"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a>Enumerazione DEI \_ CERTIFICATI \_ CAPICOM SAVE \_ AS \_ TYPE

Il **tipo di enumerazione \_ CAPICOM CERTIFICATES \_ SAVE AS \_ \_ TYPE** definisce il formato di un file contenente informazioni sui certificati. Questo tipo di enumerazione è stato introdotto da CAPICOM 2.0.

## <a name="members"></a>Membri



| Membro                                          | Descrizione                                          | Valore |
|-------------------------------------------------|------------------------------------------------------|-------|
| **CERTIFICATI CAPICOM \_ \_ \_ SALVANO \_ COME SERIALIZZATI** | I certificati salvati vengono serializzati.<br/>    | 0     |
| **I CERTIFICATI CAPICOM \_ \_ VENGONO \_ SALVATI COME \_ PKCS7**      | I certificati vengono salvati come PKCS \# 7.<br/> | 1     |
| **CERTIFICATI CAPICOM \_ \_ SALVA COME \_ \_ PFX**        | I certificati vengono salvati come PFX.<br/>      | 2     |



## <a name="remarks"></a>Commenti

Il tipo di enumerazione \_ CAPICOM CERTIFICATES \_ SAVE AS TYPE viene usato dal metodo \_ \_ [**Certificates.Save.**](certificates-save.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 




