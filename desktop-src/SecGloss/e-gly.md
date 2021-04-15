---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera E.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: f1caccd2-3453-448e-b194-bf899eff8091
title: E (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed30465ef5764d4553ceb03e1094b73d940f85f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529568"
---
# <a name="e-security-glossary"></a>E (Glossario sulla sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [d](d-gly.md) E F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ecb_gly"></span><span id="_SECURITY_ECB_GLY"></span>**BCE**
</dt> <dd>

Vedere *Electronic Codebook*.

</dd> <dt>

<span id="_security_ecc_gly"></span><span id="_SECURITY_ECC_GLY"></span>**ECC**
</dt> <dd>

Vedere *crittografia a curva ellittica*.

</dd> <dt>

<span id="_security_efs_gly"></span><span id="_SECURITY_EFS_GLY"></span>**EFS**
</dt> <dd>

Vedere *Encrypting File System*.

</dd> <dt>

<span id="_security_eku_gly"></span><span id="_SECURITY_EKU_GLY"></span>**EKU**
</dt> <dd>

Vedere *utilizzo chiavi avanzato*.

</dd> <dt>

<span id="_security_electronic_codebook_gly"></span><span id="_SECURITY_ELECTRONIC_CODEBOOK_GLY"></span>**Codebook elettronico**
</dt> <dd>

BCE Modalità di crittografia A blocchi (ogni blocco viene crittografato singolarmente) che non usa commenti e suggerimenti. Ciò significa che qualsiasi blocco di testo normale identico (nello stesso messaggio o in un messaggio diverso crittografato con la stessa chiave) viene trasformato in blocchi di testo crittografato identici. I vettori di inizializzazione non possono essere utilizzati con questa modalità di crittografia. Se un singolo bit del blocco di testo crittografato viene confuso, viene anche confuso l'intero blocco di testo non crittografato corrispondente.

</dd> <dt>

<span id="_security_elliptic_curve_cryptography_gly"></span><span id="_SECURITY_ELLIPTIC_CURVE_CRYPTOGRAPHY_GLY"></span>**crittografia a curva ellittica**
</dt> <dd>

ECC Approccio alla crittografia a chiave pubblica basata sulle proprietà delle curve ellittiche. Il vantaggio principale dell'ECC è l'efficienza, che diventa importante quando i dispositivi diventano più piccoli e i requisiti di sicurezza sono più complessi. Ad esempio, le chiavi ECC tra 163 bit e 512 bit sono da 1 a 6 a un trentesimo le dimensioni delle chiavi RSA a livello di sicurezza equivalenti. Man mano che le dimensioni della chiave aumentano l'efficienza relativa degli aumenti ECC.

</dd> <dt>

<span id="_security_encoding_gly"></span><span id="_SECURITY_ENCODING_GLY"></span>**codifica**
</dt> <dd>

Modalità di conversione dei dati in flussi di bit. La codifica è una parte del processo di serializzazione che converte i dati in un flusso di zero e uno.

</dd> <dt>

<span id="_security_encoding_type_gly"></span><span id="_SECURITY_ENCODING_TYPE_GLY"></span>**tipo di codifica**
</dt> <dd>

Indica il tipo di codifica utilizzato per la codifica dei messaggi e dei certificati. I tipi di codifica vengono specificati come **DWORD**, con il tipo di codifica del certificato archiviato nella parola di basso livello e il tipo di codifica dei messaggi archiviati nella parola più ordinata. Sebbene alcune funzioni o campi della struttura richiedano solo uno dei tipi di codifica, è sempre accettabile specificare entrambi.

</dd> <dt>

<span id="_security_encryption_gly"></span><span id="_SECURITY_ENCRYPTION_GLY"></span>**crittografia**
</dt> <dd>

Processo di conversione del testo non crittografato in testo crittografato per impedirne la lettura e la comprensione da parte di utenti non autorizzati. La crittografia è l'opposto della decrittografia.

</dd> <dt>

<span id="_security_encrypted_data_gly"></span><span id="_SECURITY_ENCRYPTED_DATA_GLY"></span>**dati crittografati**
</dt> <dd>

Dati che sono stati convertiti da testo non crittografato a testo crittografato. I messaggi crittografati vengono utilizzati per mascherare il contenuto di un messaggio quando viene inviato o archiviato.

</dd> <dt>

<span id="_security_encrypting_file_system_gly"></span><span id="_SECURITY_ENCRYPTING_FILE_SYSTEM_GLY"></span>**Encrypting File System**
</dt> <dd>

EFS Funzionalità del sistema operativo Windows che consente agli utenti di crittografare file e cartelle in un disco del volume NTFS per mantenerli protetti dall'accesso da parte di eventuali intrusi.

</dd> <dt>

<span id="_security_encryption_and_decryption_functions_gly"></span><span id="_SECURITY_ENCRYPTION_AND_DECRYPTION_FUNCTIONS_GLY"></span>**funzioni di crittografia e decrittografia**
</dt> <dd>

Funzioni di messaggio semplificate utilizzate per codificare e crittografare o decodificare e decrittografare i dati. Come set, queste funzioni includono il supporto per la crittografia e la decrittografia simultanea dei dati.

Vedere anche [*funzioni di messaggio semplificate*](s-gly.md).

</dd> <dt>

<span id="_security_enhanced_content_type_gly"></span><span id="_SECURITY_ENHANCED_CONTENT_TYPE_GLY"></span>**tipo di contenuto migliorato**
</dt> <dd>

Classe di dati contenuta in un \# messaggio PKCS 7 contenente dati (probabilmente crittografati), oltre a miglioramenti crittografici, ad esempio hash o firme. I tipi di dati avanzati definiti da PKCS \# 7 includono i dati firmati, i dati in busta, i dati con firma e la busta e i dati di cui è stato eseguito il digest (con hash).

</dd> <dt>

<span id="_security_enhanced_key_usage_gly"></span><span id="_SECURITY_ENHANCED_KEY_USAGE_GLY"></span>**utilizzo chiavi avanzato**
</dt> <dd>

EKU Sia un'estensione del certificato che un valore della proprietà estesa del certificato. Un EKU specifica gli utilizzi per i quali un certificato è valido.

</dd> <dt>

<span id="_security_enveloped_data_content_type_gly"></span><span id="_SECURITY_ENVELOPED_DATA_CONTENT_TYPE_GLY"></span>**tipo di contenuto dati in busta**
</dt> <dd>

\#Contenuto avanzato PKCS 7 costituito da contenuto crittografato (di qualsiasi tipo) e da chiavi di crittografia del contenuto (per uno o più destinatari). La combinazione di contenuto crittografato e chiave di crittografia per un destinatario è detta *busta digitale* per il destinatario. Questo tipo di messaggio deve essere utilizzato quando si desidera tenere il contenuto del segreto del messaggio e consentire solo a persone o entità specifiche di recuperare il contenuto.

</dd> <dt>

<span id="_security_exchange_key_gly"></span><span id="_SECURITY_EXCHANGE_KEY_GLY"></span>**chiave di scambio**
</dt> <dd>

Vedere *coppia di chiavi di scambio*.

</dd> <dt>

<span id="_security_exchange_key_pair_gly"></span><span id="_SECURITY_EXCHANGE_KEY_PAIR_GLY"></span>**coppia di chiavi di scambio**
</dt> <dd>

Coppia di chiavi pubblica/privata utilizzata per crittografare le chiavi di sessione affinché possano essere archiviate e scambiate in modo sicuro con altri utenti. Le coppie di chiavi di scambio vengono create chiamando la funzione **CryptGenKey** .

Confrontare la [*coppia di chiavi di firma*](s-gly.md).

</dd> <dt>

<span id="_security_external_store_gly"></span><span id="_SECURITY_EXTERNAL_STORE_GLY"></span>**Archivio esterno**
</dt> <dd>

Archivio certificati che gestisce i certificati, i CRL e scopi consentiti in un percorso esterno alla memoria memorizzata nella cache, ad esempio in un database in un server di rete. Un archivio esterno non legge e decodifica i relativi certificati, CRL e CTL quando viene chiamata la funzione **CertOpenStore** . La lettura e la decodifica vengono posticipate fino a quando non viene chiamato un metodo di enumerazione o di ricerca.

</dd> </dl>

 

 



