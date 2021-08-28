---
description: Restituisce un oggetto Certificates contenente tutti i certificati che corrispondono ai criteri di ricerca specificati.
ms.assetid: a2b8f4d4-dce3-467b-aaa0-a125056a1dd3
title: Metodo ICertificates2::Find
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
ms.openlocfilehash: 51e3d19348f0bff9cdbe0b4211d648a25025b2a3ab8feee9df6f804486265857
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120100991"
---
# <a name="icertificates2find-method"></a>Metodo ICertificates2::Find

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2Collection**](/dotnet/api/system.security.cryptography.x509certificates.x509certificate2collection?view=netcore-3.1) nello spazio dei nomi [**System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

Il **metodo Find** restituisce un oggetto [**Certificates**](certificates.md) che contiene tutti i certificati che corrispondono ai criteri di ricerca specificati. Questo metodo è stato introdotto in CAPICOM 2.0.

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

*FindType* \[ Pollici\]
</dt> <dd>

Valore [**dell'enumerazione CAPICOM \_ CERTIFICATE FIND \_ \_ TYPE**](capicom-certificate-find-type.md) che specifica il tipo di criteri di corrispondenza specificati nel *parametro varCriteria.* Nella tabella seguente sono illustrati i possibili valori.



| Valore                                                                                                                                                                                                                                                        | Significato                                                                                                                                                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CAPICOM_CERTIFICATE_FIND_SHA1_HASH"></span><span id="capicom_certificate_find_sha1_hash"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ SHA1 \_ HASH**</dt> </dl>                              | Restituisce i certificati con un hash SHA1 che corrisponde all'hash SHA1 specificato nel *parametro varCriteria.*<br/>                                                                                                                              |
| <span id="CAPICOM_CERTIFICATE_FIND_SUBJECT_NAME"></span><span id="capicom_certificate_find_subject_name"></span><dl> <dt>**CAPICOM \_ CERTIFICATE FIND SUBJECT NAME (TROVA NOME SOGGETTO DEL CERTIFICATO CAPICOM) \_ \_ \_**</dt> </dl>                     | Restituisce i certificati il cui nome soggetto corrisponde esattamente o parzialmente al nome del soggetto specificato nel *parametro varCriteria.* Questa chiamata esegue la ricerca solo nel campo del nome soggetto.<br/>                                                         |
| <span id="CAPICOM_CERTIFICATE_FIND_ISSUER_NAME"></span><span id="capicom_certificate_find_issuer_name"></span><dl> <dt>**CAPICOM \_ CERTIFICATE \_ FIND \_ ISSUER \_ NAME**</dt> </dl>                        | Restituisce i certificati il cui nome dell'autorità di certificazione corrisponde esattamente o parzialmente al nome dell'autorità emittente specificato nel *parametro varCriteria.* Questa chiamata cerca solo il campo del nome dell'autorità di emittente.<br/>                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_ROOT_NAME"></span><span id="capicom_certificate_find_root_name"></span><dl> <dt>**TROVARE IL \_ NOME RADICE \_ DEL \_ CERTIFICATO \_ CAPICOM**</dt> </dl>                              | Restituisce i certificati il cui nome soggetto radice corrisponde esattamente o parzialmente al nome del soggetto radice specificato nel *parametro varCriteria.* Questa chiamata crea una catena. Questa chiamata cerca il campo del nome soggetto del certificato radice.<br/> |
| <span id="CAPICOM_CERTIFICATE_FIND_TEMPLATE_NAME"></span><span id="capicom_certificate_find_template_name"></span><dl> <dt>**NOME MODELLO \_ DI RICERCA \_ CERTIFICATO \_ CAPICOM \_**</dt> </dl>                  | Restituisce i certificati il cui nome di modello corrisponde al nome del modello specificato nel *parametro varCriteria.*<br/>                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENSION"></span><span id="capicom_certificate_find_extension"></span><dl> <dt>**ESTENSIONE CAPICOM \_ CERTIFICATE \_ FIND \_**</dt> </dl>                               | Restituisce i certificati con un'estensione corrispondente all'estensione specificata nel *parametro varCriteria.*<br/>                                                                                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_EXTENDED_PROPERTY"></span><span id="capicom_certificate_find_extended_property"></span><dl> <dt>**PROPRIETÀ ESTESA \_ TROVA \_ CERTIFICATO \_ \_ CAPICOM**</dt> </dl>      | Restituisce i certificati nell'archivio che contengono in modo esplicito una proprietà estesa con il valore specificato nel *parametro varCriteria.*<br/>                                                                                                 |
| <span id="CAPICOM_CERTIFICATE_FIND_APPLICATION_POLICY"></span><span id="capicom_certificate_find_application_policy"></span><dl> <dt>**CRITERI \_ DELL'APPLICAZIONE CAPICOM CERTIFICATE \_ FIND \_ \_**</dt> </dl>   | Restituisce i certificati nell'archivio con un'estensione avanzata per l'utilizzo delle chiavi, un'estensione dei criteri di applicazione o una proprietà estesa specificata nel *parametro varCriteria.*<br/>                                                        |
| <span id="CAPICOM_CERTIFICATE_FIND_CERTIFICATE_POLICY"></span><span id="capicom_certificate_find_certificate_policy"></span><dl> <dt>**CRITERI DI \_ RICERCA CERTIFICATI CAPICOM \_ \_ \_**</dt> </dl>   | Restituisce i certificati che contengono l'OID dei criteri nell'estensione Criteri certificato specificata nel *parametro varCriteria.*<br/>                                                                                                          |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_VALID"></span><span id="capicom_certificate_find_time_valid"></span><dl> <dt>**ORA DI RICERCA CERTIFICATO CAPICOM \_ \_ \_ \_ VALIDA**</dt> </dl>                           | Restituisce i certificati la cui ora è valida.<br/>                                                                                                                                                                                               |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_NOT_YET_VALID"></span><span id="capicom_certificate_find_time_not_yet_valid"></span><dl> <dt>**ORA DI RICERCA DEL CERTIFICATO CAPICOM \_ \_ NON ANCORA \_ \_ \_ \_ VALIDA**</dt> </dl> | Restituisce i certificati la cui ora non è ancora valida.<br/>                                                                                                                                                                                       |
| <span id="CAPICOM_CERTIFICATE_FIND_TIME_EXPIRED"></span><span id="capicom_certificate_find_time_expired"></span><dl> <dt>**TEMPO DI RICERCA CERTIFICATO CAPICOM \_ \_ \_ \_ SCADUTO**</dt> </dl>                     | Restituisce i certificati il cui tempo è scaduto.<br/>                                                                                                                                                                                            |
| <span id="CAPICOM_CERTIFICATE_FIND_KEY_USAGE"></span><span id="capicom_certificate_find_key_usage"></span><dl> <dt>**INDIVIDUAZIONE \_ DELL'UTILIZZO \_ DELLA CHIAVE PER IL \_ CERTIFICATO \_ CAPICOM**</dt> </dl>                              | Restituisce i certificati contenenti gli utilizzi delle chiavi nell'estensione KeyUsage specificata nel *parametro varCriteria.* Se l'estensione KeyUsage non è presente, si presuppone che tutti gli utilizzi delle chiavi non siano disponibili.<br/>                           |



 

</dd> <dt>

*varCriteria* \[ in, facoltativo\]
</dt> <dd>

Variante che contiene i criteri di ricerca. Questi dati devono corrispondere al tipo di dati specificato nel *parametro FindType.* Se il valore del parametro *FindType* è CAPICOM \_ CERTIFICATE FIND TIME \_ \_ \_ VALID, CAPICOM CERTIFICATE FIND TIME NOT YET VALID o \_ \_ \_ \_ CAPICOM CERTIFICATE FIND TIME \_ \_ \_ \_ \_ \_ EXPIRED e non si passa un valore a questo parametro, si presuppone l'ora corrente. Per esempi di ogni tipo di dati, vedere Note. Il valore predefinito è 0.

</dd> <dt>

*bFindValidOnly* \[ in, facoltativo\]
</dt> <dd>

Valore booleano che indica se vengono restituiti solo certificati validi. Il valore predefinito è false. indica che vengono restituiti tutti i certificati che corrispondono ai criteri di ricerca.

Se true, la ricerca non restituirà i tipi di certificati seguenti:

-   Certificati il cui tempo è scaduto o non è ancora valido.
-   Certificati non concatenati correttamente.
-   Certificati con problemi di firma.
-   Certificati revocati.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

[**Oggetto Certificates**](certificates.md) che contiene i risultati della ricerca.

**CAPICOM 2.1:** [**L'oggetto**](certificates.md) Certificates restituito contiene riferimenti ai certificati nella raccolta in cui è stata eseguita la ricerca. Tutte le modifiche apportate ai certificati nell'oggetto **Certificates** restituito vengono riflesse in tale raccolta.

**CAPICOM 2.0, CAPICOM 2.0.0.1, CAPICOM 2.0.0.2 e CAPICOM 2.0.0.3:** [**L'oggetto**](certificates.md) Certificates restituito contiene copie dei certificati nella raccolta in cui è stata eseguita la ricerca. Tutte le modifiche apportate ai certificati nell'oggetto **Certificates** restituito non vengono riflesse in tale raccolta.

## <a name="remarks"></a>Commenti

Gli esempi seguenti illustrano i possibili criteri di ricerca per i diversi tipi di criteri di ricerca.



| *Parametro FindType*                              | *Parametro varCriteria*                                                                                                            |
|---------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| CAPICOM \_ CERTIFICATE \_ FIND \_ SHA1 \_ HASH            | 33F362434B577F844BB7226BE36F7D72EF9D9393                                                                                           |
| CAPICOM \_ CERTIFICATE FIND SUBJECT NAME (TROVA NOME SOGGETTO DEL CERTIFICATO CAPICOM) \_ \_ \_         | "NameOfPerson"                                                                                                                     |
| CAPICOM \_ CERTIFICATE \_ FIND \_ ISSUER \_ NAME          | "VeriSign"                                                                                                                         |
| TROVARE IL \_ NOME RADICE \_ DEL \_ CERTIFICATO \_ CAPICOM            | "Autorità radice Microsoft"                                                                                                         |
| NOME MODELLO \_ DI RICERCA \_ CERTIFICATO \_ CAPICOM \_        | "AutoEnrollEFS"<br/> 1.3.6.1.4.1.311.21.8.3692315854.1256661383.1690418588.4201632533.1741915387.2177932052<br/>       |
| ESTENSIONE CAPICOM \_ CERTIFICATE \_ FIND \_             | "2.5.29.31"<br/> ESTENSIONE \_ CAPICOM OID \_ KEY \_ USAGE \_<br/> "Elenco di distribuzione CRL"<br/>                           |
| PROPRIETÀ ESTESA \_ TROVA \_ CERTIFICATO \_ \_ CAPICOM    | INFORMAZIONI SUL \_ \_ \_ PROV DELLA CHIAVE PROPID CAPICOM \_                                                                                                   |
| CRITERI \_ DELL'APPLICAZIONE CAPICOM CERTIFICATE \_ FIND \_ \_   | "1.3.6.1.5.5.7.3.3"<br/> "1.3.6.1.5.5.7.3.4"<br/> \_EKU DI AUTENTICAZIONE DEL SERVER CAPICOM OID \_ \_ \_<br/> "Firma del codice"<br/> |
| CRITERI DI \_ RICERCA CERTIFICATI CAPICOM \_ \_ \_   | "1.3.6.1.5.5.7.3.4.3.5"<br/> "Garanzia elevata aziendale"<br/>                                                           |
| ORA DI RICERCA CERTIFICATO CAPICOM \_ \_ \_ \_ VALIDA           | \#15/04/2002, 18:00\#                                                                                                            |
| ORA DI RICERCA DEL CERTIFICATO CAPICOM \_ \_ NON ANCORA \_ \_ \_ \_ VALIDA | \#15/04/2002, 18:00\#                                                                                                            |
| TEMPO DI RICERCA CERTIFICATO CAPICOM \_ \_ \_ \_ SCADUTO         | \#15/04/2002, 18:00\#                                                                                                            |
| INDIVIDUAZIONE \_ DELL'UTILIZZO \_ DELLA CHIAVE PER IL \_ CERTIFICATO \_ CAPICOM            | CAPICOM \_ ENCIPHER \_ ONLY \_ KEY \_ USAGE                                                                                                |



 

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
</dt> <dt>

[**CAPICOM \_ OID**](capicom-oid.md)
</dt> </dl>

 

 
