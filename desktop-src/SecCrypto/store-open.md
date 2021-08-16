---
description: Apre un archivio certificati specificato.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Metodo Store.Open
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Store.Open
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: d70c6410d0ecb8edb91aa722bcf6f35cb9536c3ed2b7f03c2d5cb141937aeb69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118897807"
---
# <a name="storeopen-method"></a>Metodo Store.Open

\[Il **metodo** Open è disponibile per l'uso nei sistemi operativi specificati nella sezione Requisiti. Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Open** apre un archivio certificati [*specificato.*](../secgloss/c-gly.md) Per impostazione predefinita, il percorso \_ CAPICOM CURRENT USER STORE e l'archivio CAPICOM MY STORE vengono \_ aperti in \_ sola \_ \_ lettura.

## <a name="syntax"></a>Sintassi


```VB
Store.Open( _
  [ ByVal StoreLocation ], _
  [ ByVal StoreName ], _
  [ ByVal OpenMode ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*StoreLocation* \[ in, facoltativo\]
</dt> <dd>

Valore [dell'enumerazione CAPICOM \_ STORE \_ LOCATION](capicom-store-location.md) che indica il percorso dell'archivio da aprire. Il valore predefinito è CAPICOM \_ CURRENT \_ USER \_ STORE. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**ARCHIVIO UTENTI \_ CAPICOM ACTIVE \_ DIRECTORY \_ \_**</dt> </dl> | L'archivio è un archivio di Active Directory. Non verrà generato alcun errore se un archivio di Active Directory viene aperto in lettura/scrittura, ma le modifiche apportate all'archivio non verranno rese persistenti. I certificati non possono essere aggiunti o rimossi dagli archivi di Active Directory.<br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**ARCHIVIO UTENTI CORRENTI CAPICOM \_ \_ \_**</dt> </dl>                             | L'archivio è un archivio utente corrente. Un archivio utente corrente può essere un archivio di lettura/scrittura. In caso contrario, le modifiche apportate al contenuto dell'archivio vengono rese persistenti.<br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**ARCHIVIO \_ DEL COMPUTER \_ LOCALE \_ CAPICOM**</dt> </dl>                          | L'archivio è un archivio di computer locale. Gli archivi di computer locali possono essere archivi di lettura/scrittura solo se l'utente dispone di autorizzazioni di lettura/scrittura. Se l'utente dispone di autorizzazioni di lettura/scrittura e se l'archivio è aperto in lettura/scrittura, le modifiche nel contenuto dell'archivio vengono rese persistenti.<br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**ARCHIVIO DI \_ MEMORIA \_ CAPICOM**</dt> </dl>                                                | L'archivio è un archivio di memoria. Le modifiche apportate al contenuto dell'archivio non vengono rese persistenti.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**ARCHIVIO UTENTI \_ DI SMART \_ CARD \_ \_ CAPICOM**</dt> </dl>                   | L'archivio è il gruppo di smart card presenti. Introduzione a CAPICOM 2.0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*StoreName* \[ in, facoltativo\]
</dt> <dd>

Stringa contenente il nome dell'archivio certificati di sistema da aprire. Il valore predefinito è CAPICOM \_ MY \_ STORE. Se l'archivio viene aperto da uno script Web, il carattere barra rovesciata ( \\ ) non è consentito nel nome. Oltre agli archivi definiti dal sistema, è possibile aprire gli archivi definiti dall'utente.

Questo parametro può essere un archivio definito dall'utente o uno degli archivi certificati di sistema seguenti.



| Valore                                                                                                                                                                            | Significato                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <dt>**ARCHIVIO \_ CA \_ CAPICOM**</dt> </dl>          | Archivio CA. Questo archivio viene usato per archiviare i certificati ca intermedi.<br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <dt>**CAPICOM \_ MY \_ STORE**</dt> </dl>          | Il mio negozio. Questo archivio viene usato per i certificati personali di un utente.<br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <dt>**CAPICOM \_ OTHER \_ STORE**</dt> </dl> | Archivio AddressBook. Questo archivio viene usato per mantenere i certificati di altri utenti.<br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <dt>**ARCHIVIO RADICE \_ \_ CAPICOM**</dt> </dl>    | Archivio radice. Questo archivio viene usato per archiviare la CA radice e i certificati attendibili autofirmati.<br/> |



 

</dd> <dt>

*OpenMode* \[ in, facoltativo\]
</dt> <dd>

Valore [dell'enumerazione CAPICOM \_ STORE OPEN \_ \_ MODE](capicom-store-open-mode.md) che indica la modalità di apertura dell'archivio. Il valore predefinito è CAPICOM \_ STORE \_ OPEN READ \_ \_ ONLY. Se l'archivio viene aperto da uno script Web, questo valore viene forzato a CAPICOM \_ STORE \_ OPEN EXISTING \_ \_ ONLY. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                           | Significato                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <dt>**CAPICOM \_ STORE OPEN MAXIMUM ALLOWED (APERTURA MASSIMA CONSENTITA PER CAPICOM \_ \_ \_ STORE)**</dt> </dl> | Aprire l'archivio in modalità lettura/scrittura se l'utente dispone delle autorizzazioni di lettura/scrittura; In caso contrario, aprire l'archivio in modalità di sola lettura.<br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ READ \_ ONLY**</dt> </dl>                   | Aprire l'archivio in modalità di sola lettura.<br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ READ \_ WRITE**</dt> </dl>                | Aprire l'archivio in modalità lettura/scrittura.<br/>                                                                                     |



 

I flag seguenti possono essere combinati con i valori della tabella precedente usando un'operazione **or logico.**



| Valore                                                                                                                                                                                                                              | Significato                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <dt>**CAPICOM \_ STORE OPEN EXISTING ONLY \_ \_ (APRI SOLO \_ ESISTENTE)**</dt> </dl>          | Aprire solo gli archivi esistenti; non creare un nuovo archivio. Introduzione a CAPICOM 2.0.<br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <dt>**CAPICOM \_ STORE \_ OPEN \_ INCLUDE \_ ARCHIVED**</dt> </dl> | Includere i certificati archiviati quando si usa l'archivio. Introduzione a CAPICOM 2.0.<br/>   |



 

Gli archivi in alcune posizioni possono essere aperti solo in modalità di sola lettura. Sono inclusi tutti gli archivi in CAPICOM LOCAL MACHINE STORE per i quali \_ \_ \_ l'utente non dispone delle autorizzazioni di scrittura. I tentativi di apertura di un archivio come archivio di lettura/scrittura senza accesso e autorizzazioni appropriate comportano l'errore del **metodo Open.** Gli archivi Active Directory possono essere aperti come archivio di lettura/scrittura senza errori del metodo **Open,** ma le modifiche apportate all'archivio non verranno rese persistenti.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se questo metodo viene chiamato in un archivio SmartCard, è possibile richiamare altre interfacce utente smart card.

> [!IMPORTANT]
> Quando questo metodo viene chiamato da uno script Web, lo script deve accedere ai certificati digitali nel computer locale. Se si consente allo script di accedere ai certificati digitali, anche il sito Web da cui viene eseguito lo script avrà accesso alle informazioni personali archiviate nei certificati. La prima volta che questo metodo viene chiamato da un dominio specifico, viene generata una finestra di dialogo in cui l'utente deve indicare se l'accesso ai certificati deve essere consentito. Gli archivi aperti da uno script Web forzano automaticamente il flag CAPICOM \_ STORE \_ OPEN EXISTING \_ \_ ONLY.

 

Se *StoreLocation è* **CAPICOM SMART CARD USER \_ \_ \_ \_ STORE,** *StoreName viene* ignorato. In questo caso CAPICOM legge tutti i certificati di tutti i lettori disponibili che contengono un smart card.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Archiviazione**](store.md)
</dt> <dt>

[**Oggetti di crittografia**](cryptography-objects.md)
</dt> <dt>

[**Chiudi**](store-close.md)
</dt> </dl>

 

 
