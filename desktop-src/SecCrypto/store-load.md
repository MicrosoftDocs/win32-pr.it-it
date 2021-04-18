---
description: Importa i certificati da un file nell'archivio.
ms.assetid: 884326b4-77ca-43d4-bda9-127d823ce9bc
title: Store. Load (metodo)
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
ms.openlocfilehash: 32261a6fd8c5cf4382832d8286d63ce5d44fb542
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106333873"
---
# <a name="storeload-method"></a>Store. Load (metodo)

\[Il metodo **Load** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Load** importa i certificati da un file nell'archivio.

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

*Nome file* \[ in\]
</dt> <dd>

Stringa che contiene il percorso di un file con estensione cer, SST, SPC, p7s o pfx o qualsiasi file firmato Authenticode.

</dd> <dt>

*Password* \[ di in, facoltativo\]
</dt> <dd>

Stringa che contiene la password in testo non crittografato per il file. Per la password è possibile usare fino a 32 caratteri Unicode, incluso un carattere null di terminazione. Per informazioni sulla protezione della password, vedere [gestione delle password](../secbp/handling-passwords.md).

</dd> <dt>

*KeyStorageFlag* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ \_ flag di archiviazione della chiave CAPICOM**](capicom-key-storage-flag.md) che definisce i flag di archiviazione delle chiavi. Il valore predefinito è CAPICOM \_ Key \_ storage \_ default. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                           | Significato                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <span id="CAPICOM_KEY_STORAGE_DEFAULT"></span><span id="capicom_key_storage_default"></span><dl> <dt>**archiviazione delle chiavi di CAPICOM \_ \_ \_ predefinite**</dt> </dl>                       | Archiviazione chiavi predefinita.<br/>       |
| <span id="CAPICOM_KEY_STORAGE_EXPORTABLE"></span><span id="capicom_key_storage_exportable"></span><dl> <dt>**\_archiviazione chiavi CAPICOM \_ \_ esportabile**</dt> </dl>              | La chiave è esportabile.<br/>     |
| <span id="CAPICOM_KEY_STORAGE_USER_PROTECTED"></span><span id="capicom_key_storage_user_protected"></span><dl> <dt>**archiviazione delle chiavi di CAPICOM \_ \_ \_ protetta dall'utente \_**</dt> </dl> | La chiave è protetta dall'utente.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se il metodo **Load** viene chiamato in un archivio di memoria, tutti i contenitori di chiavi creati verranno eliminati quando l'archivio di memoria viene eliminato. Se, ad esempio, un file con estensione PFX viene caricato in un archivio di memoria e successivamente aggiunto a un archivio di sistema, ad esempio archivio personale, dall'archivio memoria, il certificato nell'archivio personale non conterrà una chiave. In questo caso, il file con estensione pfx deve essere caricato direttamente nell'archivio personale.

Questo metodo genera CAPICOM \_ E \_ non \_ è consentito quando viene inserito nello script da un'applicazione basata sul Web.

Se la password non riesce a decrittografare il file di chiave privata, è necessario eseguire una query sul [*provider del servizio di crittografia*](../secgloss/c-gly.md) (CSP) predefinito. Se il CSP predefinito è il provider di crittografia di base di Microsoft e l'operazione di decrittografia ha esito negativo, l'operazione di decrittografia deve essere riprovata con il provider Microsoft Strong Cryptographic Provider o Microsoft Enhanced Cryptographic Provider, a seconda di quale sia disponibile.

Se il certificato caricato nell'archivio è identico a quello già presente, il metodo **Load** eliminerà il certificato esistente dall'archivio e quindi aggiungerà il nuovo certificato. Il nuovo certificato erediterà le proprietà dal certificato esistente. Il contenitore di chiavi private esistente viene sostituito dal nuovo contenitore di chiavi private.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Store**](store.md)
</dt> </dl>

 

 
