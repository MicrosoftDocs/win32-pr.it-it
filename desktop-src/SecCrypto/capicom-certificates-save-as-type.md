---
description: Definisce il formato di un file contenente le informazioni sui certificati.
ms.assetid: 2118746a-9fa4-4e6a-82ce-e57f154f4a94
title: Enumerazione CAPICOM_CERTIFICATES_SAVE_AS_TYPE (CAPICOM. h)
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
ms.openlocfilehash: 3cbde0e8a64fa931ce50d2277d33b5fd5c27ee68
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328133"
---
# <a name="capicom_certificates_save_as_type-enumeration"></a>\_Enumerazione dei certificati CAPICOM \_ Salva \_ come \_ tipo

Il tipo di enumerazione dei **certificati di capico \_ \_ \_ , \_** che definisce il formato di un file contenente le informazioni sui certificati. Questo tipo di enumerazione è stato introdotto da capicol 2,0.

## <a name="members"></a>Membri



| Membro                                          | Descrizione                                          | Valore |
|-------------------------------------------------|------------------------------------------------------|-------|
| **i certificati CAPICOM \_ vengono \_ salvati \_ come \_ serializzati** | I certificati salvati vengono serializzati.<br/>    | 0     |
| **I certificati CAPICOM \_ vengono \_ salvati \_ come \_ PKCS7**      | I certificati vengono salvati come PKCS \# 7.<br/> | 1     |
| **\_certificati CAPICOM \_ Salva \_ come \_ PFX**        | I certificati vengono salvati come PFX.<br/>      | 2     |



## <a name="remarks"></a>Commenti

Il \_ tipo di enumerazione dei certificati capico \_ \_ \_ è usato dal metodo [**Certificates. Save**](certificates-save.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




