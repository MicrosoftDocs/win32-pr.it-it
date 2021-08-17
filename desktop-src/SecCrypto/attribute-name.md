---
description: Imposta o recupera il nome CAPICOM dell'attributo. Si tratta della proprietà predefinita.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Attribute.Name proprietà
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attribute.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3234d02e5e0f68817896f2d0c9d05be25b55bbe97f49fea4d34bafbab627b2c9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117773655"
---
# <a name="attributename-property"></a>Attribute.Name proprietà

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio [**dei nomi System.Security.Cryptography.**](/previous-versions/windows/)\]

La **proprietà Name** imposta o recupera il nome CAPICOM dell'attributo. Si tratta della proprietà predefinita.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a>Valore proprietà

Valore [**dell'enumerazione CAPICOM \_ ATTRIBUTE**](capicom-attribute.md) che specifica il nome CAPICOM dell'attributo. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                                                                 | Significato                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <dt>**ORA DI FIRMA \_ DELL'ATTRIBUTO AUTENTICATO \_ \_ CAPICOM \_**</dt> </dl>                         | L'attributo contiene l'ora di creazione della firma.<br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <dt>**NOME DOCUMENTO ATTRIBUTO AUTENTICATO CAPICOM \_ \_ \_ \_**</dt> </dl>                      | L'attributo contiene il nome del documento firmato.<br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <dt>**DESCRIZIONE \_ DEL DOCUMENTO DELL'ATTRIBUTO AUTENTICATO \_ \_ CAPICOM \_**</dt> </dl> | L'attributo contiene una descrizione del documento firmato.<br/>    |



 

## <a name="remarks"></a>Commenti

Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero stato dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributo**](attribute.md)
</dt> </dl>

 

 
