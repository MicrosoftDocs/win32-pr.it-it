---
description: Apre un archivio certificati specificato.
ms.assetid: d6f398b4-dba6-4d84-b5eb-3c7737d17a6e
title: Store. Open (metodo)
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
ms.openlocfilehash: ef4ffe89a4b726ecfa33fb95d213d809cae2487b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106327086"
---
# <a name="storeopen-method"></a>Store. Open (metodo)

\[Il metodo **Open** è disponibile per l'uso nei sistemi operativi specificati nella sezione requisiti. Usare invece la [**classe X509Store**](/dotnet/api/system.security.cryptography.x509certificates.x509store?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Open** apre un [*archivio certificati*](../secgloss/c-gly.md)specificato. Per impostazione predefinita, il percorso dell' \_ \_ Archivio dell'utente di CAPICOM \_ e l'archivio archivio \_ personale \_ sono aperti come di sola lettura.

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

Valore dell'enumerazione del [ \_ \_ percorso dell'archivio CAPICOM](capicom-store-location.md) che indica il percorso dell'archivio da aprire. Il valore predefinito è CAPICOM ( \_ \_ archivio utente corrente) \_ . Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                              | Significato                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_ACTIVE_DIRECTORY_USER_STORE"></span><span id="capicom_active_directory_user_store"></span><dl> <dt>**\_archivio utenti di Active \_ directory \_ di \_ CAPICOM**</dt> </dl> | L'archivio è un archivio Active Directory. Se un archivio Active Directory viene aperto in modalità di lettura/scrittura, non verrà generato alcun errore, ma tutte le modifiche apportate all'archivio non verranno rese permanente. I certificati non possono essere aggiunti o rimossi dagli archivi Active Directory.<br/>                   |
| <span id="CAPICOM_CURRENT_USER_STORE"></span><span id="capicom_current_user_store"></span><dl> <dt>**\_ \_ archivio utente corrente CAPICOM \_**</dt> </dl>                             | L'archivio è un archivio utente corrente. Un archivio utente corrente può essere un archivio di lettura/scrittura. In caso contrario, le modifiche apportate al contenuto dell'archivio vengono rese permanente.<br/>                                                                                                                        |
| <span id="CAPICOM_LOCAL_MACHINE_STORE"></span><span id="capicom_local_machine_store"></span><dl> <dt>**\_Archivio del computer locale \_ CAPICOM \_**</dt> </dl>                          | L'archivio è un archivio del computer locale. Gli archivi del computer locale possono essere archivi di lettura/scrittura solo se l'utente dispone di autorizzazioni di lettura/scrittura. Se l'utente dispone di autorizzazioni di lettura/scrittura e se l'archivio è aperto in lettura/scrittura, le modifiche apportate al contenuto dell'archivio vengono rese permanente.<br/> |
| <span id="CAPICOM_MEMORY_STORE"></span><span id="capicom_memory_store"></span><dl> <dt>**\_Archivio di memoria CAPICOM \_**</dt> </dl>                                                | L'archivio è un archivio di memoria. Eventuali modifiche apportate al contenuto dell'archivio non vengono rese permanente.<br/>                                                                                                                                                                                |
| <span id="CAPICOM_SMART_CARD_USER_STORE"></span><span id="capicom_smart_card_user_store"></span><dl> <dt>**\_ \_ \_ archivio utenti smart card \_ CAPICOM**</dt> </dl>                   | L'archivio è il gruppo di smart card presenti. Introdotta in capicol 2,0.<br/>                                                                                                                                                                                               |



 

</dd> <dt>

*StoreName* \[ in, facoltativo\]
</dt> <dd>

Stringa che contiene il nome dell'archivio certificati di sistema da aprire. Il valore predefinito è CAPICOMe \_ My \_ Store. Se l'archivio viene aperto da uno script Web, il carattere barra rovesciata ( \\ ) non è consentito nel nome. Oltre agli archivi definiti dal sistema, è possibile aprire gli archivi definiti dall'utente.

Questo parametro può essere un archivio definito dall'utente o uno degli archivi certificati di sistema seguenti.



| Valore                                                                                                                                                                            | Significato                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CA_STORE"></span><span id="capicom_ca_store"></span><dl> <dt>**\_archivio CA CAPICOM \_**</dt> </dl>          | Archivio CA. Questo archivio viene usato per archiviare i certificati della CA intermedia.<br/>                        |
| <span id="CAPICOM_MY_STORE"></span><span id="capicom_my_store"></span><dl> <dt>**\_archivio personale di CAPICOM \_**</dt> </dl>          | Archivio personale. Questo archivio viene usato per i certificati personali di un utente.<br/>                           |
| <span id="CAPICOM_OTHER_STORE"></span><span id="capicom_other_store"></span><dl> <dt>**\_ \_ Archivio CAPICOM**</dt> </dl> | Archivio Rubrica. Questo archivio viene usato per conservare i certificati di altri utenti.<br/>                  |
| <span id="CAPICOM_ROOT_STORE"></span><span id="capicom_root_store"></span><dl> <dt>**\_archivio radice CAPICOM \_**</dt> </dl>    | Archivio radice. Questo archivio viene usato per archiviare la CA radice e i certificati attendibili autofirmati.<br/> |



 

