---
description: Le proprietà dei nomi sono proprietà di certificati e richieste di certificati che rappresentano i dati relativi all'oggetto, ovvero il proprietario del certificato o l'utente per il quale viene richiesto un certificato.
ms.assetid: c32756f7-4431-410e-ab3a-c7b748a43829
title: Proprietà nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63c5978b3fe5ab7c6ead39840dfb1793372c5feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104233498"
---
# <a name="name-properties"></a>Proprietà nome

Le proprietà dei nomi sono proprietà di certificati e richieste di certificati che rappresentano i dati relativi all'oggetto, ovvero il proprietario del certificato o l'utente per il quale viene richiesto un certificato. Ogni proprietà Name è identificata da un nome di proprietà. Questi nomi non sono localizzabili; Tuttavia, le proprietà dei nomi corrispondono in genere a una colonna di database di Servizi certificati ed è possibile utilizzare lo snap-in MMC Autorità di certificazione, lo strumento da riga di comando "certutil-schema" o il metodo [**IEnumCERTVIEWCOLUMN:: GetDisplayName**](/windows/desktop/api/Certview/nf-certview-ienumcertviewcolumn-getdisplayname) per visualizzare le versioni localizzate dei nomi delle colonne di database.

Il nome della proprietà, ma non gli alias, potrebbe avere "Subject". come prefisso facoltativo. Ad esempio, per fare riferimento al nome comune del soggetto, è possibile usare "CommonName" o "Subject. CommonName".

Oltre al nome, ogni proprietà ha un certo numero di alias che i servizi certificati riconoscono come nomi alternativi per la proprietà. Si noti che gli [*identificatori di oggetto*](../secgloss/o-gly.md) (OID) sono alias accettabili, così come le **\_ \* *costanti szOID _. Queste costanti sono definizioni (in WinCrypt. h) che rappresentano il OID. Ad esempio, _* szOID \_ \_ nome comune** è definito come "2.5.4.3". Di conseguenza, è possibile usare le costanti **szOID \_ \** _ come alias al posto dei OID che rappresentano.



| Nome proprietà                 | Alias                                                                                                                                                        | Tipo di dati                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Subject. CommonName"          | "CommonName" "CN"<br/> "2.5.4.3"<br/> _ * szOID \_ \_ nome comune * *<br/>                                                                           | **Stringa** (max. 64 caratteri)  | Per i certificati utente, il nome completo della persona. Per i certificati del computer, il *percorso completo del nome host * **/**  utilizzato nelle ricerche Domain Name System (DNS), ad esempio *hostname ***.** _Esempio_* _. com_*).<br/>                                                                                                                                                                                                                                                                        |
| "Subject. Country"             | "Paese" "C"<br/> "2.5.4.6"<br/> **\_nome del paese szOID \_**<br/>                                                                              | **Stringa** (max 2 caratteri)    | Paese o area geografica dell'oggetto. Si tratta di un codice di paese/area geografica di due caratteri [*X. 500*](../secgloss/x-gly.md) , ad esempio per Stati Uniti o CA per il Canada.<br/> Molti di questi codici a due caratteri sono definiti nello standard ISO 3166. Inoltre, il codice delle impostazioni locali correnti è disponibile tramite una chiamata alla funzione di Windows [**GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) (specificando un *LCType* di impostazioni locali \_ SISO3166CTRYNAME).<br/> |
| "Subject. DeviceSerialNumber"  | "DeviceSerialNumber" "2.5.4.5"<br/> **\_numero di \_ serie del dispositivo szOID \_**<br/>                                                                         | **Stringa** (max 1024 caratteri) | Numero di serie del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject. DomainComponent"     | "DomainComponent" "DC"<br/> "0.9.2342.19200300.100.1.25"<br/> **\_componente di dominio szOID \_**<br/>                                              | **Stringa** (max 128 caratteri)  | Componente di un nome DNS (Domain Name System).                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject.EMail"               | "Posta elettronica" "E"<br/> "1.2.840.113549.1.9.1"<br/> **szOID \_ RSA \_ emailAddr**<br/>                                                                  | **Stringa** (max 128 caratteri)  | Indirizzo di posta elettronica (ad esempio, " someone@example.com ").                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject. GIVENAME"           | "Given" "G"<br/> "2.5.4.42"<br/> **\_nome szOID specificato \_**<br/>                                                                             | **Stringa** (max 16 caratteri)   | Nome dell'oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| "Subject.Initials"            | "Iniziali" "I"<br/> "2.5.4.43"<br/> **\_iniziali szOID**<br/>                                                                                 | **Stringa** (max 5 caratteri)    | Iniziali dell'oggetto (facoltativo).                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Soggetto. località"            | "Località" "L"<br/> "2.5.4.7"<br/> **\_nome località szOID \_**<br/>                                                                            | **Stringa** (max 128 caratteri)  | Nome della città dell'oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| "Subject. Organization"        | "Organizzazione" "org"<br/> O<br/> "2.5.4.10"<br/> **\_nome organizzazione \_ szOID**<br/>                                                  | **Stringa** (max 64 caratteri)   | Nome legale dell'organizzazione dell'oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject. unità organizzativa"             | "Unità organizzativa" "OrganizationUnit"<br/> OrganizationalUnit<br/> UNITÀ organizzativa<br/> 2.5.4.11<br/> **\_ \_ nome unità organizzativa \_ szOID**<br/> | **Stringa** (max 64 caratteri)   | Nome dell'organizzazione o del reparto secondario dell'oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject. state"               | "State" "ST"<br/> S<br/> "2.5.4.8"<br/> **\_nome di \_ \_ provincia o stato szOID \_**<br/>                                                    | **Stringa** (max 128 caratteri)  | Nome completo dello stato o della provincia del soggetto (ad esempio, California).                                                                                                                                                                                                                                                                                                                                                                                                                         |
| "Subject. StreetAddress"       | "StreetAddress" "via"<br/> "2.5.4.9"<br/> **szOID \_ via \_ Indirizzo**<br/>                                                                 | **Stringa** (al massimo 30 caratteri)   | Indirizzo della strada o casella di ordine dell'oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject. cognome"             | "Cognome" "SN"<br/> "2.5.4.4"<br/> **\_nome szOID sur \_**<br/>                                                                                 | **Stringa** (max 40 caratteri)   | Cognome dell'oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject. title"               | "Title" "T"<br/> "2.5.4.12"<br/> **\_titolo szOID**<br/>                                                                                       | **Stringa** (max 64 caratteri)   | Titolo del singolo utente che ha richiesto il certificato (facoltativo).                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject. UnstructuredAddress" | "UnstructuredAddress" "1.2.840.113549.1.9.8"<br/> **szOID \_ RSA \_ unstructAddr**<br/>                                                                | **Stringa** (max 1024 caratteri) | Indirizzo non strutturato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject. unstructuredname"    | "Unstructuredname" "1.2.840.113549.1.9.2"<br/> **szOID \_ RSA \_ unstructname**<br/>                                                                   | **Stringa** (max 1024 caratteri) | Nome non strutturato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

