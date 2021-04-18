---
description: Definisce i nomi di utilizzo chiavi estesi in base alla posizione in cui possono essere utilizzati.
ms.assetid: 78f9f9cb-46e7-4f81-a16e-503750a0d743
title: Enumerazione CAPICOM_EKU (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_EKU
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: e1d2f4f435fa31df00b87e20254aad57b690b047
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106328131"
---
# <a name="capicom_eku-enumeration"></a>\_Enumerazione EKU di CAPICOM

Il tipo di enumerazione **\_ EKU CAPICOM** definisce i nomi di utilizzo chiavi estesi in base alla posizione in cui possono essere utilizzati.

## <a name="members"></a>Membri



| Membro                                     | Descrizione                                                                                                                                                 | Valore |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **\_altro EKU di CAPICOM \_**                    | Il certificato ha usi definiti nei criteri locali. Viene usato se l'EKU necessario non è predefinito e il valore OID deve essere impostato dall'applicazione.<br/> | 0     |
| **\_ \_ autenticazione server EKU CAPICOM \_**             | Il certificato può essere usato per autenticare un server.<br/>                                                                                                | 1     |
| **\_ \_ autenticazione client EKU CAPICOM \_**             | Il certificato può essere usato per autenticare un client.<br/>                                                                                                | 2     |
| **\_firma del codice EKU \_ di \_ CAPICOM**            | Il certificato può essere usato per creare una firma digitale.<br/>                                                                                           | 3     |
| **\_ \_ protezione della posta elettronica EKU di CAPICOM \_**        | Il certificato può essere usato per la protezione della posta elettronica.<br/>                                                                                                    | 4     |
| **\_ \_ accesso smart card EKU CAPICOM \_**         | È possibile utilizzare il certificato per l'accesso con smart card. Introdotta in capicol 2,0.<br/>                                                                         | 5     |
| **\_crittografia EKU del \_ \_ file \_ System per CAPICOM** | Il certificato può essere usato per EFS. Introdotta in capicol 2,0.<br/>                                                                                      | 6     |



## <a name="remarks"></a>Commenti

Il tipo di enumerazione **\_ EKU CAPICOM** viene usato dall' [**EKU. Proprietà Name**](eku-name.md) .

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




