---
description: Imposta o Recupera il nome del CAPICOM dell'attributo. Si tratta della proprietà predefinita.
ms.assetid: 082f286e-f2ac-4e45-94b9-abdaa3f4c926
title: Proprietà Attribute.Name
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
ms.openlocfilehash: f71bb231941765dd073d44abd11c56152ea2d975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324916"
---
# <a name="attributename-property"></a>Proprietà Attribute.Name

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista, Windows XP. Usare invece la [**classe CryptographicAttributeObject**](/dotnet/api/system.security.cryptography.cryptographicattributeobject?view=dotnet-plat-ext-3.1&preserve-view=true) nello spazio dei nomi [**System. Security. Cryptography**](/previous-versions/windows/) .\]

La proprietà **Name** imposta o Recupera il nome del CAPICOM dell'attributo. Si tratta della proprietà predefinita.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
Attribute.Name As CAPICOM_ATTRIBUTE
```



## <a name="property-value"></a>Valore proprietà

Valore dell'enumerazione dell' [**\_ attributo CAPICOM**](capicom-attribute.md) che specifica il nome del CAPICOM dell'attributo. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                                                                 | Significato                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_SIGNING_TIME"></span><span id="capicom_authenticated_attribute_signing_time"></span><dl> <dt>**\_tempo di firma dell'attributo autenticato di CAPICOM \_ \_ \_**</dt> </dl>                         | L'attributo contiene la data e l'ora di creazione della firma.<br/> |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_NAME"></span><span id="capicom_authenticated_attribute_document_name"></span><dl> <dt>**\_nome del documento dell'attributo autenticato di CAPICOM \_ \_ \_**</dt> </dl>                      | L'attributo contiene il nome del documento firmato.<br/>         |
| <span id="CAPICOM_AUTHENTICATED_ATTRIBUTE_DOCUMENT_DESCRIPTION"></span><span id="capicom_authenticated_attribute_document_description"></span><dl> <dt>**\_Descrizione del documento dell'attributo autenticato CAPICOM \_ \_ \_**</dt> </dl> | L'attributo contiene una descrizione del documento firmato.<br/>    |



 

## <a name="remarks"></a>Commenti

Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero stato dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Attributo**](attribute.md)
</dt> </dl>

 

 
