---
description: Le proprietà del nome sono proprietà dei certificati e delle richieste di certificato che rappresentano i dati relativi al soggetto, ad esempio il proprietario del certificato o la persona per cui viene richiesto un certificato.
ms.assetid: c32756f7-4431-410e-ab3a-c7b748a43829
title: Proprietà nome
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28765f0c278678ed5bdca9ef8547c1c6dc85ca7b6b343b229441b4b777eac688
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425311"
---
# <a name="name-properties"></a>Proprietà nome

Le proprietà del nome sono proprietà dei certificati e delle richieste di certificato che rappresentano i dati relativi al soggetto, ad esempio il proprietario del certificato o la persona per cui viene richiesto un certificato. Ogni proprietà name è identificata da un nome di proprietà. Questi nomi non sono localizzabili. Tuttavia, le proprietà name corrispondono in genere a una colonna di database di Servizi certificati ed è possibile usare lo snap-in MMC Autorità di certificazione, lo strumento da riga di comando 'certutil -schema' o il metodo [**IEnumCERTVIEWCOLUMN::GetDisplayName**](/windows/desktop/api/Certview/nf-certview-ienumcertviewcolumn-getdisplayname) per visualizzare le versioni localizzate dei nomi di colonna del database.

Il nome della proprietà (ma non gli alias) può avere "Subject". come prefisso facoltativo. Ad esempio, per fare riferimento al nome comune del soggetto, è possibile usare "CommonName" o "Subject.CommonName".

Oltre al nome, ogni proprietà ha un certo numero di alias che Servizi certificati riconosce come nomi alternativi per la proprietà. Si noti [*che gli*](../secgloss/o-gly.md) identificatori di oggetto (OID) sono alias accettabili, così come le **costanti szOID \_ \* *_. Queste costanti sono definizioni (in Wincrypt.h) che rappresentano gli OID. Ad esempio, _* szOID \_ COMMON \_ NAME** è definito come "2.5.4.3". Di conseguenza, è possibile usare **le costanti \_ \* szOID** come alias al posto degli OID che rappresentano.



| Nome proprietà                 | Alias                                                                                                                                                        | Tipo di dati                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|-------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Subject.CommonName"          | "CommonName" "CN"<br/> "2.5.4.3"<br/> **szOID \_ COMMON \_ NAME**<br/>                                                                           | **Stringa** (massimo 64 caratteri)  | Per i certificati utente, il nome completo della persona. Per i certificati computer, il percorso hostname* completo usato nelle ricerche DNS (Domain Name System), ad esempio ***/**  *HostName***.** _Esempio_* _.com_*).<br/>                                                                                                                                                                                                                                                                        |
| "Subject.Country"             | "Country" "C"<br/> "2.5.4.6"<br/> **szOID \_ COUNTRY \_ NAME**<br/>                                                                              | **Stringa** (massimo 2 caratteri)    | Paese o area geografica del soggetto. Si tratta di un codice paese/area geografica [*X.500*](../secgloss/x-gly.md) a due caratteri(ad esempio Stati Uniti per Stati Uniti o CA per Canada).<br/> Molti di questi codici a due caratteri sono definiti nello standard ISO 3166. Inoltre, il codice delle impostazioni locali correnti è disponibile tramite una chiamata alla funzione [**Windows GetLocaleInfo**](/windows/win32/api/winnls/nf-winnls-getlocaleinfoa) (specificando *un LCType* di \_ LOCALE SISO3166CTRYNAME).<br/> |
| "Subject.DeviceSerialNumber"  | "DeviceSerialNumber" "2.5.4.5"<br/> **szOID \_ DEVICE \_ SERIAL \_ NUMBER**<br/>                                                                         | **Stringa** (massimo 1024 caratteri) | Numero di serie del dispositivo.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject.DomainComponent"     | "DomainComponent" "DC"<br/> "0.9.2342.19200300.100.1.25"<br/> **SzOID \_ DOMAIN \_ COMPONENT**<br/>                                              | **Stringa** (massimo 128 caratteri)  | Componente di un Domain Name System (DNS).                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject.EMail"               | "EMail" "E"<br/> "1.2.840.113549.1.9.1"<br/> **szOID \_ RSA \_ emailAddr**<br/>                                                                  | **Stringa** (massimo 128 caratteri)  | Indirizzo di posta elettronica (ad esempio, " someone@example.com ").                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject.GivenName"           | "GivenName" "G"<br/> "2.5.4.42"<br/> **szOID \_ GIVEN \_ NAME**<br/>                                                                             | **Stringa** (massimo 16 caratteri)   | Nome dell'oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| "Subject.Initials"            | "Initials" "I"<br/> "2.5.4.43"<br/> **szOID \_ INITIALS**<br/>                                                                                 | **Stringa** (massimo 5 caratteri)    | Iniziali dell'oggetto (facoltativo).                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject.Locality"            | "Locality" "L"<br/> "2.5.4.7"<br/> **szOID \_ LOCALITY \_ NAME**<br/>                                                                            | **Stringa** (massimo 128 caratteri)  | Nome della città del soggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| "Subject.Organization"        | "Organizzazione" "Organizzazione"<br/> "O"<br/> "2.5.4.10"<br/> **szOID \_ ORGANIZATION \_ NAME**<br/>                                                  | **Stringa** (massimo 64 caratteri)   | Nome legale dell'organizzazione del soggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject.OrgUnit"             | "OrgUnit" "OrganizationUnit"<br/> "OrganizationalUnit"<br/> "OU"<br/> "2.5.4.11"<br/> **szOID \_ ORGANIZATIONAL \_ UNIT \_ NAME**<br/> | **Stringa** (massimo 64 caratteri)   | Nome della sotto-organizzazione o del reparto del soggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject.State"               | "State" "ST"<br/> "S"<br/> "2.5.4.8"<br/> **szOID \_ STATE OR PROVINCE \_ \_ \_ NAME**<br/>                                                    | **Stringa** (massimo 128 caratteri)  | Nome completo dello stato o della provincia del soggetto(ad esempio, California).                                                                                                                                                                                                                                                                                                                                                                                                                         |
| "Subject.StreetAddress"       | "StreetAddress" "Street"<br/> "2.5.4.9"<br/> **szOID \_ STREET \_ ADDRESS**<br/>                                                                 | **Stringa** (massimo 30 caratteri)   | Indirizzo dell'oggetto o casella postale.                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| "Subject.SurName"             | "SurName" "SN"<br/> "2.5.4.4"<br/> **szOID \_ SUR \_ NAME**<br/>                                                                                 | **Stringa** (massimo 40 caratteri)   | Cognome dell'oggetto.                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| "Subject.Title"               | "Title" "T"<br/> "2.5.4.12"<br/> **szOID \_ TITLE**<br/>                                                                                       | **Stringa** (massimo 64 caratteri)   | Titolo dell'utente che ha richiesto il certificato (facoltativo).                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| "Subject.UnstructuredAddress" | "UnstructuredAddress" "1.2.840.113549.1.9.8"<br/> **szOID \_ RSA \_ unstructAddr**<br/>                                                                | **Stringa** (massimo 1024 caratteri) | Indirizzo non strutturato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| "Subject.UnstructuredName"    | "UnstructuredName" "1.2.840.113549.1.9.2"<br/> **szOID \_ RSA \_ unstructName**<br/>                                                                   | **Stringa** (massimo 1024 caratteri) | Nome non strutturato.                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |



 

