---
description: Definisce quali informazioni devono essere sottoposte a query da un certificato.
ms.assetid: b603c06b-e6d4-4d5d-92b2-3b4f5b93478a
title: Enumerazione CAPICOM_CERT_INFO_TYPE (CAPICOM. h)
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
ms.openlocfilehash: 8e38bb8940645bbefecb3822bce8de8c2e0eb902
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327649"
---
# <a name="capicom_cert_info_type-enumeration"></a>\_Enumerazione del tipo di informazioni del certificato CApicol \_ \_

Il tipo di enumerazione **CApicol \_ CERT \_ info \_ Type** definisce quali informazioni devono essere sottoposte a query da un certificato.

## <a name="members"></a>Membri



| Membro                                         | Descrizione                                                                                  | Valore |
|------------------------------------------------|----------------------------------------------------------------------------------------------|-------|
| **\_ \_ \_ \_ nome semplice soggetto informazioni sul certificato capicot \_** | Restituisce il nome visualizzato dell'oggetto del certificato.<br/>                              | 0     |
| **\_ \_ \_ nome semplice dell'emittente informazioni \_ sul certificato capicot \_**  | Restituisce il nome visualizzato dell'emittente del certificato.<br/>                        | 1     |
| **\_ \_ \_ nome di \_ posta elettronica dell'oggetto \_ del certificato di capicol**  | Restituisce l'indirizzo di posta elettronica del soggetto del certificato.<br/>                             | 2     |
| **\_ \_ \_ nome di \_ posta elettronica dell'autorità emittente informazioni sul certificato CAPICOM \_**   | Restituisce l'indirizzo di posta elettronica dell'emittente del certificato.<br/>                       | 3     |
| **nome \_ \_ \_ UPN oggetto informazioni del certificato \_ CAPICOM**          | Restituisce l'UPN dell'oggetto del certificato. Introdotta in capicol 2,0.<br/>            | 4     |
| **nome UPN dell' \_ \_ \_ autorità emittente informazioni sul certificato capicot \_**           | Restituisce l'UPN dell'emittente del certificato. Introdotta in capicol 2,0.<br/>      | 5     |
| **\_ \_ \_ nome DNS dell'oggetto informazioni \_ sul certificato capicol \_**    | Restituisce il nome DNS del soggetto del certificato. Introdotta in capicol 2,0.<br/>       | 6     |
| **\_ \_ \_ nome DNS dell'autorità emittente informazioni sul \_ certificato \_ CAPICOM**     | Restituisce il nome DNS dell'emittente del certificato. Introdotta in capicol 2,0.<br/> | 7     |



## <a name="remarks"></a>Commenti

Il tipo di enumerazione **CApicol \_ CERT \_ info \_ Type** viene utilizzato dal metodo [**Certificate. GetInfo**](certificate-getinfo.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




