---
description: Restituisce un oggetto Certificates che contiene tutti i certificati che corrispondono ai criteri di ricerca specificati.
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: 'Metodo ICertificates2:: Find'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificates.Find
- ICertificates2.Find
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 9ea15891c33a0789e5b6746b55dfd0b0eb602afc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106332840"
---
# <a name="icertificates2find-method"></a>Metodo ICertificates2:: Find

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) nello spazio dei nomi [**System. Security. Cryptography. X509Certificates**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1) .\]

Il metodo **Find** restituisce un oggetto [**Certificates**](certificates.md) che contiene tutti i certificati che corrispondono ai criteri di ricerca specificati. Questo metodo è stato introdotto in capicol 2,0.

## <a name="syntax"></a>Sintassi


```VB
Certificates.Find( _
  ByVal FindType, _
  [ ByVal varCriteria ], _
  [ ByVal bFindValidOnly ] _
)
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FindType* \[ in\]
</dt> <dd>

Valore dell'enumerazione del [**\_ \_ \_ tipo Find del certificato CAPICOM**](capicom-certificate-find-type.md) che specifica il tipo di criterio di corrispondenza fornito nel parametro *varCriteria* . Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                                        | Significato                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <dt>**Il certificato CAPICOM \_ \_ trova \_ hash SHA1 \_**</dt> </dl>                              | Restituisce i certificati con un hash SHA1 che corrisponde all'hash SHA1 specificato nel parametro *varCriteria* .<br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <dt>**\_ \_ \_ nome oggetto trovato certificato capicot \_**</dt> </dl>                     | Restituisce i certificati il cui nome soggetto è esattamente o parzialmente corrispondente al nome del soggetto specificato nel parametro *varCriteria* . Questa chiamata Cerca solo il campo del nome del soggetto.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <dt>**\_ \_ \_ nome dell'autorità emittente trovare il certificato di CAPICOM \_**</dt> </dl>                        | Restituisce i certificati il cui nome dell'autorità di certificazione corrisponde esattamente o parzialmente al nome dell'autorità di certificazione specificato nel parametro *varCriteria* . Questa chiamata Cerca solo il campo del nome dell'autorità emittente.<br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <dt>**\_ \_ \_ nome radice trovato certificato capicol \_**</dt> </dl>                              | Restituisce i certificati il cui nome soggetto radice corrisponde esattamente o parzialmente al nome soggetto radice specificato nel parametro *varCriteria* . Questa chiamata crea una catena. Questa chiamata esegue la ricerca nel campo del nome del soggetto del certificato radice.<br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <dt>**\_nome del modello di \_ ricerca del certificato \_ CAPICOM \_**</dt> </dl>                  | Restituisce i certificati il cui nome modello corrisponde al nome del modello specificato nel parametro *varCriteria* .<br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <dt>**estensione per la \_ ricerca del certificato CApicol \_ \_**</dt> </dl>                               | Restituisce i certificati con un'estensione corrispondente all'estensione specificata nel parametro *varCriteria* .<br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <dt>**il certificato CAPICOM \_ \_ trova la \_ \_ proprietà estesa**</dt> </dl>      | Restituisce i certificati nell'archivio che contengono in modo esplicito una proprietà estesa con il valore specificato nel parametro *varCriteria* .<br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <dt>**\_ \_ criterio di ricerca \_ dell'applicazione \_ per il certificato capicol**</dt> </dl>   | Restituisce i certificati nell'archivio che dispongono di un'estensione per l'utilizzo delle chiavi avanzata, di un'estensione dei criteri dell'applicazione o di una proprietà estesa specificata nel parametro *varCriteria* .<br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <dt>**\_ \_ criterio di individuazione \_ \_ certificati di capicol**</dt> </dl>   | Restituisce i certificati che contengono l'OID del criterio nell'estensione dei criteri di certificato specificata nel parametro *varCriteria* .<br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <dt>**tempo di ricerca certificato capicol \_ \_ \_ \_ valido**</dt> </dl>                           | Restituisce i certificati il cui tempo è valido.<br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <dt>**tempo di individuazione del certificato capicol \_ \_ \_ \_ non \_ ancora \_ valido**</dt> </dl> | Restituisce i certificati il cui tempo non è ancora valido.<br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <dt>**tempo di individuazione certificato capicot \_ \_ \_ \_ scaduto**</dt> </dl>                     | Restituisce i certificati il cui tempo è scaduto.<br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <dt>**\_ \_ utilizzo chiave di ricerca del certificato CAPICOM \_ \_**</dt> </dl>                              | Restituisce i certificati contenenti gli utilizzi delle chiavi nell'estensione per l'utilizzo delle chiavi specificata nel parametro *varCriteria* . Se l'estensione per l'utilizzo delle chiavi non è presente, si presuppone che tutti gli utilizzi delle chiavi non siano disponibili.<br/>                           |



 

</dd> <dt>

*varCriteria* \[ in, facoltativo\]
</dt> <dd>

Variante che contiene i criteri di ricerca. Questi dati devono corrispondere al tipo di dati specificato nel parametro *FindType* . Se il valore del parametro *FindType* è l'ora di ricerca del certificato capicol \_ \_ \_ \_ valido, il tempo di ricerca del certificato capicol \_ non è \_ \_ \_ \_ ancora \_ valido o il tempo di ricerca del certificato capicol è \_ \_ \_ \_ scaduto e non si passa un valore in questo parametro, viene utilizzata l'ora corrente. Per esempi di ogni tipo di dati, vedere la sezione Osservazioni. Il valore predefinito è 0.

</dd> <dt>

*bFindValidOnly* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che indica se vengono restituiti solo certificati validi. Il valore predefinito è false; Ciò indica che vengono restituiti tutti i certificati che corrispondono ai criteri di ricerca.

Se true, la ricerca non restituisce i tipi di certificati seguenti:

-   Certificati il cui tempo è scaduto o non è ancora valido.
-   I certificati non sono concatenati correttamente.
-   Certificati con problemi di firma.
-   Certificati revocati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Oggetto [**Certificates**](certificates.md) che contiene i risultati della ricerca.

**Capicom 2,1:** L'oggetto [**certificati**](certificates.md) restituito contiene riferimenti ai certificati della raccolta in cui è stata eseguita la ricerca. Tutte le modifiche apportate ai certificati nell'oggetto **certificati** restituiti vengono riflesse in tale raccolta.

**CApicol 2,0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 e CApicol 2.0.0.3:** L'oggetto [**certificati**](certificates.md) restituito contiene copie dei certificati della raccolta in cui è stata eseguita la ricerca. Tutte le modifiche apportate ai certificati nell'oggetto **certificati** restituiti non vengono riflesse in tale raccolta.

## <a name="remarks"></a>Commenti

Negli esempi seguenti vengono illustrati i criteri di ricerca possibili per i diversi tipi di criteri di ricerca.



| Parametro *FindType*                              | parametro *varCriteria*                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| Il certificato CAPICOM \_ \_ trova \_ hash SHA1 \_            | 33F362434B577F844BB7226BE36F7D72EF9D9393                                                                                           |
| \_ \_ \_ nome oggetto trovato certificato capicot \_         | "NameOfPerson"                                                                                                                     |
| \_ \_ \_ nome dell'autorità emittente trovare il certificato di CAPICOM \_          | Verisign                                                                                                                         |
| \_ \_ \_ nome radice trovato certificato capicol \_            | "Autorità radice Microsoft"                                                                                                         |
| \_nome del modello di \_ ricerca del certificato \_ CAPICOM \_        | "AutoEnrollEFS"<br/> 1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052<br/>       |
| estensione per la \_ ricerca del certificato CApicol \_ \_             | "2.5.29.31"<br/> \_ \_ \_ estensione utilizzo chiave OID capicol \_<br/> "Elenco di distribuzione CRL"<br/>                           |
| il certificato CAPICOM \_ \_ trova la \_ \_ proprietà estesa    | CAPICOM \_ propid \_ chiave \_ prova \_ informazioni                                                                                                   |
| \_ \_ criterio di ricerca \_ dell'applicazione \_ per il certificato capicol   | 1.3.6.1.5.5.7.3.3<br/> 1.3.6.1.5.5.7.3.4<br/> \_ \_ \_ EKU autenticazione server OID CAPICOM \_<br/> "Firma codice"<br/> |
| \_ \_ criterio di individuazione \_ \_ certificati di capicol   | "1.3.6.1.5.5.7.3.4.3.5"<br/> "Garanzia aziendale elevata"<br/>                                                           |
| tempo di ricerca certificato capicol \_ \_ \_ \_ valido           | \#04/15/2002, 6:00 PM\#                                                                                                            |
| tempo di individuazione del certificato capicol \_ \_ \_ \_ non \_ ancora \_ valido | \#04/15/2002, 6:00 PM\#                                                                                                            |
| tempo di individuazione certificato capicot \_ \_ \_ \_ scaduto         | \#04/15/2002, 6:00 PM\#                                                                                                            |
| \_ \_ utilizzo chiave di ricerca del certificato CAPICOM \_ \_            | CAPICOM \_ \_ solo \_ \_ utilizzo chiavi                                                                                                |



 

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Certificati**](certificates.md)
</dt> <dt>

[**\_OID CAPICOM**](capicom-oid.md)
</dt> </dl>

 

 
