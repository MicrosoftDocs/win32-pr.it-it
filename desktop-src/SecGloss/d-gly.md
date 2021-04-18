---
description: Contiene le definizioni dei termini di sicurezza che iniziano con la lettera D.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: d007cbb9-b547-4dc7-bc22-b526f650f7c2
title: D (Glossario sulla sicurezza)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f81a17b2ba2c34b6d5367c1f920ad4b2a4048b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314688"
---
# <a name="d-security-glossary"></a>D (Glossario sulla sicurezza)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) d [E](e-gly.md) F [G](g-gly.md) [H](h-gly.md) [i](i-gly.md) J [K](k-gly.md) [L](l-gly.md) [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_dac_gly"></span><span id="_SECURITY_DAC_GLY"></span>**DAC**
</dt> <dd>

Vedere *controllo dinamico degli accessi*.

</dd> <dt>

<span id="_security_dacl_gly"></span><span id="_SECURITY_DACL_GLY"></span>**DACL**
</dt> <dd>

Vedere *l'elenco di controllo di accesso discrezionale*.

</dd> <dt>

<span id="_security_data_content_type_gly"></span><span id="_SECURITY_DATA_CONTENT_TYPE_GLY"></span>**tipo di contenuto dati**
</dt> <dd>

Tipo di contenuto di base definito da PKCS \# 7. Il contenuto dei dati è semplicemente una stringa ottetto (byte).

</dd> <dt>

<span id="_security_data_encryption_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_GLY"></span>**crittografia dei dati**
</dt> <dd>

Vedere [*crittografia*](e-gly.md).

</dd> <dt>

<span id="_security_data_encryption_function_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_FUNCTION_GLY"></span>**funzione di crittografia dei dati**
</dt> <dd>

Vedere [*funzioni di crittografia e decrittografia*](e-gly.md).

</dd> <dt>

<span id="_security_data_encryption_standard_gly"></span><span id="_SECURITY_DATA_ENCRYPTION_STANDARD_GLY"></span>**Standard di crittografia dei dati**
</dt> <dd>

DES Crittografia a blocchi che esegue la crittografia dei dati in blocchi a 64 bit. DES è un algoritmo simmetrico che usa lo stesso algoritmo e la stessa chiave per la crittografia e la decrittografia.

Sviluppato nel primo 1970, DES è anche noto come DEA (Data Encryption Algorithm) da ANSI e da DEA-1 per ISO.

</dd> <dt>

<span id="_security_datagram_gly"></span><span id="_SECURITY_DATAGRAM_GLY"></span>**datagramma**
</dt> <dd>

Canale di comunicazione che utilizza le informazioni indirizzate tramite una rete di cambio di pacchetti. Queste informazioni includono pacchetti di informazioni separate e le informazioni di recapito associate a tali pacchetti, ad esempio l'indirizzo di destinazione. In una rete con cambio di pacchetti i pacchetti di dati vengono instradati in modo indipendente l'uno dall'altro e possono seguire diverse route. Possono inoltre arrivare in un ordine diverso rispetto a quello in cui sono stati inviati.

</dd> <dt>

<span id="_security_decoding_gly"></span><span id="_SECURITY_DECODING_GLY"></span>**decodifica**
</dt> <dd>

Il processo di conversione di un oggetto codificato (ad esempio un certificato) o di dati di nuovo nel formato originale.

In termini generali, i dati vengono decodificati dal livello di codifica/decodifica del protocollo di comunicazione. I certificati vengono decodificati da una chiamata alla funzione **CryptDecodeObject** .

</dd> <dt>

<span id="_security_decryption_gly"></span><span id="_SECURITY_DECRYPTION_GLY"></span>**decrittografia**
</dt> <dd>

Processo di conversione del testo crittografato in testo non crittografato. La decrittografia è l'opposto della crittografia.

</dd> <dt>

<span id="_security_default_mode_gly"></span><span id="_SECURITY_DEFAULT_MODE_GLY"></span>**modalità predefinita**
</dt> <dd>

Impostazioni predefinite, ad esempio la modalità di crittografia a blocchi o il metodo di riempimento della crittografia a blocchi.

</dd> <dt>

<span id="_security_der_gly"></span><span id="_SECURITY_DER_GLY"></span>**DER**
</dt> <dd>

