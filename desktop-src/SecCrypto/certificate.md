---
description: Rappresenta un singolo certificato digitale.
ms.assetid: da95312b-cc9f-44f0-9517-0b28c5fcfb61
title: Oggetto Certificato
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Certificate
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: b6c19acc094426f99599b9e4aa9ea3968414c7de1d99377b2ce0bd2e8e3fde05
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119877991"
---
# <a name="certificate-object"></a>Oggetto Certificato

\[CAPICOM è un componente solo a 32 bit disponibile per l'uso nei sistemi operativi seguenti: Windows Server 2008, Windows Vista e Windows XP. Usare invece la [**classe X509Certificate2**](/previous-versions/windows/embedded/hh424017(v=msdn.10)) nello spazio dei [**nomi System.Security.Cryptography.X509Certificates.**](/dotnet/api/system.security.cryptography.x509certificates.publickey.-ctor?view=netcore-3.1)\]

**L'oggetto** Certificate rappresenta un [*singolo certificato digitale.*](../secgloss/d-gly.md)

**L'oggetto** Certificate espone le interfacce seguenti:

-   **ICertificate:** introdotto in CAPICOM 1.0.
-   **ICertificate2** : introdotto in CAPICOM 2.0.

## <a name="when-to-use"></a>Utilizzo

**L'oggetto** Certificate viene usato per eseguire le attività seguenti:

-   Caricare i dati del certificato, inclusa la chiave privata, da un file.
-   Ottenere informazioni dal certificato.
-   Restituisce vincoli di base, EKU, proprietà estese, estensioni, utilizzo della chiave, chiave pubblica e oggetti modello associati al certificato.
-   Determinare se il certificato è valido e verificare la disponibilità di accesso della chiave privata del soggetto del certificato.
-   Visualizzare il certificato.
-   Importare ed esportare il certificato.
-   Salvare il certificato in un file.
-   Recuperare o impostare le proprietà che descrivono il certificato.

## <a name="members"></a>Membri

**L'oggetto** Certificate ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

**L'oggetto Certificate** dispone di questi metodi.



| Metodo                                                       | Descrizione                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Proprietà BasicConstraints**](certificate-basicconstraints.md)     | Restituisce un [**oggetto BasicConstraints**](basicconstraints.md) che rappresenta l'estensione dei vincoli di base del certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**.                                                   |
| [**Visualizzazione**](certificate-display.md)                       | Visualizza un certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**.                                                                                                                                                             |
| [**Esportazione**](certificate-export.md)                         | Copia un certificato in una stringa codificata. La stringa codificata può essere scritta in un file o importata in un nuovo **oggetto** Certificate.<br/> Ereditato da **CertificateICertificate2ICertificate**.                                               |
| [**ExtendedKeyUsage**](certificate-extendedkeyusage.md)     | Restituisce un [**oggetto ExtendedKeyUsage**](extendedkeyusage.md) che indica gli utilizzi validi della chiave estesa del certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**.                                                       |
| [**ExtendedProperties**](certificate-extendedproperties.md) | Restituisce una raccolta delle proprietà estese del certificato.<br/> Ereditato da **CertificateICertificate2**                                                                                                                             |
| [**Estensioni**](certificate-extensions.md)                 | Restituisce una raccolta delle estensioni associate al certificato.<br/> Ereditato da **CertificateICertificate2**                                                                                                                         |
| [**GetInfo**](certificate-getinfo.md)                       | Recupera informazioni dal certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**.                                                                                                                                         |
| [**HasPrivateKey**](certificate-hasprivatekey.md)           | Determina se al certificato è [*associata una*](../secgloss/p-gly.md) chiave privata.<br/> Ereditato da **CertificateICertificate2ICertificate**.                                    |
| [**Importa**](certificate-import.md)                         | Importa un certificato codificato in precedenza da una stringa **nell'oggetto** Certificate.<br/> Ereditato da **CertificateICertificate2ICertificate**.                                                                                             |
| [**isValid**](certificate-isvalid.md)                       | Compila una catena di verifica del certificato per un certificato e restituisce un [**oggetto CertificateStatus**](certificatestatus.md) che contiene lo stato di validità del certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**. |
| [**KeyUsage**](certificate-keyusage.md)                     | Restituisce un [**oggetto KeyUsage**](keyusage.md) che indica l'utilizzo valido della chiave del certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**.                                                                                |
| [**Caricamento**](certificate-load.md)                             | Importa un certificato da un file.<br/> Ereditato da **CertificateICertificate2**                                                                                                                                                              |
| [**Publickey**](certificate-publickey.md)                   | Restituisce un [**oggetto PublicKey.**](publickey.md)<br/> Ereditato da **CertificateICertificate2**                                                                                                                                                |
| [**Salva**](certificate-save.md)                             | Salva il certificato in un file.<br/> Ereditato da **CertificateICertificate2**                                                                                                                                                                |
| [**Modello**](certificate-template.md)                     | Restituisce il modello associato al certificato.<br/> Ereditato da **CertificateICertificate2**                                                                                                                                           |



 

