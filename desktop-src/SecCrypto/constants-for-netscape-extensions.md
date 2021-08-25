---
description: Usato con operazioni di codifica e decodifica.
ms.assetid: 713c95ae-e5d0-416c-ba0c-4b5399aa8a33
title: Costanti per le estensioni Netscape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 315d27039bf29220f1a7cdfba82baa1350da084025f436aa1b4746d7e92f5c2c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119876751"
---
# <a name="constants-for-netscape-extensions"></a>Costanti per le estensioni Netscape

Le estensioni Netscape seguenti vengono usate con operazioni di codifica e decodifica. Le costanti predefinite di Netscape e le stringhe degli identificatori di oggetto non vengono usate direttamente con le funzioni di codifica o decodifica, [**CryptEncodeObject,**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobject) [**CryptEncodeObjectEx,**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) [**CryptSignAndEncodeCertificate,**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate) [**CryptDecodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobject)o [**CryptDecodeObjectEx.**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) Queste estensioni richiedono invece l'uso di *lpszStructType* illustrato.

Per altri dettagli che si applicano ad alcune estensioni di Netscape, vedere le osservazioni seguenti nella tabella.



| Identificatori di oggetto dell'estensione del certificato Netscape                      | *lpszStructType*                                           | *pvStructInfo corrispondente*                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| szOID \_ NETSCAPE \_ BASE \_ URL"2.16.840.1.113730.1.2"<br/>           | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il **membro dwValueType** è impostato su CERT \_ RDN \_ IA5 \_ STRING. Il **membro** **pbData** del membro Value punta a una stringa IA5 aggiunta all'inizio di tutti gli indirizzi URL relativi in un \_ certificato. Questa estensione può essere considerata un'ottimizzazione per ridurre le dimensioni delle estensioni URL.                                                                                                       |
| szOID \_ NETSCAPE \_ CA POLICY \_ \_ URL"2.16.840.1.113730.1.8"<br/>     | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il **membro dwValueType** è impostato su CERT \_ RDN \_ IA5 \_ STRING. Il **membro** **pbData** del membro Value punta a una stringa IA5, l'URL relativo o assoluto della pagina Web che descrive i criteri con cui è stato \_ rilasciato il certificato.                                                                                                                                                            |
| szOID \_ NETSCAPE \_ CA \_ REVOCATION \_ URL"2.16.840.1.113730.1.4"<br/> | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il **membro dwValueType** è impostato su CERT \_ RDN \_ IA5 \_ STRING. Il  membro **pbData** del membro Value punta a una stringa IA5 che rappresenta l'URL relativo o assoluto usato per controllare lo stato di revoca dei certificati firmati dall'autorità di certificazione a cui appartiene il certificato \_ [](../secgloss/c-gly.md) corrente. |
| szOID \_ NETSCAPE \_ CERT \_ RENEWAL \_ URL"2.16.840.1.113730.1.7"<br/>  | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il **membro dwValueType** è impostato su CERT \_ RDN \_ IA5 \_ STRING. Il **membro** **pbData** del membro Value punta a una stringa IA5 che rappresenta l'URL relativo o assoluto di un modulo di rinnovo del \_ certificato.                                                                                                                                                                                                     |
| szOID \_ NETSCAPE \_ CERT \_ SEQUENCE"2.16.840.1.113730.2.5"<br/>      | SEQUENZA DI INFORMAZIONI SUL CONTENUTO PKCS \_ \_ DI \_ \_ \_ QUALSIASI                     | [**SEQUENZA DI \_ INFORMAZIONI SUL \_ CONTENUTO \_ CRYPT DI \_ \_ QUALSIASI**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)                                                                                                                                                                                                                                                                                                                                                                |
| szOID \_ NETSCAPE \_ CERT \_ TYPE"2.16.840.1.113730.1.1"<br/>          | BIT X509 \_                                                 | [**BLOB DI BIT CRYPT \_ \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_bit_blob)                                                                                                                                                                                                                                                                                                                                                                                                           |
| szOID \_ NETSCAPE \_ COMMENT"2.16.840.1.113730.1.13"<br/>            | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il **membro dwValueType** è impostato su CERT \_ RDN \_ IA5 \_ STRING. Il **membro** **pbData del** membro Value punta a una stringa IA5 che rappresenta un commento da visualizzare quando viene visualizzato il \_ certificato.                                                                                                                                                                                                         |
| szOID \_ NETSCAPE \_ REVOCATION \_ URL"2.16.840.1.113730.1.3"<br/>     | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il **membro dwValueType** è impostato su CERT \_ RDN \_ IA5 \_ STRING. Il **membro** **pbData** del membro Value punta a una stringa IA5 che è un URL relativo o assoluto usato per controllare lo stato di revoca \_ del certificato.                                                                                                                                                                              |
| szOID \_ NETSCAPE \_ SSL SERVER \_ \_ NAME"2.16.840.1.113730.1.12"<br/>  | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il **membro dwValueType** è impostato su CERT \_ RDN \_ IA5 \_ STRING. Il **membro** **pbData** del membro Value punta a una stringa IA5 che è un'espressione della shell usata per trovare la corrispondenza con il nome host del \_ server SSL usando questo certificato.                                                                                                                                                                       |



 