Vedere *Distinguished Encoding Rules*.

</dd> <dt>

<span id="_security_derived_key_gly"></span><span id="_SECURITY_DERIVED_KEY_GLY"></span>**chiave derivata**
</dt> <dd>

Chiave crittografica creata da una chiamata alla funzione **CryptDeriveKey** . Una chiave derivata può essere creata da una password o da altri dati utente. Le chiavi derivate consentono alle applicazioni di creare chiavi di sessione in base alle esigenze, eliminando la necessità di archiviare una chiave specifica.

</dd> <dt>

<span id="_security_des_gly"></span><span id="_SECURITY_DES_GLY"></span>**DES**
</dt> <dd>

Vedere *Data Encryption Standard*.

</dd> <dt>

<span id="_security_dh_gly"></span><span id="_SECURITY_DH_GLY"></span>**DH**
</dt> <dd>

Vedere *algoritmo Diffie-Hellman*.

</dd> <dt>

<span id="_security_dh_keyx_gly"></span><span id="_SECURITY_DH_KEYX_GLY"></span>**\_KEYX DH**
</dt> <dd>

Nome dell'algoritmo CryptoAPI per il Diffie-Hellman algoritmo di scambio delle chiavi.

Vedere anche *algoritmo Diffie-Hellman*.

</dd> <dt>

<span id="_security_diffie_hellman_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_ALGORITHM_GLY"></span>**Algoritmo Diffie-Hellman**
</dt> <dd>

DH Algoritmo di chiave pubblica utilizzato per lo scambio di chiave protetto. Non è possibile usare Diffie-Hellman per la crittografia dei dati. Questo algoritmo viene specificato come algoritmo di scambio delle chiavi per i tipi di provider di prova \_ DSS \_ DH.

Vedere anche l'algoritmo di scambio di chiave e l'algoritmo di scambio della chiave Diffie- *Hellman (archiviazione e inoltri)* e l' *algoritmo di scambio di chiave Diffie-Hellman (effimero)*.

</dd> <dt>

<span id="_security_diffie_hellman_store_and_forward_key_exchange_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_STORE_AND_FORWARD_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Algoritmo di scambio della chiave Diffie-Hellman (Store e inoltr)**
</dt> <dd>

Algoritmo di Diffie-Hellman in cui i valori della chiave di scambio vengono conservati (in CSP) dopo che l'handle della chiave è stato eliminato definitivamente.

Vedere anche *algoritmo di scambio delle chiavi Diffie-Hellman (effimero)*.

</dd> <dt>

<span id="_security_diffie_hellman_ephemeral_key_exchange_algorithm_gly"></span><span id="_SECURITY_DIFFIE_HELLMAN_EPHEMERAL_KEY_EXCHANGE_ALGORITHM_GLY"></span>**Algoritmo di scambio di chiave Diffie-Hellman (effimero)**
</dt> <dd>

Algoritmo Diffie-Hellman in cui il valore della chiave di scambio viene eliminato dal CSP quando l'handle della chiave viene eliminato definitivamente.

Vedere anche l' *algoritmo di scambio della chiave Diffie-Hellman (archivia e invia)*.

</dd> <dt>

<span id="_security_digested_data_gly"></span><span id="_SECURITY_DIGESTED_DATA_GLY"></span>**dati digest**
</dt> <dd>

Tipo di contenuto dei dati definito da PKCS \# 7 costituito da qualsiasi tipo di dati e da un hash del messaggio (digest) del contenuto.

</dd> <dt>

<span id="_security_digital_certificate_gly"></span><span id="_SECURITY_DIGITAL_CERTIFICATE_GLY"></span>**certificato digitale**
</dt> <dd>

Vedere [*Certificate*](c-gly.md).

</dd> <dt>

<span id="_security_digital_envelope_gly"></span><span id="_SECURITY_DIGITAL_ENVELOPE_GLY"></span>**busta digitale**
</dt> <dd>

Messaggi privati crittografati tramite la chiave pubblica del destinatario. I messaggi in busta digitale possono essere decrittografati solo tramite la chiave privata del destinatario, consentendo solo al destinatario di comprendere il messaggio.

</dd> <dt>