### <a name="properties"></a>Proprietà

**L'oggetto Certificate** ha queste proprietà.



| Proprietà                                                      | Tipo di accesso           | Descrizione                                                                                                                                          |
|:--------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Archiviato**](certificate-archived.md)<br/>           | Lettura/Scrittura<br/> | Imposta o recupera un valore booleano che indica se il certificato è archiviato.<br/> Ereditato da **CertificateICertificate2**       |
| [**IssuerName**](certificate-issuername.md)<br/>       | Sola lettura<br/>  | Recupera una stringa che contiene il nome dell'autorità emittente del certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**.            |
| [**PrivateKey**](certificate-privatekey.md)<br/>       | Lettura/Scrittura<br/> | Imposta o recupera la chiave privata associata al certificato.<br/> Ereditato da **CertificateICertificate2**                          |
| [**Serialnumber**](certificate-serialnumber.md)<br/>   | Sola lettura<br/>  | Recupera una stringa che contiene il numero di serie del certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**.                 |
| [**SubjectName**](certificate-subjectname.md)<br/>     | Sola lettura<br/>  | Recupera una stringa che contiene il nome del soggetto del certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**.           |
| [**Identificazione personale**](certificate-thumbprint.md)<br/>       | Sola lettura<br/>  | Recupera una stringa esadecimale che contiene l'hash SHA-1 del certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**. |
| [**ValidFromDate**](certificate-validfromdate.md)<br/> | Sola lettura<br/>  | Recupera la data di inizio per la validità del certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**.               |
| [**ValidToDate**](certificate-validtodate.md)<br/>     | Sola lettura<br/>  | Recupera la data di fine per la validità del certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**.                  |
| [**Versione**](certificate-version.md)<br/>             | Sola lettura<br/>  | Recupera il numero di versione del certificato.<br/> Ereditato da **CertificateICertificate2ICertificate**.                                |



 

## <a name="remarks"></a>Commenti

**L'oggetto** Certificato può essere creato ed è sicuro per lo scripting. Il ProgID per **l'oggetto Certificate** è "CAPICOM. Certificate.2".

**CAPICOM 1. *x:*** il ProgID per **l'oggetto Certificate** è "CAPICOM. Certificate.1".

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|----------------------------------|----------------------------------------------------------------------------------------|
| Fine del supporto client<br/> | Windows Vista<br/>                                                               |
| Fine del supporto server<br/> | Windows Server 2008<br/>                                                         |
| Componente ridistribuibile<br/>       | CAPICOM 2.0 o versioni successive in Windows Server 2003 e Windows XP<br/>                  |
| DLL<br/>                   | <dl> <dt>Capicom.dll</dt> </dl> |



 

 
