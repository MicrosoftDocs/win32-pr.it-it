---
description: Salva il certificato in un file.
ms.assetid: 2012b39b-47fd-4071-9752-98bb10954fc0
title: 'Metodo ICertificate2:: Save'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Save
- ICertificate2.Save
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 3427feb86c705f5558d083bc39673fdf77553f58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327098"
---
# <a name="icertificate2save-method"></a>Metodo ICertificate2:: Save

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Save** Salva il certificato in un file. Questo metodo è stato introdotto in capicol 2,0.

## <a name="syntax"></a>Sintassi


```VB
Certificate.Save( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal SaveAs ], _
  [ ByVal IncludeOption ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome file* \[ in\]
</dt> <dd>

Stringa che contiene il nome del file di output in cui verrà salvato il certificato.

</dd> <dt>

*Password* \[ di in, facoltativo\]
</dt> <dd>

Stringa che contiene la password in [*testo non crittografato*](../secgloss/p-gly.md) per un file di [*chiave privata*](../secgloss/p-gly.md) . La password può contenere fino a 32 caratteri Unicode, incluso un carattere di terminazione null. Per informazioni sulla protezione della password, vedere [gestione delle password](../secbp/handling-passwords.md).

</dd> <dt>

*SaveAs* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione dei [**\_ \_ \_ \_ tipi Salva come del certificato CAPICOM**](capicom-certificate-save-as-type.md) che specifica il formato del file di output. Il valore predefinito è il **\_ certificato CAPICOM \_ Salva \_ come \_ CER**. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                  | Significato                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_CER"></span><span id="capicom_certificate_save_as_cer"></span><dl> <dt>**\_certificato CAPICOM \_ Salva \_ come \_ CER**</dt> </dl> | Il file di output verrà formattato come file con estensione CER senza chiavi private salvate.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_SAVE_AS_PFX"></span><span id="capicom_certificate_save_as_pfx"></span><dl> <dt>**certificato capicol \_ \_ Salva \_ come \_ PFX**</dt> </dl> | Il file di output verrà formattato come file con estensione pfx (PKCS \# 12) e verranno salvate anche tutte le chiavi private associate esportabili.<br/> |



 

</dd> <dt>

*IncludeOption* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione dell' [**\_ \_ \_ opzione Includi certificato CAPICOM**](capicom-certificate-include-option.md) che specifica il numero di certificati nella catena salvati nel file di output. Il valore predefinito è il certificato capicol \_ \_ include \_ \_ solo l'entità end \_ . Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                                             | Significato                                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_INCLUDE_CHAIN_EXCEPT_ROOT"></span><span id="capicom_certificate_include_chain_except_root"></span><dl> <dt>**il certificato di \_ CAPICOM \_ include la \_ catena \_ ad eccezione della \_ radice**</dt> </dl> | Salva tutti i certificati nella catena con l'eccezione dell'entità radice<br/> |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_WHOLE_CHAIN"></span><span id="capicom_certificate_include_whole_chain"></span><dl> <dt>**il certificato di \_ CAPICOM \_ include l' \_ intera \_ catena**</dt> </dl>                    | Salva la catena di certificati completa<br/>                                      |
| <span id="CAPICOM_CERTIFICATE_INCLUDE_END_ENTITY_ONLY"></span><span id="capicom_certificate_include_end_entity_only"></span><dl> <dt>**il certificato capicol \_ \_ include \_ \_ solo entità finale \_**</dt> </dl>       | Salva solo il certificato di entità finale<br/>                                     |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo genera CAPICOM \_ E \_ non \_ è consentito quando viene inserito nello script da un'applicazione basata sul Web.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