</dd> <dt>

*OpenMode* \[ in, facoltativo\]
</dt> <dd>

Valore dell'enumerazione della [ \_ \_ \_ modalità di apertura dell'archivio CAPICOM](capicom-store-open-mode.md) che indica la modalità di apertura dell'archivio. Il valore predefinito è capicot \_ Store \_ aperto in \_ sola lettura \_ . Se l'archivio viene aperto da uno script Web, questo valore è forzato nell'archivio capicoy \_ \_ aperto \_ \_ solo esistente. Questo parametro può avere uno dei valori seguenti.



| Valore                                                                                                                                                                                                                           | Significato                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_MAXIMUM_ALLOWED"></span><span id="capicom_store_open_maximum_allowed"></span><dl> <dt>**\_ \_ \_ massimo \_ consentito per l'archivio CAPICOM**</dt> </dl> | Aprire l'archivio in modalità di lettura/scrittura se l'utente dispone di autorizzazioni di lettura/scrittura; in caso contrario, aprire l'archivio in modalità di sola lettura.<br/> |
| <span id="CAPICOM_STORE_OPEN_READ_ONLY"></span><span id="capicom_store_open_read_only"></span><dl> <dt>**\_Archivio CAPICOM aperto in \_ \_ sola lettura \_**</dt> </dl>                   | Aprire l'archivio in modalità di sola lettura.<br/>                                                                                      |
| <span id="CAPICOM_STORE_OPEN_READ_WRITE"></span><span id="capicom_store_open_read_write"></span><dl> <dt>**\_Archivio CAPICOM \_ aperto lettura/ \_ \_ scrittura**</dt> </dl>                | Aprire l'archivio in modalità di lettura/scrittura.<br/>                                                                                     |



 

I flag seguenti possono essere combinati con i valori della tabella precedente tramite **un'operazione or** logica.



| Valore                                                                                                                                                                                                                              | Significato                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <span id="CAPICOM_STORE_OPEN_EXISTING_ONLY"></span><span id="capicom_store_open_existing_only"></span><dl> <dt>**\_Archivio CAPICOM \_ aperto \_ \_ solo esistente**</dt> </dl>          | Apri solo archivi esistenti; non creare un nuovo archivio. Introdotta in capicol 2,0.<br/> |
| <span id="CAPICOM_STORE_OPEN_INCLUDE_ARCHIVED"></span><span id="capicom_store_open_include_archived"></span><dl> <dt>**\_ \_ Archivio CAPICOM aperto \_ include \_ archiviato**</dt> </dl> | Includere i certificati archiviati quando si usa l'archivio. Introdotta in capicol 2,0.<br/>   |



 

Gli archivi in alcune posizioni possono essere aperti solo in modalità di sola lettura. Sono inclusi tutti i punti vendita nell'archivio del computer locale capicol \_ \_ \_ per cui l'utente non dispone delle autorizzazioni di scrittura. Tenta di aprire un archivio come archivio di lettura/scrittura senza l'accesso e le autorizzazioni appropriate comporteranno l'errore del metodo **Open** . Gli archivi di Active Directory possono essere aperti come archivio di lettura/scrittura senza errori del metodo **Open** , ma le modifiche apportate all'archivio non verranno rese permanente.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo non restituisce valori.

## <a name="remarks"></a>Commenti

Se questo metodo viene chiamato in un archivio Smart Card, è possibile che vengano richiamate interfacce utente aggiuntive per la smart card.

> [!IMPORTANT]
> Quando questo metodo viene chiamato da uno script Web, lo script deve accedere ai certificati digitali sul computer locale. Se si consente allo script di accedere ai certificati digitali, il sito Web da cui viene eseguito lo script otterrà anche l'accesso a tutte le informazioni personali archiviate nei certificati. La prima volta che questo metodo viene chiamato da un particolare dominio, viene generata una finestra di dialogo in cui l'utente deve indicare se l'accesso ai certificati deve essere consentito. Gli archivi aperti da uno script Web forzano automaticamente il flag capicot \_ Store \_ Open \_ existing \_ .

 

Se *StoreLocation* è l' **\_ \_ \_ \_ archivio utente smart card di capicol**, *StoreName* viene ignorato. In questo caso, CAPICOM legge tutti i certificati da tutti i lettori disponibili che contengono una smart card.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|----------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Store**](store.md)
</dt> <dt>

[**Oggetti Cryptography**](cryptography-objects.md)
</dt> <dt>

[**Chiudi**](store-close.md)
</dt> </dl>

 

 
