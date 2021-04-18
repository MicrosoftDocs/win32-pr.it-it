---
description: Fornisce i nomi per gli identificatori di oggetto CAPICOM.
ms.assetid: 6c1eb2cc-84ac-4920-99ba-56ac8de4a851
title: Enumerazione CAPICOM_OID (CAPICOM. h)
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
ms.openlocfilehash: 4cedd7c039212b7bae3e681d7e0d594d3e1b8de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/22/2021
ms.locfileid: "106326980"
---
# <a name="capicom_oid-enumeration"></a>\_Enumerazione OID CAPICOM

L'enumerazione **\_ OID di CAPICOM** fornisce i nomi per gli identificatori di oggetto CAPICOM.

Questa enumerazione viene utilizzata dall' [**OID. Proprietà Name**](oid-name.md) .

## <a name="members"></a>Membri



| Membro                                                        | Descrizione                                                                                                                                                                                                                                    | Valore |
|---------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------|
| **sqlpicot \_ OID \_ altro**                                       | L'oggetto non è uno dei tipi di oggetto CAPICOM predefiniti.<br/>                                                                                                                                                                       | 0     |
| **\_estensione dell'identificatore di \_ \_ chiave dell' \_ autorità \_ di certificazione di CAPICOM**       | L'oggetto è un'estensione del certificato che contiene l'identificatore di chiave pubblica dell'autorità di certificazione (CA).<br/>                                                                                                                  | 1     |
| **\_ \_ estensione degli attributi chiave OID \_ di \_ CAPICOM**                  | L'oggetto è un'estensione del certificato che contiene attributi facoltativi di una chiave pubblica.<br/>                                                                                                                                            | 2     |
| **Estensione di capicol \_ OID \_ CERT \_ Policies \_ 95 \_**               | L'oggetto è un'estensione di certificato che contiene informazioni sui criteri dei certificati di Windows 95.<br/>                                                                                                                                      | 3     |
| **\_estensione di limitazione all' \_ utilizzo della chiave OID \_ \_ di capicol \_**          | L'oggetto è un'estensione di certificato che contiene restrizioni sull'utilizzo della chiave pubblica di un certificato.<br/>                                                                                                                          | 4     |
| **estensione per i \_ \_ mapping dei \_ criteri \_ legacy \_ di capicol OID**         | L'oggetto è un'estensione di certificato che contiene informazioni legacy sul mapping dei criteri.<br/>                                                                                                                                              | 5     |
| **\_ \_ \_ estensione del nome Alt del soggetto capicol OID \_ \_**               | L'oggetto è un'estensione del certificato che contiene un nome alternativo per l'oggetto del certificato.<br/>                                                                                                                         | 6     |
| **\_ \_ \_ estensione del nome alternativo dell'emittente dell' \_ OID di capicol \_**                | L'oggetto è un'estensione di certificato che contiene un nome alternativo per l'emittente del certificato.<br/>                                                                                                                          | 7     |
| **\_estensione di vincoli di \_ base dell'OID \_ capicol \_**               | L'oggetto è un'estensione del certificato che indica se l'oggetto certificato può fungere da autorità di certificazione, entità finale o entrambi. <br/>                                                                                                        | 8     |
| **\_estensione dell'identificatore di \_ \_ chiave del \_ soggetto \_ di capicol OID**         | L'oggetto è un'estensione del certificato che contiene l'identificatore di chiave dell'oggetto del certificato.<br/>                                                                                                                           | 9     |
| **\_ \_ \_ estensione utilizzo chiave OID capicol \_**                       | L'oggetto è un'estensione del certificato che contiene informazioni sull'utilizzo previsto della chiave pubblica di un certificato.<br/>                                                                                                               | 10    |
| **\_estensione del periodo di \_ \_ utilizzo PRIVATEKEY \_ di capicol OID \_**        | L'oggetto è un'estensione del certificato che contiene informazioni sul periodo di tempo durante il quale è utilizzabile la chiave privata di un certificato.<br/>                                                                                           | 11    |
| **\_ \_ Estensione dell'oggetto \_ \_ name2 \_ di CAPICOM**              | L'oggetto è un'estensione del certificato che contiene un nome alternativo per l'oggetto del certificato.<br/>                                                                                                                         | 12    |
| **\_ \_ Estensione dell'autorità emittente \_ ALT \_ name2 \_ di capicol**               | L'oggetto è un'estensione di certificato che contiene un nome alternativo per l'emittente del certificato.<br/>                                                                                                                          | 13    |
| **\_ \_ Estensione CONSTRAINTS2 di base OID \_ capicol \_**              | L'oggetto è un'estensione del certificato che indica se l'oggetto certificato può fungere da autorità di certificazione, entità finale o entrambi. <br/>                                                                                                        | 14    |
| **\_ \_ estensione di vincoli nome OID \_ capicol \_**                | L'oggetto è un'estensione del certificato che contiene informazioni sui certificati specificamente consentiti o esclusi dal trust.<br/>                                                                                          | 15    |
| **estensione per i punti di Dist di sqlpicol \_ OID \_ CRL \_ \_ \_**                | L'oggetto è un'estensione del certificato che contiene le informazioni utilizzate per aggiornare l'elenco di revoche di certificati (CRL).<br/>                                                                                                               | 16    |
| **estensione di criteri di certificato capicol \_ OID \_ \_ \_**                   | L'oggetto è un'estensione del certificato che contiene un elenco dei criteri supportati dal certificato.<br/>                                                                                                                           | 17    |
| **\_ \_ estensione mapping dei criteri OID \_ di CAPICOM \_**                 | L'oggetto è un'estensione di certificato che fornisce i mapping tra i criteri in domini diversi.<br/>                                                                                                                                 | 18    |
| **\_ \_ \_ Estensione IDENTIFIER2 della chiave dell'autorità \_ di certificazione di CAPICOM \_**      | L'oggetto è un'estensione del certificato che contiene l'identificatore di chiave pubblica dell'autorità di certificazione.<br/>                                                                                                                                            | 19    |
| **\_estensione dei vincoli dei \_ criteri \_ OID \_ di CAPICOM**              | L'oggetto è un'estensione di certificato che contiene i criteri stabiliti per accettare certificati come attendibili.<br/>                                                                                                                     | 20    |
| **\_ \_ \_ \_ estensione utilizzo chiavi avanzato \_ di capicol OID**             | L'oggetto è un'estensione del certificato che contiene informazioni avanzate sull'utilizzo previsto della chiave pubblica di un certificato.<br/>                                                                                                      | 21    |
| **estensione del modello di certificato capicol \_ OID \_ \_ \_**            | L'oggetto è un'estensione del certificato che contiene un modello di certificato.<br/>                                                                                                                                                         | 22    |
| **estensione per i \_ \_ criteri del \_ certificato dell'applicazione \_ di capicol OID \_**      | L'oggetto è un'estensione del certificato che contiene i criteri dell'applicazione del certificato.<br/>                                                                                                                                      | 23    |
| **\_estensione dei mapping dei \_ criteri dell'applicazione \_ \_ \_ sqlpicol OID**    | L'oggetto è un'estensione di certificato che contiene i mapping tra i diversi criteri di applicazione.<br/>                                                                                                                                | 24    |
| **\_estensione dei vincoli dei \_ \_ criteri dell' \_ applicazione \_ capicol OID** | L'oggetto è un'estensione del certificato che contiene i vincoli dei criteri dell'applicazione del certificato.<br/>                                                                                                                          | 25    |
| **\_ \_ \_ estensione di \_ accesso alle informazioni sull'autorità OID di CAPICOM \_**          | L'oggetto è un'estensione del certificato che indica come accedere alle informazioni e ai servizi della CA per l'emittente del certificato.<br/>                                                                                                   | 26    |
| **\_ \_ \_ EKU autenticazione server OID CAPICOM \_**                           | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per autenticare un server.<br/>                                                                                                                | 100   |
| **\_ \_ EKU di autenticazione client OID \_ di \_ CAPICOM**                           | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per autenticare un client.<br/>                                                                                                                | 101   |
| **\_identificatore EKU per la \_ firma del codice di \_ CAPICOM \_**                          | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per creare una firma digitale.<br/>                                                                                                           | 102   |
| **ID del \_ messaggio di \_ posta elettronica di \_ protezione dell'OID di CAPICOM \_**                      | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per la protezione della posta elettronica.<br/>                                                                                                                    | 103   |
| **\_ \_ \_ EKU del sistema finale IPSec \_ \_ OID**                     | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per un sistema finale IPSec.<br/>                                                                                                                 | 104   |
| **\_ \_ \_ EKU del tunnel IPSec \_ del capicol OID**                          | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per il tunneling IPsec.<br/>                                                                                                                     | 105   |
| **\_ \_ \_ EKU utente IPSec \_ di capicol OID**                            | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per un utente IPSec.<br/>                                                                                                                       | 106   |
| **\_identificatore \_ \_ EKU timestamp timestamp \_**                         | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per il timestamp.<br/>                                                                                                                       | 107   |
| **\_ \_ \_ EKU di \_ firma utilizzo \_ EKU di capicol OID**                    | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per firmare l'elenco di certificati attendibili (CTL).<br/>                                                                                                | 108   |
| **\_identificatore EKU per la \_ \_ firma del \_ timestamp \_ di CAPICOM**                   | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per firmare un timestamp.<br/>                                                                                                                    | 109   |
| **\_ \_ \_ EKU di \_ crittografia gestito server \_ di CAPICOM**                  | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per la [*crittografia gestita dal server*](../secgloss/s-gly.md) (SGC).<br/> | 110   |
| **ID del \_ \_ file System per la crittografia del \_ file \_ System \_ EKU**               | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per il [*Encrypting File System*](../secgloss/e-gly.md) (EFS).<br/>      | 111   |
| **EKU per il recupero di sqlpicol \_ OID \_ EFS \_ \_**                          | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per il ripristino dell'EFS.<br/>                                                                                                                 | 112   |
| **ID del certificato di crittografia per l'ID del certificato \_ \_ WHQL \_ \_**                           | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per la crittografia Windows Hardware Quality Labs (WHQL).<br/>                                                                                   | 113   |
| **L'EKU di \_ \_ crittografia NT5 \_ OID \_**                            | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per la crittografia di windows Server 2003 e Windows XP.<br/>                                                                                     | 114   |
| **ID della \_ crittografia WHQL di CAPICOM \_ OEM \_ WHQL \_ \_**                      | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per la crittografia WHQL di Original Equipment Manufacturer (OEM).<br/>                                                                            | 115   |
| **ID dell' \_ EKU di \_ \_ crittografia NT incorporato \_ dell'OID di CAPICOM \_**                    | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per la crittografia Windows NT Embedded.<br/>                                                                                                    | 116   |
| **\_ \_ \_ EKU del \_ firmatario dell'elenco radice \_ di CAPICOM**                     | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per firmare un elenco radice.<br/>                                                                                                                     | 117   |
| **\_ \_ \_ EKU di subordinazione dell'OID di CAPICOM qualificato \_**               | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per la subordinazione qualificata.<br/>                                                                                                             | 118   |
| **\_ \_ EKU di recupero chiavi OID \_ di \_ CAPICOM**                          | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per il recupero della chiave.<br/>                                                                                                                        | 119   |
| **\_ \_ \_ EKU diritti digitali OID \_**                        | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per i diritti digitali.<br/>                                                                                                                      | 120   |
| **\_ \_ EKU licenze OID \_**                               | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per le licenze.<br/>                                                                                                                            | 121   |
| **\_ \_ \_ EKU del server licenze \_ sqlpicot OID**                        | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per un server licenze.<br/>                                                                                                                    | 122   |
| **\_EKU di accesso con \_ Smart \_ card \_ di \_ capicol OID**                     | L'oggetto è un oggetto [**EKU**](eku.md) che specifica che il certificato può essere utilizzato per l'accesso con smart card.<br/>                                                                                                                    | 123   |
| **\_ \_ PKIX del \_ qualificatore di criteri \_ \_ di CAPICOM, CPS**                | L'oggetto è un CPS (Certification Practice Statement) che può essere usato per il qualificatore di criteri X. 509 (PKIX) dell'infrastruttura a chiave pubblica.<br/>                                                                                            | 124   |
| **\_ \_ PKIX \_ qualificatore del criterio di \_ capicol OID \_ USERNOTICE**         | L'oggetto è una nota utente che può essere utilizzata per il qualificatore di criteri PKIX (Public Key Infrastructure X. 509).<br/>                                                                                                                       | 125   |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------|--------------------------------------------------------------------------------------|
| Componente ridistribuibile<br/> | CAPICOM 2,0 o versioni successive in Windows Server 2003 e Windows XP<br/>                |
| Intestazione<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
