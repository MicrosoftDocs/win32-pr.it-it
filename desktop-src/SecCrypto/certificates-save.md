---
description: Salva gli oggetti Certificate nella raccolta.
ms.assetid: 1d4b7bd5-3ed3-4ace-9894-4e89c5cf844f
title: Metodo Certificates.Save
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: c3d724a6859a1fbc7765822227290facfb2c2f021fce2f5815f32c5e91fe6453
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120126761"
---
# <a name="certificatessave-method"></a>Metodo Certificates.Save

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/previous-versions/windows/embedded/hh424013(v=msdn.10)) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Save** salva gli oggetti [**Certificate**](certificate.md) nella raccolta .

## <a name="syntax"></a>Sintassi


```VB
Certificates.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal ExportFlag ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FileName* \[ Pollici\]
</dt> <dd>

Stringa che contiene il nome del file di output in cui verranno salvati i certificati.

</dd> <dt>

*Password* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene la password [*in testo non crittografato*](../secgloss/p-gly.md) per un file [*di chiave*](../secgloss/p-gly.md) privata. Il valore predefinito è una stringa vuota (""). Per la password è possibile usare fino a 32 caratteri Unicode, incluso un carattere null di terminazione. Per informazioni sulla protezione della password, vedere [Gestione delle password.](../secbp/handling-passwords.md)

</dd> <dt>

*SaveAs* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione [**CAPICOM \_ CERTIFICATES SAVE AS \_ \_ \_ TYPE**](capicom-certificates-save-as-type.md) che specifica il formato del file di output. Il valore predefinito è CAPICOM \_ CERTIFICATES \_ SAVE AS \_ \_ PFX. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                          | Significato                                              |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PFX"></span><span id="capicom_certificates_save_as_pfx"></span><dl> <dt>**SALVATAGGIO DEI CERTIFICATI CAPICOM \_ \_ COME \_ \_ PFX**</dt> </dl>                      | I certificati vengono salvati come PFX.<br/>      |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_PKCS7"></span><span id="capicom_certificates_save_as_pkcs7"></span><dl> <dt>**CERTIFICATI CAPICOM \_ \_ \_ SALVANO \_ COME PKCS7**</dt> </dl>                | I certificati vengono salvati come PKCS \# 7.<br/> |
| <span id="CAPICOM_CERTIFICATES_SAVE_AS_SERIALIZED"></span><span id="capicom_certificates_save_as_serialized"></span><dl> <dt>**CERTIFICATI CAPICOM \_ \_ SALVA COME \_ \_ SERIALIZZATI**</dt> </dl> | I certificati vengono salvati come serializzati.<br/> |



 

</dd> <dt>

*ExportFlag* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione [**CAPICOM \_ EXPORT \_ FLAG**](capicom-export-flag.md) che specifica se eventuali errori di esportazione della chiave privata vengono ignorati. Il valore predefinito è CAPICOM \_ EXPORT \_ DEFAULT. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                                                                          | Significato                                               |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------|
| <span id="CAPICOM_EXPORT_DEFAULT"></span><span id="capicom_export_default"></span><dl> <dt>**IMPOSTAZIONE PREDEFINITA \_ DELL'ESPORTAZIONE \_ CAPICOM**</dt> </dl>                                                                                                      | Gli errori di esportazione della chiave privata non vengono ignorati.<br/> |
| <span id="CAPICOM_EXPORT_IGNORE_PRIVATE_KEY_NOT_EXPORTABLE_ERROR"></span><span id="capicom_export_ignore_private_key_not_exportable_error"></span><dl> <dt>**ERRORE CAPICOM EXPORT IGNORE PRIVATE KEY NOT EXPORTABLE (IGNORA CHIAVE \_ \_ PRIVATA NON \_ \_ \_ \_ \_ ESPORTABILE)**</dt> </dl> | Gli errori di esportazione della chiave privata vengono ignorati.<br/>     |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo genera CAPICOM \_ E NOT ALLOWED quando viene generato tramite script da \_ \_ un'applicazione basata sul Web.

Gli [**oggetti**](certificate.md) Certificato possono essere recuperati usando il [**metodo Store.Load.**](store-load.md)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Certificati**](certificates.md)
</dt> </dl>

 

 