Le proprietà seguenti sono correlate all'oggetto, sebbene non siano proprietà nome. Il modulo criteri non può impostare direttamente queste proprietà.



| Proprietà                    | Tipo di dati                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Request. Distinguishname" | **Stringa** (max 8192 caratteri) | [*Nome distinto relativo*](../secgloss/r-gly.md) per la richiesta, una rappresentazione testuale dell'oggetto nella richiesta. Questa rappresentazione è costituita da proprietà nome, ad esempio "CN = nome, OU = UnitàOrg, C = US". L'applicazione Servizi certificati imposta questa proprietà prima di chiamare il modulo criteri chiamando [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) usando l'oggetto di RawRequest. |
| "Request. RawName"           | **Binario** (max 4096 byte) | [*BLOB*](../secgloss/b-gly.md) dell'oggetto binario [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN. 1) Estratto dalla richiesta. L'applicazione Servizi certificati imposta questa proprietà prima di chiamare il modulo criteri; il valore è determinato dall'oggetto RawRequest.                                                                                     |
| DistinguishedName         | **Stringa** (max 8192 caratteri) | Nome distinto relativo per il certificato, rappresentazione testuale dell'oggetto nel certificato. Questa rappresentazione è costituita da proprietà nome, ad esempio "CN = nome, OU = UnitàOrg, C = US". L'applicazione Servizi certificati imposta questa proprietà dopo aver chiamato il modulo criteri chiamando [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) usando RawName.                                                                                                               |
| "RawName"                   | **Binario** (max 4096 byte) | [*BLOB*](../secgloss/b-gly.md) dell'oggetto binario ASN. 1 usato per costruire il certificato. L'applicazione Servizi certificati imposta questa proprietà dopo la chiamata al modulo criteri. il valore è determinato dai valori di proprietà nome specifiche (Subject. CommonName e così via) come indicato da SubjectTemplate.                                                                                                                                        |



 

I componenti del [*nome distinto relativo*](../secgloss/r-gly.md) vengono visualizzati nella proprietà Distinguishname e l'ordine in cui vengono visualizzati sono controllati dal valore del registro di sistema "SubjectTemplate" contenuto nella chiave del registro di sistema seguente:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            CertSvc
               Configuration
                  CaName
```

Quando Servizi certificati analizza i nomi di [*attributo*](../secgloss/a-gly.md) , ignora gli spazi, i trattini (segni meno) e le maiuscole e minuscole. Ad esempio, "AttributeName1", "attribute name1" e "attribute-name1" sono tutti equivalenti. Per i valori di attributo, Servizi certificati ignora gli spazi vuoti iniziali e finali.

Tutte le proprietà precedenti eccetto Distinguishname, RawName e Subject. Country supportano la sintassi a più valori usando un carattere di nuova riga. Il separatore di nuova riga non può essere disabilitato o modificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà certificato](certificate-properties.md)
</dt> <dt>

[**ICertServerExit::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getcertificateproperty)
</dt> <dt>

[**ICertServerExit::GetRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverexit-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy::GetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getcertificateproperty)
</dt> <dt>

[**ICertServerPolicy::GetRequestProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-getrequestproperty)
</dt> <dt>

[**ICertServerPolicy::SetCertificateProperty**](/windows/desktop/api/Certif/nf-certif-icertserverpolicy-setcertificateproperty)
</dt> </dl>

 

 