Per tutte le funzioni di codifica che usano X509 ANY STRING o \_ \_ X5O9 \_ UNICODE ANY STRING \_ \_ **lpszStructType,** viene usato X509 ANY STRING se il formato della stringa nel membro \_ pbData \_   [](../secgloss/a-gly.md) \_ \_ \_ del membro Value è ASCII e X509 UNICODE ANY STRING viene usato se il formato della stringa è UNICODE. Nel caso Unicode, la stringa deve essere convertita in una stringa IA5 prima della codifica impostando il membro \_ **dwValueType** della struttura [**CERT \_ NAME \_ VALUE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value) su CERT \_ RDN \_ IA5 \_ STRING.

Per le funzioni di decodifica, l'utente seleziona il formato della stringa di output. Usare X509 ANY STRING se il formato della stringa desiderato è \_ \_ ASCII e X509 UNICODE ANY STRING se il formato di stringa desiderato \_ è \_ \_ Unicode.

Per l'estensione szOID NETSCAPE CERT RENEWAL URL, la struttura dei dati contiene un URL relativo o assoluto \_ che punta a un modulo di rinnovo del \_ \_ \_ certificato. Il modulo di rinnovo sarà accessibile con un metodo HTTP GET usando un URL che rappresenta la concatenazione di renewal-URL e certificate-serial-number. Il numero di serie del certificato viene codificato come stringa di cifre esadecimali ASCII. Ad esempio, se netscape-base-url è https://*URL* dell'autorità di certificazione /, netscape-cert-renewal-url è cgi-bin/check-renew.cgi?, e il numero di serie del certificato è 173420, l'URL risultante sarà: https://*certification authority URL*/cgi-bin/check-renew.cgi?02a56c. Il documento restituito deve essere un modulo HTML che consentirà all'utente di richiedere il rinnovo del certificato.

Per l'estensione szOID \_ NETSCAPE CERT SEQUENCE con \_ CODIFICA \_ ASN X509, il certificato viene codificato come struttura \_ PKCS CONTENT \_ INFO \_ che \_ esegue il wrapping di una sequenza di ANY. Il valore del membro **contentType** è **pszObjId**, mentre il campo content è la struttura seguente:

SequenceOfAny ::= SEQUENCE OF ANY

I [**BLOB \_ \_ DER CRYPT**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))in [**CRYPT \_ CONTENT INFO SEQUENCE OF \_ \_ \_ \_ ANY**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)'s **rgValue** puntano ai certificati X509 codificati.

Per le estensioni SzOID \_ NETSCAPE \_ CERT TYPE, sono definiti \_ i bit seguenti.



| Valore bit | Tipo corrispondente                      |
|-----------|-----------------------------------------|
| 0x80      | TIPO DI \_ CERTIFICATO DI AUTENTICAZIONE CLIENT SSL \_ \_ \_ \_ NETSCAPE |
| 0x40      | NETSCAPE \_ SSL \_ SERVER \_ AUTH \_ CERT \_ TYPE |
| 0x04      | NETSCAPE \_ SSL \_ CA \_ CERT \_ TYPE           |



 

Per le estensioni \_ szOID NETSCAPE REVOCATION URL, è possibile usare un URL relativo o assoluto per controllare lo stato \_ di revoca di un \_ certificato. Il controllo di revoca verrà eseguito come metodo HTTP GET usando un URL che è la concatenazione di revoca-URL e certificate-serial-number. Il numero di serie del certificato viene codificato come stringa di cifre esadecimali ASCII. Ad esempio, se netscape-base-url è https: \/ /www.certs-r-us.com/, netscape-revocation-url è cgi-bin/check-rev.cgi?, e il numero di serie del certificato è 173420, l'URL risultante sarà: https: \/ /www.certs-r-us.com/cgi-bin/check-rev.cgi?02a56c.

Il server deve restituire un documento con content-type di application/x-netscape-revocation. Il documento deve contenere una singola cifra ASCII, "1" se il certificato non è attualmente valido e "0" se è attualmente valido.

Si noti che per tutti gli URL che includono il numero di serie del certificato, il numero di serie verrà codificato come stringa costituita da un numero pari di cifre esadecimali. Se il numero di cifre significative è dispari, la stringa avrà un singolo zero iniziale per garantire che sia generato un numero pari di cifre.

 

 