<span id="_security_digital_signature_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_GLY"></span>**firma digitale**
</dt> <dd>

Dati che associano l'identità di un mittente alle informazioni inviate. Una firma digitale può essere inviata come entità a parte oppure insieme a un messaggio, un file o un qualsiasi altro contenuto con codifica digitale. Le firme digitali vengono utilizzate negli ambienti a chiave pubblica e forniscono servizi di autenticazione e integrità.

</dd> <dt>

<span id="_security_digital_signature_algorithm_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_ALGORITHM_GLY"></span>**Algoritmo di firma digitale**
</dt> <dd>

DSA Algoritmo di chiave pubblica specificato da Digital Signature Standard (DSS). DSA viene usato solo per generare firme digitali. Non può essere usato per la crittografia dei dati.

</dd> <dt>

<span id="_security_digital_signature_key_pair_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_KEY_PAIR_GLY"></span>**coppia di chiavi firma digitale**
</dt> <dd>

Vedere [*coppia di chiavi di firma*](s-gly.md).

</dd> <dt>

<span id="_security_digital_signature_standard_gly"></span><span id="_SECURITY_DIGITAL_SIGNATURE_STANDARD_GLY"></span>**Standard di firma digitale**
</dt> <dd>

DSS Standard che specifica l'algoritmo di firma digitale (DSA) per il rispettivo algoritmo di firma e SHA-1 come algoritmo hash del messaggio. DSA è una crittografia a chiave pubblica che viene usata solo per generare firme digitali e non può essere usata per la crittografia dei dati. DSS viene specificato dai \_ tipi di provider prova DSS, prov \_ DSS \_ DH e provo \_ .

</dd> <dt>

<span id="_security_discretionary_access_control_list_gly"></span><span id="_SECURITY_DISCRETIONARY_ACCESS_CONTROL_LIST_GLY"></span>**elenco di controllo di accesso discrezionale**
</dt> <dd>

DACL Elenco di controllo di accesso controllato dal proprietario di un oggetto che specifica l'accesso a utenti o gruppi specifici che possono avere per l'oggetto.

Vedere anche elenco di [*controllo di accesso*](a-gly.md) e elenco di controllo di [*accesso di sistema*](s-gly.md).

</dd> <dt>

<span id="_security_distinguished_encoding_rules_gly"></span><span id="_SECURITY_DISTINGUISHED_ENCODING_RULES_GLY"></span>**Distinguished Encoding Rules**
</dt> <dd>

DER Set di regole per la codifica dei dati definiti ASN. 1 come flusso di bit per l'archiviazione o la trasmissione esterna. Ogni oggetto ASN. 1 dispone esattamente di una codifica DER corrispondente. DER è definito nella raccomandazione CCITT X. 509, sezione 8,7. Si tratta di uno dei due metodi di codifica attualmente utilizzati da CryptoAPI.

</dd> <dt>

<span id="_security_dll_gly"></span><span id="_SECURITY_DLL_GLY"></span>**DLL**
</dt> <dd>

Vedere *libreria a collegamento dinamico*.

</dd> <dt>

<span id="_security_dsa_gly"></span><span id="_SECURITY_DSA_GLY"></span>**DSA**
</dt> <dd>

Vedere *algoritmo di firma digitale*.

</dd> <dt>

<span id="_security_dss_gly"></span><span id="_SECURITY_DSS_GLY"></span>**DSS**
</dt> <dd>

Vedere *Digital Signature Standard*.

</dd> <dt>

<span id="_security_dynamic_access_control_gly"></span><span id="_SECURITY_DYNAMIC_ACCESS_CONTROL_GLY"></span>**Controllo dinamico degli accessi**
</dt> <dd>

DAC Possibilità di specificare i criteri di controllo di accesso in base alle attestazioni di utente, dispositivo e risorsa. Questo rende più flessibile l'autenticazione per le applicazioni mantenendo i requisiti di sicurezza e conformità.

</dd> <dt>

<span id="_security_dynamic_link_library_gly"></span><span id="_SECURITY_DYNAMIC_LINK_LIBRARY_GLY"></span>**libreria a collegamento dinamico**
</dt> <dd>

(DLL) file che contiene routine eseguibili che possono essere chiamate da altre applicazioni.

</dd> </dl>

 

 



