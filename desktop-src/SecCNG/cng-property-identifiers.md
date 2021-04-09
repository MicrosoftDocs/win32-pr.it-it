---
description: Utilizzato con le funzioni BCryptGetProperty e BCryptSetProperty per identificare una proprietà.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Identificatori delle proprietà primitive di crittografia (bcrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 71f4996a216fbc4fbf63216f99b5f630c4769e97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878614"
---
# <a name="cryptography-primitive-property-identifiers"></a>Identificatori delle proprietà primitive di crittografia

Per identificare una proprietà vengono usati i valori seguenti con le funzioni [**BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) e [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) .

<dl> <dt>

<span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**\_nome dell'algoritmo BCRYPT \_**
</dt> <dd> <dl> <dt>

L "algorithmName"
</dt> <dt>



Stringa Unicode con terminazione null che contiene il nome dell'algoritmo.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**\_lunghezza del \_ tag di autenticazione BCRYPT \_**
</dt> <dd> <dl> <dt>

L "AuthTagLength"
</dt> <dt>



Lunghezze dei tag di autenticazione supportate dall'algoritmo. Questa proprietà è una [**struttura \_ \_ \_ \_ struct di lunghezze di tag di autenticazione BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) . Questa proprietà si applica solo agli algoritmi.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**\_Lunghezza blocco \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "BlockLength"
</dt> <dt>



Dimensione, in byte, di un blocco di crittografia per l'algoritmo. Questa proprietà si applica solo agli algoritmi di crittografia a blocchi. Questo tipo di dati è un **valore DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**\_ \_ elenco dimensioni blocco \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "BlockSizeList"
</dt> <dt>



Elenco delle lunghezze dei blocchi supportate da un algoritmo di crittografia. Questo tipo di dati è una matrice di **DWORD**. Il numero di elementi nella matrice può essere determinato dividendo il numero di byte recuperati dalla dimensione di un singolo **valore DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**\_modalità di concatenamento BCRYPT \_**
</dt> <dd> <dl> <dt>

L "ChainingMode"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione null che rappresenta la modalità di concatenamento dell'algoritmo di crittografia. Questa proprietà può essere impostata su un handle di algoritmo o un handle di chiave per uno dei valori seguenti.



| Identificatore                   | Valore                         | Descrizione                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CBC (BCRYPT \_ Chain \_ mode) \_** | L "ChainingModeCBC"<br/> | Imposta la modalità di concatenamento dell'algoritmo sul [*concatenamento dei blocchi crittografici*](/windows/desktop/SecGloss/c-gly).<br/>            |
| **\_ \_ CCM modalità a catena BCRYPT \_** | L "ChainingModeCCM"<br/> | Imposta la modalità di concatenamento dell'algoritmo su Counter con la modalità CBC-MAC (CCM). **Windows Vista:** Questo valore è supportato a partire da Windows Vista con SP1.<br/> <br/> |
| **\_modalità a catena BCRYPT \_ \_ CFB** | L "ChainingModeCFB"<br/> | Imposta la modalità di concatenamento dell'algoritmo su [*feedback crittografico*](/windows/desktop/SecGloss/c-gly).<br/>                              |
| **BCRYPT \_ Chain \_ mode \_ BCE** | L "ChainingModeECB"<br/> | Imposta la modalità di concatenamento dell'algoritmo su [*Electronic Codebook*](/windows/desktop/SecGloss/e-gly).<br/>                  |
| **\_modalità a catena BCRYPT \_ \_ GCM** | L "ChainingModeGCM"<br/> | Imposta la modalità di concatenamento dell'algoritmo su Galois/Counter Mode (GCM). **Windows Vista:** Questo valore è supportato a partire da Windows Vista con SP1.<br/> <br/>       |
| **\_modalità a catena BCRYPT \_ \_ na**  | L "ChainingModeN/A"<br/> | L'algoritmo non supporta il concatenamento.<br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**\_parametri DH \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "DHParameters"
</dt> <dt>



Specifica i parametri da utilizzare con una chiave Diffie-Hellman. Questo tipo di dati è un puntatore a una struttura di [**\_ intestazione del \_ parametro \_ BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) . Questa proprietà può essere impostata solo e deve essere impostata per la chiave prima del completamento della chiave.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**\_parametri DSA \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "DSAParameters"
</dt> <dt>



Specifica i parametri da usare con una chiave DSA. Questa proprietà è un' [**\_ intestazione del \_ parametro \_ DSA BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) o una struttura dell' [**intestazione del \_ parametro DSA BCRYPT \_ \_ \_ v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) . Questa proprietà può essere impostata solo e deve essere impostata per la chiave prima del completamento della chiave.

**Windows 8:** A partire da Windows 8, questa proprietà può essere una struttura [**BCRYPT \_ DSA \_ Parameter \_ header \_ v2**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) . Usare questa struttura se la dimensione della chiave supera 1024 bit ed è minore o uguale a 3072 bit. Se la dimensione della chiave è maggiore o uguale a 512 ma minore o uguale a 1024 bit, usare la struttura [**dell' \_ \_ \_ intestazione del parametro BCRYPT DSA**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**\_ \_ Lunghezza chiave effettiva \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "EffectiveKeyLength"
</dt> <dt>



Dimensione, in bit, della lunghezza effettiva di una chiave RC2. Questo tipo di dati è un **valore DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**\_ \_ Lunghezza blocco hash \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "HashBlockLength"
</dt> <dt>



Dimensione, in byte, del blocco per un hash. Questa proprietà si applica solo agli algoritmi hash. Questo tipo di dati è un **valore DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**\_lunghezza hash \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "HashDigestLength"
</dt> <dt>



Dimensione, in byte, del valore hash di un provider hash. Questo tipo di dati è un **valore DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**\_elenco di \_ OID \_ hash BCRYPT**
</dt> <dd> <dl> <dt>

L "HashOIDList"
</dt> <dt>



Elenco di [*identificatori di oggetti*](/windows/desktop/SecGloss/o-gly) hash codificati [*der*](/windows/desktop/SecGloss/d-gly)(OID). Questa proprietà è una struttura dell' [**\_ \_ elenco di OID BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) . Questa proprietà può essere letta solo.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**\_vettore di inizializzazione BCRYPT \_**
</dt> <dd> <dl> <dt>

L "IV"
</dt> <dt>



Contiene il [*vettore di inizializzazione*](/windows/desktop/SecGloss/i-gly) (IV) per una chiave. Questa proprietà si applica solo alle chiavi.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**\_lunghezza della chiave BCRYPT \_**
</dt> <dd> <dl> <dt>

L "lunghezza della lunghezza"
</dt> <dt>



Dimensione, in bit, del valore della chiave di un provider di chiavi simmetriche. Questo tipo di dati è un **valore DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**\_lunghezze della chiave BCRYPT \_**
</dt> <dd> <dl> <dt>

L "lunghezze della lunghezza"
</dt> <dt>



Lunghezze delle chiavi supportate dall'algoritmo. Questa proprietà è una [**struttura \_ \_ \_ struct della lunghezza della chiave BCRYPT**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) . Questa proprietà si applica solo agli algoritmi.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**\_lunghezza dell' \_ oggetto \_ chiave BCRYPT**
</dt> <dd> <dl> <dt>

L "KeyObjectLength"
</dt> <dt>



Questa proprietà non viene utilizzata. Per ottenere queste informazioni, viene usata la proprietà **BCRYPT \_ Object \_ length** .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**\_complessità della chiave BCRYPT \_**
</dt> <dd> <dl> <dt>

L "livello di attendibilità"
</dt> <dt>



Numero di bit nella chiave. Questo tipo di dati è un **valore DWORD**. Questa proprietà si applica solo alle chiavi.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**\_lunghezza del \_ blocco di messaggi BCRYPT \_**
</dt> <dd> <dl> <dt>

L "MessageBlockLength"
</dt> <dt>



Questo può essere impostato su qualsiasi handle di chiave con la modalità di concatenamento CFB impostata. Per impostazione predefinita, questa proprietà è impostata su 1 per CFB a 8 bit. Se viene impostato sulla dimensione del blocco in byte, viene utilizzato il CFB di blocco completo. Per le chiavi XTS, viene usato per impostare le dimensioni, in byte, dell'unità dati XTS (in genere 512 o 4096).


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**\_ \_ lunghezza MULTIoggetto \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "MultiObjectLength"
</dt> <dt>



Questa proprietà restituisce uno [**\_ struct di \_ \_ lunghezza BCRYPT \_ multioggetto**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct)che contiene le informazioni necessarie per calcolare le dimensioni di un buffer di oggetti. Questa proprietà è supportata solo nelle versioni del sistema operativo che supportano la funzione [**BCryptCreateMultiHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash) .


</dt> </dl> </dd> <dt>

<span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**\_lunghezza dell'oggetto BCRYPT \_**
</dt> <dd> <dl> <dt>

L "ObjectLength"
</dt> <dt>



Dimensione, in byte, del sottooggetto di un provider. Questo tipo di dati è un **valore DWORD**. Attualmente, i provider di algoritmi di crittografia hash e simmetrico utilizzano buffer allocati dal chiamante per archiviare i relativi oggetti sottooggetti. Per il provider hash, ad esempio, è necessario allocare memoria per l'oggetto hash ottenuto con la funzione [**BCryptCreateHash**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) . Questa proprietà fornisce le dimensioni del buffer per l'oggetto di un provider, in modo da poter allocare memoria per l'oggetto creato dal provider.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**\_schemi di riempimento BCRYPT \_**
</dt> <dd> <dl> <dt>

L "PaddingSchemes"
</dt> <dt>



Rappresenta lo schema di riempimento del provider di algoritmi RSA. Questo tipo di dati è un **valore DWORD**. Può corrispondere a uno dei valori seguenti.



| Identificatore                             | Valore      | Descrizione                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| **\_router di \_ riempimento \_ supportato da BCRYPT**     | 0x00000001 | Il provider supporta la spaziatura interna aggiunta dal router.         |
| **BCRYPT \_ \_ Pad supportato \_ PKCS1 \_ enc** | 0x00000002 | Il provider supporta lo schema di riempimento della crittografia PKCS1. |
| **BCRYPT \_ \_ Pad supportato \_ PKCS1 \_ sig** | 0x00000004 | Il provider supporta lo schema di riempimento della firma PKCS1.  |
| **\_ \_ OAEP Pad supportato da BCRYPT \_**       | 0x00000008 | Il provider supporta lo schema di riempimento OAEP.             |
| **BCRYPT \_ Pad supportato da \_ \_ PSS**        | 0x00000010 | Il provider supporta lo schema di riempimento PSS.              |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**\_handle del provider BCRYPT \_**
</dt> <dd> <dl> <dt>

L "ProviderHandle"
</dt> <dt>



Handle del provider CNG che ha creato l'oggetto passato nel parametro *hObject* . Questo tipo di dati è **un \_ \_ handle BCRYPT ALG**. Questa proprietà può essere recuperata solo. non può essere impostata.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**\_lunghezza firma \_ BCRYPT**
</dt> <dd> <dl> <dt>

L "SignatureLength"
</dt> <dt>



Dimensione, in byte, della lunghezza di una firma per una chiave. Questo tipo di dati è un **valore DWORD**. Questa proprietà si applica solo alle chiavi. Questa proprietà può essere recuperata solo. non può essere impostata.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Bcrypt. h</dt> </dl> |



 

