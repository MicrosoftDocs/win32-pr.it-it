---
description: Imposta o recupera un valore di enumerazione che specifica il nome CAPICOM dell'EKU. Si tratta della proprietà predefinita.
ms.assetid: afce5553-ef18-4a7f-b1c8-fbe00d3277e0
title: Proprietà IEKU::Name
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
ms.openlocfilehash: ca1564b943874ec086dd5e4459e69543cbdc90ebde2a11a2084c3054e3727dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767229"
---
# <a name="iekuname-property"></a>Proprietà IEKU::Name

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509EnhancedKeyUsageExtension**](/dotnet/api/system.security.cryptography.x509certificates.x509enhancedkeyusageextension?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

La **proprietà Name** imposta o recupera un valore di enumerazione che specifica il nome CAPICOM dell'EKU. Si tratta della proprietà predefinita.

Si tratta di una proprietà di lettura/scrittura.

## <a name="syntax"></a>Sintassi


```VB
EKU.Name As CAPICOM_EKU
```



## <a name="property-value"></a>Valore proprietà

Valore [**dell'enumerazione \_ CAPICOM EKU**](capicom-eku.md) che specifica il nome CAPICOM dell'EKU. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                           | Significato                                                                                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_EKU_OTHER"></span><span id="capicom_eku_other"></span><dl> <dt>**CAPICOM \_ EKU \_ OTHER**</dt> </dl>                                                      | Il certificato usa definito nei criteri locali. Viene usato se l'EKU necessario non è predefinito e il valore OID deve essere impostato dall'applicazione.<br/> |
| <span id="CAPICOM_EKU_SERVER_AUTH"></span><span id="capicom_eku_server_auth"></span><dl> <dt>**CAPICOM \_ EKU \_ SERVER \_ AUTH**</dt> </dl>                                   | Il certificato può essere usato per autenticare un server.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CLIENT_AUTH"></span><span id="capicom_eku_client_auth"></span><dl> <dt>**AUTENTICAZIONE CLIENT \_ CAPICOM \_ \_ EKU**</dt> </dl>                                   | Il certificato può essere usato per autenticare un client.<br/>                                                                                                |
| <span id="CAPICOM_EKU_CODE_SIGNING"></span><span id="capicom_eku_code_signing"></span><dl> <dt>**FIRMA DEL CODICE EKU CAPICOM \_ \_ \_**</dt> </dl>                                | Il certificato può essere usato per creare una firma digitale.<br/>                                                                                           |
| <span id="CAPICOM_EKU_EMAIL_PROTECTION"></span><span id="capicom_eku_email_protection"></span><dl> <dt>**PROTEZIONE DELLA POSTA ELETTRONICA DI CAPICOM \_ EKU \_ \_**</dt> </dl>                    | Il certificato può essere usato per la protezione della posta elettronica.<br/>                                                                                                    |
| <span id="CAPICOM_EKU_SMARTCARD_LOGON"></span><span id="capicom_eku_smartcard_logon"></span><dl> <dt>**ACCESSO \_ ALLA SMART CARD CAPICOM EKU \_ \_**</dt> </dl>                       | Il certificato può essere usato per smart card accesso. Introdotto in CAPICOM 2.0.<br/>                                                                         |
| <span id="CAPICOM_EKU_ENCRYPTING_FILE_SYSTEM"></span><span id="capicom_eku_encrypting_file_system"></span><dl> <dt>**FILE \_ \_ \_ \_ SYSTEM DI CRITTOGRAFIA CAPICOM EKU**</dt> </dl> | Il certificato può essere usato per EFS. Introdotto in CAPICOM 2.0.<br/>                                                                                      |



 

## <a name="remarks"></a>Commenti

Quando il valore di questa proprietà viene reimpostato, direttamente o indirettamente, viene [*reimpostato*](../secgloss/s-gly.md) l'intero stato dell'oggetto.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
