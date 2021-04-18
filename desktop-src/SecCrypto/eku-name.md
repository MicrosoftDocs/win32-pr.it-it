---
description: Imposta o recupera un valore di enumerazione che specifica il nome di CAPICOM dell'EKU. Si tratta della proprietà predefinita.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: 'Proprietà IEKU:: Name'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEKU.Name
- IEKU.get_Name
- IEKU.put_Name
- EKU.Name
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e0e28a8816d7e4c4f44e3cd1ec0dc479372d66d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106330912"
---
# <a name="iekuname-property"></a>Proprietà IEKU:: Name

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

La proprietà **Name** imposta o recupera un valore di enumerazione che specifica il nome di CAPICOM dell'EKU. Si tratta della proprietà predefinita.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a>Valore proprietà

Valore dell'enumerazione [**\_ EKU di CAPICOM**](capicom-eku.md) che specifica il nome di CAPICOM dell'EKU. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                           | Significato                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <dt>**\_altro EKU di CAPICOM \_**</dt> </dl>                                                      | Il certificato ha usi definiti nei criteri locali. Viene usato se l'EKU necessario non è predefinito e il valore OID deve essere impostato dall'applicazione.<br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <dt>**\_ \_ autenticazione server EKU CAPICOM \_**</dt> </dl>                                   | Il certificato può essere usato per autenticare un server.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <dt>**\_ \_ autenticazione client EKU CAPICOM \_**</dt> </dl>                                   | Il certificato può essere usato per autenticare un client.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <dt>**\_firma del codice EKU \_ di \_ CAPICOM**</dt> </dl>                                | Il certificato può essere usato per creare una firma digitale.<br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <dt>**\_ \_ protezione della posta elettronica EKU di CAPICOM \_**</dt> </dl>                    | Il certificato può essere usato per la protezione della posta elettronica.<br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <dt>**\_ \_ accesso smart card EKU CAPICOM \_**</dt> </dl>                       | È possibile utilizzare il certificato per l'accesso con smart card. Introdotta in capicol 2,0.<br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <dt>**\_crittografia EKU del \_ \_ file \_ System per CAPICOM**</dt> </dl> | Il certificato può essere usato per EFS. Introdotta in capicol 2,0.<br/>                                                                                      |



 

## <a name="remarks"></a>Commenti

Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene reimpostato l'intero [*stato*](../secgloss/s-gly.md) dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
