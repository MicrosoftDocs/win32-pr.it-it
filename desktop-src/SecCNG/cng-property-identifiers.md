---
description: Usato con le funzioni BCryptGetProperty e BCryptSetProperty per identificare una proprietà.
ms.assetid: ebcc8202-94b4-47ad-9918-e5bc843a258f
title: Identificatori di proprietà primitive di crittografia (Bcrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5452c6a55388998a08577cb19ef2fba6905faddbdf28f5f8051b7bc8d9d1c375
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118908222"
---
# <a name="cryptography-primitive-property-identifiers"></a>Identificatori di proprietà primitive di crittografia

I valori seguenti vengono usati con le [**funzioni BCryptGetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptgetproperty) e [**BCryptSetProperty**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptsetproperty) per identificare una proprietà.

<dl> <dt>

<span id="BCRYPT_ALGORITHM_NAME"></span><span id="bcrypt_algorithm_name"></span>**NOME \_ DELL'ALGORITMO \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"AlgorithmName"
</dt> <dt>



Stringa Unicode con terminazione Null che contiene il nome dell'algoritmo.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_AUTH_TAG_LENGTH"></span><span id="bcrypt_auth_tag_length"></span>**LUNGHEZZA DEL TAG DI AUTENTICAZIONE BCRYPT \_ \_ \_**
</dt> <dd> <dl> <dt>

L"AuthTagLength"
</dt> <dt>



Lunghezze dei tag di autenticazione supportate dall'algoritmo . Questa proprietà è una [**struttura STRUCT BCRYPT \_ AUTH \_ TAG \_ LENGTHS. \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Questa proprietà si applica solo agli algoritmi.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_LENGTH"></span><span id="bcrypt_block_length"></span>**LUNGHEZZA DEL \_ BLOCCO \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"BlockLength"
</dt> <dt>



Dimensione, in byte, di un blocco di crittografia per l'algoritmo. Questa proprietà si applica solo agli algoritmi di crittografia a blocchi. Questo tipo di dati è **un valore DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_BLOCK_SIZE_LIST"></span><span id="bcrypt_block_size_list"></span>**ELENCO DELLE \_ DIMENSIONI DEL \_ BLOCCO BCRYPT \_**
</dt> <dd> <dl> <dt>

L"BlockSizeList"
</dt> <dt>



Elenco delle lunghezze dei blocchi supportate da un algoritmo di crittografia. Questo tipo di dati è una matrice **di DWORD**. Il numero di elementi nella matrice può essere determinato dividendo il numero di byte recuperati per le dimensioni di un singolo **valore DWORD.**


</dt> </dl> </dd> <dt>

<span id="BCRYPT_CHAINING_MODE"></span><span id="bcrypt_chaining_mode"></span>**MODALITÀ \_ CONCATENAMENTO \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"ChainingMode"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione Null che rappresenta la modalità di concatenamento dell'algoritmo di crittografia. Questa proprietà può essere impostata su un handle di algoritmo o un handle di chiave su uno dei valori seguenti.



| Identificatore                   | Valore                         | Descrizione                                                                                                                                                                    |
|------------------------------|-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **BCRYPT \_ CHAIN \_ MODE \_ CBC** | L"ChainingModeCBC"<br/> | Imposta la modalità di concatenamento dell'algoritmo [*su cipher block chaining*](/windows/desktop/SecGloss/c-gly).<br/>            |
| **MODALITÀ \_ CATENA \_ \_ BCRYPT CCM** | L"ChainingModeCCM"<br/> | Imposta la modalità di concatenamento dell'algoritmo su counter con la modalità CBC-MAC (CCM). **Windows Vista:** Questo valore è supportato a partire da Windows Vista con SP1.<br/> <br/> |
| **BCRYPT \_ CHAIN \_ MODE \_ CFB** | L"ChainingModeCFB"<br/> | Imposta la modalità di concatenamento dell'algoritmo [*su cipher feedback*](/windows/desktop/SecGloss/c-gly).<br/>                              |
| **BCE IN MODALITÀ CATENA BCRYPT \_ \_ \_** | L"ChainingModeECB"<br/> | Imposta la modalità di concatenamento dell'algoritmo su [*codebook elettronico.*](/windows/desktop/SecGloss/e-gly)<br/>                  |
| **BCRYPT \_ CHAIN \_ MODE \_ GCM** | L"ChainingModeGCM"<br/> | Imposta la modalità di concatenamento dell'algoritmo su Galese/modalità contatore (GCM). **Windows Vista:** Questo valore è supportato a partire da Windows Vista con SP1.<br/> <br/>       |
| **BCRYPT \_ CHAIN \_ MODE \_ NA**  | L"ChainingModeN/A"<br/> | L'algoritmo non supporta il concatenamento.<br/>                                                                                                                            |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DH_PARAMETERS"></span><span id="bcrypt_dh_parameters"></span>**PARAMETRI \_ DH \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"DHParameters"
</dt> <dt>



Specifica i parametri da usare con una Diffie-Hellman chiave. Questo tipo di dati è un puntatore a una [**struttura \_ BCRYPT DH \_ PARAMETER \_ HEADER.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Questa proprietà può essere impostata solo e deve essere impostata per la chiave prima del completamento della chiave.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_DSA_PARAMETERS"></span><span id="bcrypt_dsa_parameters"></span>**PARAMETRI \_ DSA \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"DSAParameters"
</dt> <dt>



Specifica i parametri da usare con una chiave DSA. Questa proprietà è una [**struttura BCRYPT \_ DSA \_ PARAMETER HEADER \_ o**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header) [**BCRYPT \_ DSA \_ PARAMETER HEADER \_ \_ V2.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) Questa proprietà può essere impostata solo e deve essere impostata per la chiave prima del completamento della chiave.

**Windows 8:** A partire Windows 8, questa proprietà può essere una [**struttura \_ BCRYPT DSA \_ PARAMETER HEADER \_ \_ V2.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header_v2) Utilizzare questa struttura se le dimensioni della chiave superano i 1024 bit ed è minore o uguale a 3072 bit. Se le dimensioni della chiave sono maggiori o uguali a 512 ma minori o uguali a 1024 bit, usare la struttura [**\_ BCRYPT DSA \_ PARAMETER \_ HEADER.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dsa_parameter_header)


</dt> </dl> </dd> <dt>

<span id="BCRYPT_EFFECTIVE_KEY_LENGTH"></span><span id="bcrypt_effective_key_length"></span>**LUNGHEZZA \_ EFFETTIVA \_ DELLA CHIAVE \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"EffectiveKeyLength"
</dt> <dt>



Dimensione, in bit, della lunghezza effettiva di una chiave RC2. Questo tipo di dati è **un valore DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_BLOCK_LENGTH"></span><span id="bcrypt_hash_block_length"></span>**LUNGHEZZA BLOCCO \_ HASH \_ \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"HashBlockLength"
</dt> <dt>



Dimensione, in byte, del blocco per un hash. Questa proprietà si applica solo agli algoritmi hash. Questo tipo di dati è **un valore DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_LENGTH"></span><span id="bcrypt_hash_length"></span>**LUNGHEZZA \_ HASH \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"HashDigestLength"
</dt> <dt>



Dimensione, in byte, del valore hash di un provider hash. Questo tipo di dati è **un valore DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_HASH_OID_LIST"></span><span id="bcrypt_hash_oid_list"></span>**ELENCO \_ \_ DI OID HASH BCRYPT \_**
</dt> <dd> <dl> <dt>

L"HashOIDList"
</dt> <dt>



Elenco di identificatori di oggetto hash [*con*](/windows/desktop/SecGloss/o-gly) codifica [*DER*](/windows/desktop/SecGloss/d-gly)(OID). Questa proprietà è una [**struttura \_ BCRYPT OID \_ LIST.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_oid_list) Questa proprietà può essere letta solo.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_INITIALIZATION_VECTOR"></span><span id="bcrypt_initialization_vector"></span>**VETTORE DI INIZIALIZZAZIONE BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"IV"
</dt> <dt>



Contiene il [*vettore di inizializzazione*](/windows/desktop/SecGloss/i-gly) (IV) per una chiave. Questa proprietà si applica solo alle chiavi.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTH"></span><span id="bcrypt_key_length"></span>**LUNGHEZZA CHIAVE \_ \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"KeyLength"
</dt> <dt>



Dimensione, in bit, del valore della chiave di un provider di chiavi simmetriche. Questo tipo di dati è **un valore DWORD**.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_LENGTHS"></span><span id="bcrypt_key_lengths"></span>**LUNGHEZZE \_ DELLE \_ CHIAVI BCRYPT**
</dt> <dd> <dl> <dt>

L"KeyLengths"
</dt> <dt>



Lunghezze delle chiavi supportate dall'algoritmo. Questa proprietà è una [**struttura STRUCT BCRYPT \_ KEY \_ LENGTHS. \_**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_key_lengths_struct) Questa proprietà si applica solo agli algoritmi.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_OBJECT_LENGTH"></span><span id="bcrypt_key_object_length"></span>**LUNGHEZZA \_ DELL'OGGETTO \_ CHIAVE \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"KeyObjectLength"
</dt> <dt>



Questa proprietà non viene utilizzata. La **proprietà BCRYPT \_ OBJECT \_ LENGTH** viene usata per ottenere queste informazioni.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_KEY_STRENGTH"></span><span id="bcrypt_key_strength"></span>**COMPLESSITÀ DELLA CHIAVE BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"KeyStrength"
</dt> <dt>



Numero di bit nella chiave. Questo tipo di dati è **un valore DWORD**. Questa proprietà si applica solo alle chiavi.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MESSAGE_BLOCK_LENGTH"></span><span id="bcrypt_message_block_length"></span>**LUNGHEZZA BLOCCO \_ MESSAGGI \_ \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"MessageBlockLength"
</dt> <dt>



Può essere impostato su qualsiasi handle di chiave con la modalità di concatenamento CFB impostata. Per impostazione predefinita, questa proprietà è impostata su 1 per CFB a 8 bit. L'impostazione della proprietà sulla dimensione in byte del blocco causa l'uso di CFB a blocchi completi. Per le chiavi XTS viene usato per impostare le dimensioni, in byte, dell'unità dati XTS (in genere 512 o 4096).


</dt> </dl> </dd> <dt>

<span id="BCRYPT_MULTI_OBJECT_LENGTH"></span><span id="bcrypt_multi_object_length"></span>**LUNGHEZZA DI \_ PIÙ \_ \_ OGGETTI BCRYPT**
</dt> <dd> <dl> <dt>

L"MultiObjectLength"
</dt> <dt>



Questa proprietà restituisce uno [**\_ \_ \_ \_ STRUCT BCRYPT MULTI OBJECT LENGTH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_multi_object_length_struct)che contiene le informazioni necessarie per calcolare le dimensioni di un buffer di oggetti. Questa proprietà è supportata solo nelle versioni del sistema operativo che supportano la [**funzione BCryptCreateMultiHash.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatemultihash)


</dt> </dl> </dd> <dt>

<span id="BCRYPT_OBJECT_LENGTH"></span><span id="bcrypt_object_length"></span>**LUNGHEZZA \_ DELL'OGGETTO \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"ObjectLength"
</dt> <dt>



Dimensione, in byte, del sottooggetto di un provider. Questo tipo di dati è **un valore DWORD**. Attualmente, i provider di algoritmi di crittografia simmetrica e hash usano buffer allocati dal chiamante per archiviare i relativi sottooggetti. Ad esempio, il provider hash richiede di allocare memoria per l'oggetto hash ottenuto con la [**funzione BCryptCreateHash.**](/windows/desktop/api/Bcrypt/nf-bcrypt-bcryptcreatehash) Questa proprietà fornisce le dimensioni del buffer per l'oggetto di un provider in modo che sia possibile allocare memoria per l'oggetto creato dal provider.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PADDING_SCHEMES"></span><span id="bcrypt_padding_schemes"></span>**SCHEMI DI RIEMPIMENTO BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"PaddingSchemes"
</dt> <dt>



Rappresenta lo schema di spaziatura interna del provider di algoritmi RSA. Questo tipo di dati è **un valore DWORD**. Può essere uno dei valori seguenti.



| Identificatore                             | Valore      | Descrizione                                                |
|----------------------------------------|------------|------------------------------------------------------------|
| **ROUTER DI \_ PAD \_ SUPPORTATO DA \_ BCRYPT**     | 0x00000001 | Il provider supporta la spaziatura interna aggiunta dal router.         |
| **ENC \_ \_ PKCS1 DEL PAD \_ SUPPORTATO DA \_ BCRYPT** | 0x00000002 | Il provider supporta lo schema di riempimento della crittografia PKCS1. |
| **BCRYPT \_ SUPPORTATO \_ PAD \_ PKCS1 \_ SIG** | 0x00000004 | Il provider supporta lo schema di riempimento della firma PKCS1.  |
| **BCRYPT \_ SUPPORTATO DA PAD \_ \_ OAEP**       | 0x00000008 | Il provider supporta lo schema di riempimento OAEP.             |
| **BCRYPT \_ SUPPORTATO DA PAD \_ \_ PSS**        | 0x00000010 | Il provider supporta lo schema di riempimento PSS.              |



 


</dt> </dl> </dd> <dt>

<span id="BCRYPT_PROVIDER_HANDLE"></span><span id="bcrypt_provider_handle"></span>**HANDLE DEL PROVIDER BCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"ProviderHandle"
</dt> <dt>



Handle del provider CNG che ha creato l'oggetto passato nel *parametro hObject.* Questo tipo di dati è **BCRYPT \_ ALG \_ HANDLE**. Questa proprietà può essere recuperata solo. non può essere impostato.


</dt> </dl> </dd> <dt>

<span id="BCRYPT_SIGNATURE_LENGTH"></span><span id="bcrypt_signature_length"></span>**LUNGHEZZA \_ DELLA FIRMA \_ BCRYPT**
</dt> <dd> <dl> <dt>

L"SignatureLength"
</dt> <dt>



Dimensione, in byte, della lunghezza di una firma per una chiave. Questo tipo di dati è **un valore DWORD**. Questa proprietà si applica solo alle chiavi. Questa proprietà può essere recuperata solo. non può essere impostato.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Bcrypt.h</dt> </dl> |



 

