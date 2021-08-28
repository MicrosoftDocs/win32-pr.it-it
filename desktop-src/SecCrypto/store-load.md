---
description: Importa i certificati da un file nell'archivio.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Metodo Store.Load
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Load
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 1b39c2be625ff88869d27e6210e49496352af868c73557d2657c509fd0e79f82
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897791"
---
# <a name="storeload-method"></a>Metodo Store.Load

\[Il **metodo** Load è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Load** importa i certificati da un file nell'archivio.

## <a name="syntax"></a>Sintassi


```VB
Store.Load( _
  ByVal FileName, _
  [ ByVal Password ], _
  [ ByVal KeyStorageFlag ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FileName* \[ Pollici\]
</dt> <dd>

Stringa contenente il percorso di un file con estensione cer, sst, spc, p7s o pfx o qualsiasi file firmato Authenticode.

</dd> <dt>

*Password* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene la password di testo non crittografato per il file. Per la password è possibile usare fino a 32 caratteri Unicode, incluso un carattere null di terminazione. Per informazioni sulla protezione della password, vedere [Gestione delle password](../secbp/handling-passwords.md).

</dd> <dt>

*KeyStorageFlag* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione [**CAPICOM \_ KEY STORAGE \_ \_ FLAG**](capicom-key-storage-flag.md) che definisce i flag di archiviazione delle chiavi. Il valore predefinito è CAPICOM \_ KEY \_ STORAGE \_ DEFAULT. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                           | Significato                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**IMPOSTAZIONE PREDEFINITA \_ DI ARCHIVIAZIONE \_ CHIAVI \_ CAPICOM**</dt> </dl>                       | Archiviazione chiavi predefinita.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**ARCHIVIAZIONE CHIAVI CAPICOM \_ \_ \_ ESPORTABILE**</dt> </dl>              | La chiave è esportabile.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**PROTEZIONE \_ DELL'UTENTE \_ DI ARCHIVIAZIONE \_ CHIAVI \_ CAPICOM**</dt> </dl> | La chiave è protetta dall'utente.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il **metodo Load** viene chiamato su un archivio di memoria, tutti i contenitori di chiavi creati verranno eliminati quando l'archivio di memoria viene eliminato. Ad esempio, se un file con estensione pfx viene caricato in un archivio di memoria e successivamente aggiunto a un archivio di sistema (ad esempio l'archivio my) dall'archivio di memoria, il certificato nell'archivio my non conterrà una chiave. In questo caso, il file con estensione pfx deve essere caricato direttamente nell'archivio my.

Questo metodo genera CAPICOM \_ E NOT ALLOWED quando viene eseguito lo script da \_ \_ un'applicazione basata sul Web.

Se la password non riesce a decrittografare il file di chiave privata, è necessario eseguire query sul [*provider*](../secgloss/c-gly.md) del servizio di crittografia (CSP) predefinito. Se il provider di crittografia predefinito è Microsoft Base Cryptographic Provider e l'operazione di decrittografia ha esito negativo, è necessario riprovare a eseguire l'operazione di decrittografia con Microsoft Strong Cryptographic Provider o Microsoft Enhanced Cryptographic Provider, a seconda di quale sia disponibile.

Se il certificato caricato nell'archivio è uguale a quello già presente, il metodo **Load** eliminerà il certificato esistente dall'archivio e quindi aggiungerà il nuovo certificato. Il nuovo certificato erediterà le proprietà dal certificato esistente. Il contenitore di chiavi private esistente viene sostituito dal nuovo contenitore di chiavi private.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Archiviazione**](store.md)
</dt> </dl>

 

 
