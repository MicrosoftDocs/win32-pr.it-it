---
description: Importa un certificato da un file.
ms.assetid: 62c3bf8e-2f52-4342-b3ee-744b032578bf
title: Metodo ICertificate2::Load
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
ms.openlocfilehash: fceb6ba9a9868711aefae64865c08e49551e20e8a05686e1691f390f05b76071
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117771537"
---
# <a name="icertificate2load-method"></a>Metodo ICertificate2::Load

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Load** importa un certificato da un file. Questo metodo è stato introdotto in CAPICOM 2.0.

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

*FileName* \[ Pollici\]
</dt> <dd>

Stringa contenente il percorso di un file con estensione cer o pfx che contiene i dati del certificato.

</dd> <dt>

*Password* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene la password [*di testo non*](../secgloss/p-gly.md) crittografato per il file di [*chiave*](../secgloss/p-gly.md) privata. La password può contenere fino a 32 caratteri Unicode, incluso un carattere Null di terminazione. Per informazioni sulla protezione della password, vedere [Gestione delle password](../secbp/handling-passwords.md).

</dd> <dt>

*KeyStorageFlag* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione [**CAPICOM \_ KEY STORAGE \_ \_ FLAG**](capicom-key-storage-flag.md) che definisce i flag di archiviazione delle chiavi. Il valore predefinito è CAPICOM \_ KEY \_ STORAGE \_ DEFAULT. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                           | Significato                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**IMPOSTAZIONE PREDEFINITA \_ DI ARCHIVIAZIONE \_ CHIAVI \_ CAPICOM**</dt> </dl>                       | Archiviazione chiavi predefinita.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**ARCHIVIAZIONE CHIAVI CAPICOM \_ \_ \_ ESPORTABILE**</dt> </dl>              | La chiave è esportabile.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**PROTEZIONE \_ DELL'UTENTE \_ DI ARCHIVIAZIONE \_ CHIAVI \_ CAPICOM**</dt> </dl> | La chiave è protetta dall'utente.<br/> |



 

</dd> <dt>

*KeyLocation* \[ in, facoltativo\]
</dt> <dd>

Valore [**dell'enumerazione CAPICOM \_ KEY \_ LOCATION**](capicom-key-location.md) che definisce i tipi di posizione della chiave. Il valore predefinito è CAPICOM \_ CURRENT \_ USER \_ KEY. Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                               | Significato                              |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------|
| <span id="CAPICOM_CURRENT_USER_KEY"></span><span id="capicom_current_user_key"></span><dl> <dt>**CHIAVE UTENTE CORRENTE \_ \_ \_ CAPICOM**</dt> </dl>    | La chiave è una chiave utente.<br/>    |
| <span id="CAPICOM_LOCAL_MACHINE_KEY"></span><span id="capicom_local_machine_key"></span><dl> <dt>**CHIAVE \_ DEL COMPUTER \_ LOCALE \_ CAPICOM**</dt> </dl> | La chiave è una chiave del computer.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Questo metodo genera CAPICOM \_ E NOT ALLOWED quando viene eseguito lo script da \_ \_ un'applicazione basata sul Web.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
