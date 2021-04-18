---
description: Importa un certificato da un file.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: 'Metodo ICertificate2:: Load'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate.Load
- ICertificate2.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9193297ad7eacc1994e4bf3729a87054573b1574
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106324409"
---
# <a name="icertificate2load-method"></a>Metodo ICertificate2:: Load

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Load** importa un certificato da un file. Questo metodo è stato introdotto in capicol 2,0.

## <a name="syntax"></a>Sintassi


```VB
Certificate.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ], _
  [ ByVal KeyLocation ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*Nome file* \[ in\]
</dt> <dd>

Stringa che contiene il percorso di un file con estensione cer o PFX che contiene i dati del certificato.

</dd> <dt>

*Password* \[ di in, facoltativo\]
</dt> <dd>

Stringa che contiene la password in [*testo non crittografato*](../secgloss/p-gly.md) per il file di [*chiave privata*](../secgloss/p-gly.md) . La password può contenere fino a 32 caratteri Unicode, incluso un carattere di terminazione null. Per informazioni sulla protezione della password, vedere [gestione delle password](../secbp/handling-passwords.md).

</dd> <dt>

*KeyStorageFlag* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ \_ flag di archiviazione della chiave CAPICOM**](capicom-key-storage-flag.md) che definisce i flag di archiviazione delle chiavi. Il valore predefinito è CAPICOM \_ Key \_ storage \_ default. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                           | Significato                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**archiviazione delle chiavi di CAPICOM \_ \_ \_ predefinite**</dt> </dl>                       | Archiviazione chiavi predefinita.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**\_archiviazione chiavi CAPICOM \_ \_ esportabile**</dt> </dl>              | La chiave è esportabile.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**archiviazione delle chiavi di CAPICOM \_ \_ \_ protetta dall'utente \_**</dt> </dl> | La chiave è protetta dall'utente.<br/> |



 

</dd> <dt>

*Posizione della sede* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ percorso della chiave CAPICOM**](capicom-key-location.md) che definisce i tipi di posizione chiave. Il valore predefinito è CAPICOM \_ \_ chiave utente corrente \_ . Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                               | Significato                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <dt>**\_ \_ chiave utente corrente di CAPICOM \_**</dt> </dl>    | La chiave è una chiave utente.<br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <dt>**\_chiave del computer locale \_ CAPICOM \_**</dt> </dl> | La chiave è una chiave del computer.<br/> |



 

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



 

 