Le proprietà seguenti sono correlate all'oggetto, anche se non sono proprietà del nome. Il modulo criteri non può impostare direttamente queste proprietà.



| Proprietà                    | Tipo di dati                   | Descrizione                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------------------|-----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| "Request.DistinguishedName" | **Stringa** (massimo 8192 caratteri) | Nome [*distinto relativo per*](../secgloss/r-gly.md) la richiesta, una rappresentazione testuale dell'oggetto nella richiesta. Questa rappresentazione è costituita dalle proprietà del nome, ad esempio "CN=MyName, OU=MyOrgUnit, C=US". L'applicazione Servizi certificati imposta questa proprietà prima di chiamare il modulo criteri, chiamando [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) usando l'oggetto di RawRequest. |
| "Request.RawName"           | **Binario** (massimo 4096 byte) | BLOB del soggetto binario ASN.1 [](../secgloss/b-gly.md) [*(Abstract Syntax Notation One)*](../secgloss/a-gly.md) estratto dalla richiesta. L'applicazione Servizi certificati imposta questa proprietà prima di chiamare il modulo criteri. il relativo valore è determinato dall'oggetto rawRequest.                                                                                     |
| "DistinguishedName"         | **Stringa** (massimo 8192 caratteri) | Nome distinto relativo per il certificato, una rappresentazione testuale del soggetto nel certificato. Questa rappresentazione è costituita dalle proprietà del nome, ad esempio "CN=MyName, OU=MyOrgUnit, C=US". L'applicazione Servizi certificati imposta questa proprietà dopo aver chiamato il modulo criteri, chiamando [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra) usando RawName.                                                                                                               |
| "RawName"                   | **Binario** (massimo 4096 byte) | [*BLOB*](../secgloss/b-gly.md) del soggetto binario ASN.1 usato per costruire il certificato. L'applicazione Servizi certificati imposta questa proprietà dopo aver chiamato il modulo criteri. Il valore è determinato dai valori delle proprietà del nome specifiche (Subject.CommonName e così via) come indicato da SubjectTemplate.                                                                                                                                        |



 

I [*componenti relativi del nome*](../secgloss/r-gly.md) distinto visualizzati nella proprietà DistinguishedName e l'ordine in cui vengono visualizzati sono controllati dal valore del Registro di sistema "SubjectTemplate" contenuto nella chiave del Registro di sistema seguente:

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            CertSvc
               Configuration
                  CaName
```

Quando Servizi certificati analizza i nomi [*degli attributi,*](../secgloss/a-gly.md) ignora gli spazi, i trattini (segni meno) e la distinzione tra maiuscole e minuscole. Ad esempio, "AttributeName1", "Attribute Name1" e "Attribute-name1" sono tutti equivalenti. Per i valori di attributo, Servizi certificati ignora gli spazi vuoti iniziali e finali.

Tutte le proprietà precedenti, ad eccezione di DistinguishedName, RawName e Subject.Country, supportano la sintassi a più valori usando un carattere di nuova riga. Il separatore di nuova riga non può essere disabilitato o modificato.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Proprietà del certificato](certificate-properties.md)
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

 

 
