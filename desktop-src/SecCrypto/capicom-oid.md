---
description: Fornisce i nomi per gli identificatori di oggetto CAPICOM.
ms.assetid: 6c1eb2cc-84ac-4920-99ba-56ac8de4a851
title: CAPICOM_OID enumerazione (Capicom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_OID
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 8c008a77e11bd7803dfb09ed2e6ddf1f57ed8695f2de33655239eb73ac49a248
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879031"
---
# <a name="capicom_oid-enumeration"></a>Enumerazione \_ OID CAPICOM

**L'enumerazione \_ OID CAPICOM** fornisce i nomi per gli identificatori di oggetto CAPICOM.

Questa enumerazione viene utilizzata [**dall'OID. Proprietà Name.**](oid-name.md)

## <a name="members"></a>Membri



| Membro                                                        | Descrizione                                                                                                                                                                                                                                    | Valore |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **CAPICOM \_ OID \_ OTHER**                                       | L'oggetto non è uno dei tipi di oggetto CAPICOM predefiniti.<br/>                                                                                                                                                                       | 0     |
| **ESTENSIONE \_ IDENTIFICATORE DI CHIAVE \_ DELL'AUTORITÀ OID \_ \_ CAPICOM \_**       | L'oggetto è un'estensione del certificato che contiene l'identificatore di chiave pubblica dell'autorità di certificazione (CA).<br/>                                                                                                                  | 1     |
| **ESTENSIONE \_ ATTRIBUTI CHIAVE OID CAPICOM \_ \_ \_**                  | L'oggetto è un'estensione del certificato che contiene attributi facoltativi di una chiave pubblica.<br/>                                                                                                                                            | 2     |
| **ESTENSIONE \_ CAPICOM OID \_ CERT \_ POLICIES \_ 95 \_**               | L'oggetto è un'estensione del certificato che contiene Windows informazioni sui criteri del certificato 95.<br/>                                                                                                                                      | 3     |
| **ESTENSIONE \_ RESTRIZIONE UTILIZZO CHIAVE OID CAPICOM \_ \_ \_ \_**          | L'oggetto è un'estensione del certificato che contiene restrizioni sull'uso della chiave pubblica di un certificato.<br/>                                                                                                                          | 4     |
| **ESTENSIONE \_ MAPPING DEI CRITERI LEGACY CAPICOM OID \_ \_ \_ \_**         | L'oggetto è un'estensione del certificato che contiene informazioni sul mapping dei criteri legacy.<br/>                                                                                                                                              | 5     |
| **ESTENSIONE \_ DEL NOME ALTERNATIVO DEL SOGGETTO OID CAPICOM \_ \_ \_ \_**               | L'oggetto è un'estensione del certificato che contiene un nome alternativo per il soggetto del certificato.<br/>                                                                                                                         | 6     |
| **ESTENSIONE \_ DEL NOME ALTERNATIVO \_ DELL'AUTORITÀ EMITTENTE DELL'OID \_ \_ CAPICOM \_**                | L'oggetto è un'estensione del certificato che contiene un nome alternativo per l'autorità emittente del certificato.<br/>                                                                                                                          | 7     |
| **ESTENSIONE DEI \_ VINCOLI DI BASE OID CAPICOM \_ \_ \_**               | L'oggetto è un'estensione del certificato che indica se il soggetto certificato può fungere da CA, entità finale o entrambi. <br/>                                                                                                        | 8     |
| **ESTENSIONE \_ DELL'IDENTIFICATORE DELLA \_ \_ CHIAVE SOGGETTO \_ OID CAPICOM \_**         | L'oggetto è un'estensione del certificato che contiene l'identificatore di chiave del soggetto del certificato.<br/>                                                                                                                           | 9     |
| **ESTENSIONE \_ CAPICOM OID \_ KEY \_ USAGE \_**                       | L'oggetto è un'estensione del certificato che contiene informazioni sull'uso previsto della chiave pubblica di un certificato.<br/>                                                                                                               | 10    |
| **ESTENSIONE \_ DEL PERIODO DI UTILIZZO DI CAPICOM OID \_ \_ \_ \_ PRIVATEKEY**        | L'oggetto è un'estensione del certificato che contiene informazioni sul periodo di tempo durante il quale è possibile utilizzare la chiave privata di un certificato.<br/>                                                                                           | 11    |
| **CAPICOM \_ OID \_ SUBJECT \_ ALT \_ NAME2 \_ EXTENSION**              | L'oggetto è un'estensione del certificato che contiene un nome alternativo per il soggetto del certificato.<br/>                                                                                                                         | 12    |
| **CAPICOM \_ OID \_ ISSUER \_ ALT \_ NAME2 \_ EXTENSION**               | L'oggetto è un'estensione del certificato che contiene un nome alternativo per l'autorità emittente del certificato.<br/>                                                                                                                          | 13    |
| **ESTENSIONE \_ CAPICOM OID \_ BASIC \_ CONSTRAINTS2 \_**              | L'oggetto è un'estensione del certificato che indica se il soggetto certificato può fungere da CA, entità finale o entrambi. <br/>                                                                                                        | 14    |
| **ESTENSIONE DEI \_ VINCOLI DEI NOMI OID CAPICOM \_ \_ \_**                | L'oggetto è un'estensione del certificato che contiene informazioni sui certificati specificamente consentiti o esclusi dal trust.<br/>                                                                                          | 15    |
| **ESTENSIONE \_ CAPICOM OID \_ CRL \_ DIST \_ \_ POINTS**                | L'oggetto è un'estensione del certificato che contiene informazioni utilizzate per aggiornare l'elenco di revoche di certificati (CRL).<br/>                                                                                                               | 16    |
| **ESTENSIONE \_ CAPICOM OID \_ CERT \_ POLICIES \_**                   | L'oggetto è un'estensione del certificato che contiene un elenco dei criteri supportati dal certificato.<br/>                                                                                                                           | 17    |
| **ESTENSIONE \_ MAPPING DEI CRITERI OID CAPICOM \_ \_ \_**                 | L'oggetto è un'estensione del certificato che fornisce mapping tra criteri in domini diversi.<br/>                                                                                                                                 | 18    |
| **ESTENSIONE \_ CAPICOM OID \_ AUTHORITY \_ KEY \_ IDENTIFIER2 \_**      | L'oggetto è un'estensione del certificato che contiene l'identificatore di chiave pubblica della CA.<br/>                                                                                                                                            | 19    |
| **ESTENSIONE DEI \_ VINCOLI DEI CRITERI OID \_ \_ CAPICOM \_**              | L'oggetto è un'estensione del certificato che contiene i criteri stabiliti per accettare certificati come attendibili.<br/>                                                                                                                     | 20    |
| **ESTENSIONE \_ CAPICOM OID \_ ENHANCED \_ KEY \_ USAGE \_**             | L'oggetto è un'estensione del certificato che contiene informazioni avanzate sull'uso previsto della chiave pubblica di un certificato.<br/>                                                                                                      | 21    |
| **ESTENSIONE DEL \_ MODELLO DI CERTIFICATO CAPICOM OID \_ \_ \_**            | L'oggetto è un'estensione del certificato che contiene un modello di certificato.<br/>                                                                                                                                                         | 22    |
| **ESTENSIONE CRITERI \_ CERTIFICATO APPLICAZIONE CAPICOM OID \_ \_ \_ \_**      | L'oggetto è un'estensione del certificato che contiene i criteri dell'applicazione del certificato.<br/>                                                                                                                                      | 23    |
| **ESTENSIONE MAPPING DEI CRITERI DI APPLICAZIONE \_ CAPICOM OID \_ \_ \_ \_**    | L'oggetto è un'estensione del certificato che contiene mapping tra criteri dell'applicazione diversi.<br/>                                                                                                                                | 24    |
| **ESTENSIONE DEI VINCOLI \_ DEI CRITERI DI APPLICAZIONE CAPICOM OID \_ \_ \_ \_** | L'oggetto è un'estensione del certificato che contiene i vincoli dei criteri dell'applicazione del certificato.<br/>                                                                                                                          | 25    |
| **ESTENSIONE DI \_ ACCESSO ALLE INFORMAZIONI DELL'AUTORITÀ OID CAPICOM \_ \_ \_ \_**          | L'oggetto è un'estensione del certificato che indica come accedere alle informazioni e ai servizi della CA per l'autorità emittente del certificato.<br/>                                                                                                   | 26    |
| **\_EKU DI AUTENTICAZIONE DEL SERVER CAPICOM OID \_ \_ \_**                           | L'oggetto è un [**oggetto EKU**](eku.md) che specifica che il certificato può essere usato per autenticare un server.<br/>                                                                                                                | 100   |
| **\_EKU DI AUTENTICAZIONE CLIENT CAPICOM OID \_ \_ \_**                           | L'oggetto è un [**oggetto EKU**](eku.md) che specifica che il certificato può essere usato per autenticare un client.<br/>                                                                                                                | 101   |
| **EKU DI \_ FIRMA DEL CODICE OID \_ \_ \_ CAPICOM**                          | L'oggetto è un [**oggetto EKU**](eku.md) che specifica che il certificato può essere usato per creare una firma digitale.<br/>                                                                                                           | 102   |
| **\_EKU DI PROTEZIONE DELLA POSTA ELETTRONICA CAPICOM OID \_ \_ \_**                      | L'oggetto è un [**oggetto EKU**](eku.md) che specifica che il certificato può essere usato per la protezione della posta elettronica.<br/>                                                                                                                    | 103   |
| **CAPICOM \_ OID \_ IPSEC \_ END \_ SYSTEM \_ EKU**                     | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per un sistema finale IPsec.<br/>                                                                                                                 | 104   |
| **CAPICOM \_ OID \_ IPSEC \_ TUNNEL \_ EKU**                          | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per il tunneling IPsec.<br/>                                                                                                                     | 105   |
| **CAPICOM \_ OID \_ IPSEC \_ USER \_ EKU**                            | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per un utente IPsec.<br/>                                                                                                                       | 106   |
| **CAPICOM \_ OID \_ TIME \_ STAMPING \_ EKU**                         | L'oggetto è un [**oggetto EKU**](eku.md) che specifica che il certificato può essere usato per il timestamp.<br/>                                                                                                                       | 107   |
| **CAPICOM \_ OID \_ CTL \_ USAGE \_ SIGNING \_ EKU**                    | L'oggetto è un [**oggetto EKU**](eku.md) che specifica che il certificato può essere usato per firmare l'elenco di certificati attendibili (CTL).<br/>                                                                                                | 108   |
| **CAPICOM \_ OID \_ TIME \_ STAMP \_ SIGNING \_ EKU**                   | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per firmare un timestamp.<br/>                                                                                                                    | 109   |
| **CAPICOM \_ OID \_ SERVER \_ GATED \_ CRYPTO \_ EKU**                  | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per la crittografia con controllo del [*server*](../secgloss/s-gly.md) (SGC).<br/> | 110   |
| **CAPICOM \_ OID \_ ENCRYPTING \_ FILE \_ SYSTEM \_ EKU**               | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per [*Encrypting File System*](../secgloss/e-gly.md) (EFS).<br/>      | 111   |
| **CAPICOM \_ OID \_ EFS \_ RECOVERY \_ EKU**                          | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per il ripristino di EFS.<br/>                                                                                                                 | 112   |
| **CAPICOM \_ OID \_ WHQL \_ CRYPTO \_ EKU**                           | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per Windows crittografia WHQL (Hardware Quality Labs).<br/>                                                                                   | 113   |
| **CAPICOM \_ OID \_ NT5 \_ CRYPTO \_ EKU**                            | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per la crittografia Windows Server 2003 e Windows XP.<br/>                                                                                     | 114   |
| **CAPICOM \_ OID \_ OEM \_ WHQL \_ CRYPTO \_ EKU**                      | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per la crittografia WHQL OEM (Original Equipment Manufacturers).<br/>                                                                            | 115   |
| **CAPICOM \_ OID \_ EMBEDED \_ NT \_ CRYPTO \_ EKU**                    | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per Windows NT crittografia incorporata.<br/>                                                                                                    | 116   |
| **CAPICOM \_ OID \_ ROOT \_ LIST \_ SIGNER \_ EKU**                     | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per firmare un elenco radice.<br/>                                                                                                                     | 117   |
| **CAPICOM \_ OID \_ QUALIFIED \_ SUBORDINATION \_ EKU**               | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per la subordinazione qualificata.<br/>                                                                                                             | 118   |
| **CAPICOM \_ OID \_ KEY \_ RECOVERY \_ EKU**                          | L'oggetto è un [**oggetto EKU**](eku.md) che specifica che il certificato può essere usato per il recupero della chiave.<br/>                                                                                                                        | 119   |
| **CAPICOM \_ OID \_ DIGITAL \_ RIGHTS \_ EKU**                        | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per i diritti digitali.<br/>                                                                                                                      | 120   |
| **CAPICOM \_ OID \_ LICENSES \_ EKU**                               | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per le licenze.<br/>                                                                                                                            | 121   |
| **CAPICOM \_ OID \_ LICENSE \_ SERVER \_ EKU**                        | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per un server licenze.<br/>                                                                                                                    | 122   |
| **CAPICOM \_ OID \_ SMART \_ CARD \_ LOGON \_ EKU**                     | L'oggetto è [**un oggetto EKU**](eku.md) che specifica che il certificato può essere usato per l smart card accesso.<br/>                                                                                                                    | 123   |
| **CPS \_ QUALIFICATORE \_ CRITERI PKIX OID \_ \_ CAPICOM \_**                | L'oggetto è un'istruzione CPS (Certification Practice Statement) che può essere usata per il qualificatore dei criteri X.509 (PKIX) dell'infrastruttura a chiave pubblica.<br/>                                                                                            | 124   |
| **QUALIFICATORE \_ DEI CRITERI \_ CAPICOM OID PKIX \_ \_ \_ USERNOTICE**         | L'oggetto è un avviso utente che può essere usato per il qualificatore dei criteri X.509 (PKIX) dell'infrastruttura a chiave pubblica.<br/>                                                                                                                       | 125   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>Capicom.h</dt> </dl> |



 

 
