---
description: Utilizzato con le operazioni di codifica e decodifica.
ms.assetid: 713c95ae-e5d0-416c-ba0c-4b5399aa8a33
title: Costanti per le estensioni Netscape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06999a879d0d289bb95cdb8ba5506200154d60e4
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/10/2021
ms.locfileid: "103886265"
---
# <a name="constants-for-netscape-extensions"></a>Costanti per le estensioni Netscape

Le estensioni Netscape seguenti vengono utilizzate con le operazioni di codifica e decodifica. Le costanti e gli identificatori di oggetto di Netscape predefiniti non vengono usati direttamente con le funzioni di codifica o decodifica, [**CryptEncodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobject), [**CryptEncodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobjectex), [**CryptSignAndEncodeCertificate**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate), [**CryptDecodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobject)o [**CryptDecodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex). Queste estensioni richiedono invece l'uso del *lpszStructType* visualizzato.

Per altri dettagli applicabili ad alcune estensioni di Netscape, vedere la sezione osservazioni che seguono la tabella.



| Identificatori di oggetto estensione del certificato Netscape                      | *lpszStructType*                                           | *PvStructInfo* corrispondente                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| URL di base di szOID \_ Netscape \_ \_ "2.16.840.1.113730.1.2"<br/>           | X509 \_ qualsiasi stringa \_ o X509 \_ Unicode \_ qualsiasi \_ stringa<br/> | [**Certificato \_ \_valore del nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il membro **dwValueType** è impostato su cert \_ RDN \_ IA5 \_ String. Il membro **pbData** del membro del **valore** punta a una \_ stringa IA5 aggiunta all'inizio di tutti gli indirizzi URL relativi in un certificato. Questa estensione può essere considerata un'ottimizzazione per ridurre le dimensioni delle estensioni URL.                                                                                                       |
| \_ \_ URL criterio CA szOID Netscape \_ \_ "2.16.840.1.113730.1.8"<br/>     | X509 \_ qualsiasi stringa \_ o X509 \_ Unicode \_ qualsiasi \_ stringa<br/> | [**Certificato \_ \_valore del nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il membro **dwValueType** è impostato su cert \_ RDN \_ IA5 \_ String. Il membro **pbData** del membro del **valore** punta a una \_ stringa IA5, l'URL relativo o assoluto della pagina Web che descrive i criteri con cui è stato emesso il certificato.                                                                                                                                                            |
| szOID \_ \_ URL di \_ revoca CA Netscape \_ "2.16.840.1.113730.1.4"<br/> | X509 \_ qualsiasi stringa \_ o X509 \_ Unicode \_ qualsiasi \_ stringa<br/> | [**Certificato \_ \_valore del nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il membro **dwValueType** è impostato su cert \_ RDN \_ IA5 \_ String. Il membro **pbData** del membro del **valore** punta a una \_ stringa IA5 che rappresenta l'URL relativo o assoluto utilizzato per controllare lo stato di revoca dei certificati firmati dall' [*autorità di certificazione*](../secgloss/c-gly.md) a cui appartiene il certificato corrente. |
| \_URL di \_ rinnovo certificato szOID Netscape \_ \_ "2.16.840.1.113730.1.7"<br/>  | X509 \_ qualsiasi stringa \_ o X509 \_ Unicode \_ qualsiasi \_ stringa<br/> | [**Certificato \_ \_valore del nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il membro **dwValueType** è impostato su cert \_ RDN \_ IA5 \_ String. Il membro **pbData** del membro del **valore** punta a una \_ stringa IA5 che rappresenta l'URL relativo o assoluto di un modulo di rinnovo del certificato.                                                                                                                                                                                                     |
| \_sequenza di \_ certificati Netscape szOID \_ "2.16.840.1.113730.2.5"<br/>      | \_ \_ sequenza di informazioni sul contenuto PKCS \_ \_ di \_ qualsiasi                     | [**\_ \_ sequenza di informazioni sul contenuto Crypt \_ \_ di \_ qualsiasi**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)                                                                                                                                                                                                                                                                                                                                                                |
| \_tipo di \_ certificato Netscape szOID \_ "2.16.840.1.113730.1.1"<br/>          | \_Bit X509                                                 | [**\_BLOB di bit di Crypt \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_bit_blob)                                                                                                                                                                                                                                                                                                                                                                                                           |
| \_Commento szOID Netscape \_ "2.16.840.1.113730.1.13"<br/>            | X509 \_ qualsiasi stringa \_ o X509 \_ Unicode \_ qualsiasi \_ stringa<br/> | [**Certificato \_ \_valore del nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il membro **dwValueType** è impostato su cert \_ RDN \_ IA5 \_ String. Il membro **pbData** del membro del **valore** punta a una \_ stringa IA5 che è un commento da visualizzare quando il certificato viene visualizzato.                                                                                                                                                                                                         |
| URL di revoca di szOID \_ Netscape \_ \_ "2.16.840.1.113730.1.3"<br/>     | X509 \_ qualsiasi stringa \_ o X509 \_ Unicode \_ qualsiasi \_ stringa<br/> | [**Certificato \_ \_valore del nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il membro **dwValueType** è impostato su cert \_ RDN \_ IA5 \_ String. Il membro **pbData** del membro del **valore** punta a una \_ stringa IA5 che corrisponde a un URL relativo o assoluto utilizzato per controllare lo stato di revoca del certificato.                                                                                                                                                                              |
| \_nome del server szOID Netscape \_ SSL \_ \_ "2.16.840.1.113730.1.12"<br/>  | X509 \_ qualsiasi stringa \_ o X509 \_ Unicode \_ qualsiasi \_ stringa<br/> | [**Certificato \_ \_valore del nome**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). Il membro **dwValueType** è impostato su cert \_ RDN \_ IA5 \_ String. Il membro **pbData** del membro del **valore** punta a una \_ stringa IA5 che è un'espressione shell utilizzata per associare il nome host al server SSL utilizzando questo certificato.                                                                                                                                                                       |



 

Per tutte le funzioni di codifica che usano X509 \_ Any \_ String o X5O9 \_ Unicode \_ Any \_ String **lpszStructType**, X509 \_ qualsiasi \_ stringa viene usata se il formato della stringa nel membro **pbData** del membro **value** è [*ASCII*](../secgloss/a-gly.md)e X509 \_ Unicode \_ qualsiasi \_ stringa viene usata se il formato della stringa è Unicode. Nel caso Unicode, la stringa deve essere convertita in una \_ stringa IA5 prima della codifica impostando il membro **dwValueType** della struttura del [**\_ \_ valore del nome del certificato**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value) su cert \_ RDN \_ IA5 \_ String.

Per le funzioni di decodifica, l'utente seleziona il formato della stringa di output. Usare X509 \_ qualsiasi \_ stringa se il formato stringa desiderato è ASCII e X509 \_ Unicode \_ qualsiasi \_ stringa se il formato della stringa desiderato è Unicode.

Per l' \_ estensione szOID Netscape \_ CERT \_ Renewal \_ URL, la struttura dei dati contiene un URL relativo o assoluto che punta a un modulo di rinnovo del certificato. Il modulo di rinnovo sarà accessibile con un metodo HTTP GET usando un URL che corrisponde alla concatenazione dell'URL di rinnovo e del numero di serie del certificato. Il numero di serie certificate è codificato come stringa di cifre esadecimali ASCII. Se, ad esempio, Netscape-base-URL è https://*autorità di certificazione URL*/, l'URL Netscape-CERT-Renewal è cgi-bin/check-Renew. cgi? e il numero di serie del certificato è 173420, l'URL risultante sarà: https://*Certification Authority URL*/cgi-bin/check-Renew.cgi? 02a56c. Il documento restituito deve essere un form HTML che consentirà all'utente di richiedere un rinnovo del certificato.

Per l' \_ estensione szOID Netscape \_ CERT \_ Sequence che usa la \_ codifica ASN X509 \_ , il certificato viene codificato come una \_ struttura di informazioni sul contenuto PKCS che racchiude \_ una sequenza di qualsiasi. Il valore del membro **ContentType** è **pszObjId**, mentre il campo Content è la struttura seguente:

SequenceOfAny:: = sequenza di qualsiasi

Il [**\_ \_ BLOB der di Crypt der**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))nella [**\_ \_ sequenza di informazioni sul contenuto \_ della crittografia \_ del \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)membro **rgValue** di qualsiasi punto del membro del punto di X509 codificato.

Per \_ \_ le estensioni di tipo CERT di szOID Netscape \_ , vengono definiti i seguenti bit.



| Valore bit | Tipo corrispondente                      |
|-----------|-----------------------------------------|
| 0x80      | \_tipo di \_ \_ certificato di autenticazione client \_ \_ di Netscape SSL |
| 0x40      | \_tipo di \_ \_ certificato di autenticazione del server SSL \_ Netscape \_ |
| 0x04      | \_tipo di \_ \_ certificato CA SSL di \_ Netscape           |



 

Per le \_ \_ estensioni URL di revoca \_ di szOID Netscape, è possibile usare un URL relativo o assoluto per controllare lo stato di revoca di un certificato. Il controllo della revoca verrà eseguito come metodo HTTP GET usando un URL che corrisponde alla concatenazione di revoca-URL e al numero di serie certificate. Il numero di serie certificate è codificato come stringa di cifre esadecimali ASCII. Se, ad esempio, Netscape-base-URL è https: \/ /www.certs-r-US.com/, Netscape-revoca-URL è cgi-bin/check-Rev. cgi? e il numero di serie del certificato è 173420, l'URL risultante sarà: https: \/ /www.certs-r-US.com/cgi-bin/check-Rev.cgi?02a56c.

Il server deve restituire un documento con un tipo di contenuto application/x-Netscape-revoca. Il documento deve contenere una singola cifra ASCII, "1" Se il certificato non è attualmente valido e "0" se è attualmente valido.

Si noti che per tutti gli URL che includono il numero di serie del certificato, il numero di serie verrà codificato come stringa costituita da un numero pari di cifre esadecimali. Se il numero di cifre significative è dispari, la stringa avrà un singolo zero iniziali per assicurarsi che venga generato un numero pari di cifre.

 

 
