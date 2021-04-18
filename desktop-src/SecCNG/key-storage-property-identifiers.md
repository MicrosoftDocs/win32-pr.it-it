---
description: Utilizzato per identificare una proprietà di archiviazione delle chiavi.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Identificatori di proprietà di archiviazione chiavi (ncrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 813a15ba106989cb558eba181bc893d75c6d1bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319389"
---
# <a name="key-storage-property-identifiers"></a>Identificatori delle proprietà di archiviazione chiavi

Per identificare una proprietà di archiviazione delle chiavi vengono usati i valori seguenti.

<dl> <dt>

<span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**\_proprietà del \_ gruppo di algoritmi NCRYPT \_**
</dt> <dd> <dl> <dt>

L "gruppo di algoritmi"
</dt> <dt>



Stringa Unicode con terminazione null che contiene il nome del gruppo di algoritmi dell'oggetto. Questa proprietà si applica solo alle chiavi. Il provider di archiviazione chiavi Microsoft restituisce gli identificatori seguenti.



| Identificatore                                     | Valore              | Descrizione                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| **\_gruppo di \_ algoritmi \_ RSA NCRYPT**<br/>   | RSA<br/>   | Gruppo di algoritmi RSA.<br/>                           |
| **\_gruppo di \_ algoritmi NCRYPT DH \_**<br/>    | DH<br/>    | Gruppo di algoritmi di Diffie-Hellman.<br/>                |
| **\_gruppo di \_ algoritmi NCRYPT DSA \_**<br/>   | DSA<br/>   | Gruppo di algoritmi DSA.<br/>                           |
| **\_gruppo di \_ algoritmi NCRYPT ECDSA \_**<br/> | ECDSA<br/> | Gruppo di algoritmi DSA a curva ellittica.<br/>            |
| **\_gruppo di \_ algoritmi NCRYPT ECDH \_**<br/>  | ECDH<br/>  | La curva ellittica Diffie-Hellman gruppo di algoritmi.<br/> |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**\_proprietà dell'algoritmo NCRYPT \_**
</dt> <dd> <dl> <dt>

L "Nome algoritmo"
</dt> <dt>



Stringa Unicode con terminazione null che contiene il nome dell'algoritmo dell'oggetto. Può trattarsi di uno degli [**identificatori di algoritmo CNG**](cng-algorithm-identifiers.md) predefiniti o di un altro identificatore dell'algoritmo registrato. Questa proprietà si applica solo alle chiavi.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**\_ \_ chiave ECDH associata \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "SmartCardAssociatedECDHKey"
</dt> <dt>



Valore **LPWSTR** che indica il nome del contenitore della chiave ellittica Diffie-Hellman (ECDH) da utilizzare durante l'accesso per un handle specificato a una chiave ECDSA (Digital Signature Algorithm) a curva ellittica. Se non sono presenti chiavi di ECDH sulla scheda, il [*provider di archiviazione chiavi*](/windows/desktop/SecGloss/k-gly) (KSP) restituisce **nte \_ non \_ trovato**. Questa proprietà si applica alle chiavi di ECDSA per l'accesso con smart card. La proprietà è supportata dal provider di archiviazione chiavi per Smart Card Microsoft e non dal provider di archiviazione chiavi software Microsoft.

**Windows Server 2008 e Windows Vista:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**\_ \_ proprietà Lunghezza blocco \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "lunghezza del blocco"
</dt> <dt>



**Valore DWORD** che contiene la lunghezza, in byte, del blocco di crittografia. Questa proprietà si applica solo alle chiavi che supportano la crittografia.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**\_proprietà del certificato NCRYPT \_**
</dt> <dd> <dl> <dt>

L "SmartCardKeyCertificate"
</dt> <dt>



Un [*BLOB*](/windows/desktop/SecGloss/b-gly) che contiene un certificato X. 509 associato alla chiave.

**Windows server 2008 R2, Windows 7, Windows server 2008 e Windows Vista:** [*BLOB*](/windows/desktop/SecGloss/b-gly) contenente il [*certificato*](/windows/desktop/SecGloss/c-gly)della chiave della [*Smart Card*](/windows/desktop/SecGloss/s-gly) . Questa proprietà non è supportata dal provider di archiviazione chiavi del software Microsoft.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**\_ \_ Proprietà parametri DH \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "DHParameters"
</dt> <dt>



Specifica i parametri da utilizzare con una chiave Diffie-Hellman. Questo tipo di dati è un puntatore a una struttura di [**\_ intestazione del \_ parametro \_ BCRYPT DH**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) . Questa proprietà può essere impostata solo e deve essere impostata per la chiave prima del completamento della chiave.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**\_proprietà dei \_ criteri di esportazione NCRYPT \_**
</dt> <dd> <dl> <dt>

L "Esporta criteri"
</dt> <dt>



**Valore DWORD** che contiene un set di flag che specificano i criteri di esportazione per una chiave permanente. Questa proprietà si applica solo alle chiavi. Può contenere zero o una combinazione di uno o più dei valori seguenti.



| Identificatore                                    | Valore      | Descrizione                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_flag NCRYPT Consenti \_ esportazione \_**               | 0x00000001 | La chiave privata può essere esportata.                                                                                                                                                                                                                                                                                 |
| **NCRYPT \_ Consenti \_ \_ flag di esportazione testo non crittografato \_**    | 0x00000002 | La chiave privata può essere esportata in formato testo normale.                                                                                                                                                                                                                                                               |
| **NCRYPT \_ consente il \_ flag di archiviazione \_**            | 0x00000004 | La chiave privata può essere esportata una sola volta a scopo di archiviazione. Questo flag si applica solo all'handle di chiave originale su cui è impostato. Questo criterio può essere applicato solo all'handle di chiave originale. Dopo la chiusura dell'handle di chiave, la chiave non può più essere esportata a scopo di archiviazione.                   |
| **NCRYPT \_ consente \_ un \_ flag di archiviazione in testo non crittografato \_** | 0x00000008 | La chiave privata può essere esportata una sola volta in formato testo non crittografato a scopo di archiviazione. Questo flag si applica solo all'handle di chiave originale su cui è impostato. Questo criterio può essere applicato solo all'handle di chiave originale. Dopo la chiusura dell'handle di chiave, la chiave non può più essere esportata a scopo di archiviazione. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**\_proprietà di \_ tipo \_ impl di NCRYPT**
</dt> <dd> <dl> <dt>

L "tipo di impl"
</dt> <dt>



**Valore DWORD** che contiene un set di flag che definiscono i dettagli di implementazione del provider. Questa proprietà si applica solo ai provider di archiviazione chiavi. Può contenere zero o una combinazione di uno o più dei valori seguenti.



| Identificatore                            | Valore      | Descrizione                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| **\_ \_ flag hardware NCRYPT \_ impl**      | 0x00000001 | Il provider è basato su hardware.                           |
| **\_ \_ flag software NCRYPT \_ impl**      | 0x00000002 | Il provider è basato su software.                           |
| **\_ \_ flag rimovibile impl NCRYPT \_**     | 0x00000008 | Il provider è rimovibile.                                |
| **\_ \_ \_ flag RNG hardware NCRYPT \_ impl** | 0x00000010 | Il provider è un generatore di numeri casuali basato su hardware. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**\_proprietà del \_ tipo di chiave NCRYPT \_**
</dt> <dd> <dl> <dt>

L "tipo di chiave"
</dt> <dt>



**Valore DWORD** che contiene un set di flag che definiscono il tipo di chiave. Questa proprietà si applica solo alle chiavi. Può contenere zero o il valore seguente.



| Identificatore                     | Valore      | Descrizione                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| **\_ \_ flag chiave del computer NCRYPT \_** | 0x00000001 | La chiave si applica al computer locale. Se questo flag non è presente, la chiave si applica all'utente corrente. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**\_ \_ Proprietà utilizzo chiavi \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "utilizzo chiave"
</dt> <dt>



**DWORD** che contiene un set di flag che definiscono i dettagli di utilizzo per una chiave. Questa proprietà si applica solo alle chiavi. Può contenere zero o una combinazione di uno o più dei valori seguenti.



| Identificatore                              | Valore      | Descrizione                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| **NCRYPT \_ Consenti \_ flag di decrittografia \_**        | 0x00000001 | La chiave può essere usata per la decrittografia.                  |
| **NCRYPT \_ Consenti \_ flag di firma \_**        | 0x00000002 | La chiave può essere usata per la firma.                     |
| **NCRYPT \_ il \_ \_ flag di accettazione del tasto \_** | 0x00000004 | La chiave può essere utilizzata per la crittografia dei contratti di segreto. |
| **NCRYPT \_ consente \_ tutti gli \_ utilizzi**          | 0x00FFFFFF | La chiave può essere usata per qualsiasi scopo.                 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**NCRYPT \_ Ultima \_ \_ proprietà modificata**
</dt> <dd> <dl> <dt>

L "modificato"
</dt> <dt>



Indica la data dell'Ultima modifica apportata alla chiave. Questo tipo di dati è un puntatore a una struttura [**FILETIME**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) . Questa proprietà si applica solo alle chiavi salvate in modo permanente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**\_proprietà Length di NCRYPT \_**
</dt> <dd> <dl> <dt>

L "lunghezza"
</dt> <dt>



**Valore DWORD** che contiene la lunghezza, in bit, della chiave. Questa proprietà si applica solo alle chiavi.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**\_Proprietà lunghezze NCRYPT \_**
</dt> <dd> <dl> <dt>

L "lunghezze"
</dt> <dt>



Indica le dimensioni delle chiavi supportate dalla chiave. Questo tipo di dati è un puntatore a una struttura di [**\_ \_ lunghezza supportata da NCRYPT**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) che contiene queste informazioni. Questa proprietà si applica solo alle chiavi.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**\_ \_ \_ proprietà lunghezza max nome \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "lunghezza massima del nome"
</dt> <dt>



**Valore DWORD** che contiene la lunghezza massima, in caratteri, del nome di una chiave persistente. Questa proprietà si applica solo a un provider.

Questa proprietà è destinata principalmente a essere usata dai provider di archiviazione chiavi che archiviano le chiavi in un dispositivo con una quantità limitata di memoria disponibile, ad esempio una smart card.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**\_proprietà Name di NCRYPT \_**
</dt> <dd> <dl> <dt>

L "nome"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione null che contiene il nome dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**\_ \_ proprietà richiesta PIN \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "SmartCardPinPrompt"
</dt> <dt>



Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**\_Proprietà pin \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "SmartCardPin"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione null che contiene il PIN. Il PIN viene usato per una chiave della smart card o la password per una chiave protetta da password archiviata in un provider di archiviazione chiavi basato su software. Questa proprietà può essere impostata solo. Microsoft KSP memorizza nella cache questo valore in modo che l'utente venga richiesto una sola volta per processo.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**\_ \_ proprietà Handle provider \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "handle del provider"
</dt> <dt>



**Handle NCRYPT \_ prova \_** contenente l'handle del provider di archiviazione chiavi CNG. Al termine dell'utilizzo dell'handle, è necessario chiamare [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) per rilasciarlo.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**\_Proprietà Reader \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "SmartCardReader"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione null che contiene il nome del lettore di smart card. Questa proprietà può essere impostata solo.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**\_ \_ Proprietà CERTSTORE radice \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "SmartcardRootCertStore"
</dt> <dt>



Oggetto **HCERTSTORE** che rappresenta l'archivio certificati radice della smart card.


</dt> </dl> </dd> <dt>

<span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ \_ \_ ID pin spaventato**
</dt> <dd> <dl> <dt>

L "SmartCardPinId"
</dt> <dt>



Puntatore al valore dell' **\_ ID pin** associato a una [*chiave crittografica*](/windows/desktop/SecGloss/c-gly) specificata in una [*Smart Card*](/windows/desktop/SecGloss/s-gly). Questa proprietà è di sola lettura. Il tipo di dati **pin \_ ID** è definito in cardmod. h.

**Windows Server 2008 e Windows Vista:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**\_ \_ informazioni sul pin spaventato \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "SmartCardPinInfo"
</dt> <dt>



Puntatore per aggiungere la struttura di [**\_ informazioni**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) del PIN associato a una chiave crittografica specificata nella smart card. Il chiamante fornisce l'handle di chiave. Questa proprietà è una proprietà di sola lettura. La struttura delle **\_ informazioni sul pin** è definita in cardmod. h.

**Windows Server 2008 e Windows Vista:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**\_Proprietà NCRYPT Secure \_ pin \_**
</dt> <dd> <dl> <dt>

L "SmartCardSecurePin"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione null che contiene il PIN della sessione della smart card. Questa proprietà può essere impostata solo.

**Windows Vista:** Questa proprietà non è supportata.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**\_ \_ Proprietà descr NCRYPT \_ Security**
</dt> <dd> <dl> <dt>

L "descr di sicurezza"
</dt> <dt>



Puntatore a una struttura [**di \_ descrittori di sicurezza**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che contiene informazioni sul controllo di accesso per la chiave. Questa proprietà si applica solo alle chiavi permanenti. Il parametro *dwFlags* della funzione [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) o [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) identifica la parte del descrittore di sicurezza da ottenere o impostare.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**Proprietà di supporto di NCRYPT \_ Security \_ Descr \_ \_**
</dt> <dd> <dl> <dt>

L "supporto del descr di sicurezza"
</dt> <dt>



Indica se il provider supporta i descrittori di sicurezza per le chiavi. Questa proprietà è un **valore DWORD** che contiene 1 se il provider supporta descrittori di sicurezza per le chiavi. Se questa proprietà contiene qualsiasi altro valore o se la funzione [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) restituisce **nte \_ non \_ supportata**, il provider non supporta i descrittori di sicurezza per le chiavi. Questa proprietà si applica solo ai provider.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**\_proprietà GUID Smart Card NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "SmartCardGuid"
</dt> <dt>



BLOB contenente l'identificatore della smart card.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**\_proprietà dei \_ criteri dell'interfaccia utente di NCRYPT \_**
</dt> <dd> <dl> <dt>

L "criteri dell'interfaccia utente"
</dt> <dt>



Se usato con la funzione [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) o [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) , si tratta di un puntatore a una struttura di [**\_ \_ criteri dell'**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) interfaccia utente NCRYPT che contiene i criteri di interfaccia utente chiave avanzata per la chiave. Questa proprietà si applica solo alle chiavi permanenti. Questa proprietà può essere impostata solo al momento della generazione della chiave. Una volta chiamata la funzione [**NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) per questa chiave, questa proprietà diventa di sola lettura.

Un provider di archiviazione chiavi può ricevere questo parametro tramite una funzione di callback [**NCryptSetPropertyFn**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) . Il valore del parametro è una \_ \_ struttura BLOB di criteri dell'interfaccia utente NCRYPT \_ che contiene le stesse informazioni. Analogamente, quando un'applicazione effettua una richiesta tramite NCryptSetPropertyFn al provider per restituire questa proprietà, è previsto che il provider restituisca una \_ struttura del BLOB dei criteri dell'interfaccia utente di NCRYPT \_ \_ .


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**\_ \_ proprietà nome univoco \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "nome univoco"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione null che contiene il nome univoco dell'oggetto. Si tratta di un nome alternativo che può essere usato per accedere alla chiave. Questa proprietà viene usata quando si pensa che il nome della chiave passato in origine a [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) non sia sufficiente per identificare in modo affidabile la chiave salvata in modo permanente. Il provider di archiviazione chiavi Microsoft restituirà il nome del file della chiave come questa proprietà.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**NCRYPT \_ utilizzare \_ la \_ proprietà di contesto**
</dt> <dd> <dl> <dt>

L "USA contesto"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione null che descrive il contesto dell'operazione. Questa proprietà non è persistente e può essere impostata su un provider o una chiave. Una chiave non ha accesso alla proprietà della **\_ proprietà di \_ contesto \_ use NCRYPT** del provider perché la proprietà è specifica solo per l'handle per cui è impostata.

Un esempio in cui questa proprietà verrebbe usata nel contesto di un provider è un provider di archiviazione chiavi che deve richiedere all'utente durante una chiamata a [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (ad esempio, "inserire la smart card nel lettore"). Poiché l'handle di chiave non è disponibile fino a quando **NCryptOpenKey** non restituisce, l'applicazione deve impostare questa proprietà sull'handle del provider prima di chiamare **NCryptOpenKey**.

Un esempio in cui questa proprietà verrebbe usata nel contesto di un handle di chiave è un provider di archiviazione chiavi che deve richiedere all'utente durante un'operazione usando la chiave (ad esempio, "questa applicazione deve usare questa chiave per firmare un documento"). Il provider potrebbe quindi inoltrare queste informazioni di contesto all'utente in qualsiasi interfaccia utente visualizzata durante l'operazione.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**\_Proprietà NCRYPT use \_ Count \_ Enabled \_**
</dt> <dd> <dl> <dt>

L "numero di utilizzi abilitati"
</dt> <dt>



Indica se il provider supporta il conteggio dell'utilizzo per le chiavi. Questa proprietà è un **valore DWORD** che contiene 1 se il provider supporta il conteggio dell'utilizzo per le chiavi. Se questa proprietà contiene qualsiasi altro valore o se la funzione [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) restituisce **nte \_ non \_ supportata**, il provider non supporta il conteggio dell'utilizzo per le chiavi. Questa proprietà si applica solo ai provider.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**\_ \_ Proprietà conteggio utilizzo \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "conteggio utilizzo"
</dt> <dt>



Variabile [**di \_ tipo Integer ULARGE**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) che contiene il numero di operazioni eseguite dalla [*chiave privata*](/windows/desktop/SecGloss/p-gly) specificata. Questa proprietà è facoltativa e potrebbe non essere supportata da tutti i provider. I provider che supportano questa proprietà nelle chiavi devono supportare anche la proprietà della **\_ Proprietà NCRYPT use \_ Count \_ Enabled \_** nell'handle del provider. Il provider di archiviazione chiavi Microsoft non supporta questa proprietà. Questa proprietà si applica solo alle chiavi permanenti.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**\_Proprietà CERTSTORE dell'utente NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L "SmartCardUserCertStore"
</dt> <dt>



Oggetto **HCERTSTORE** che rappresenta l'archivio certificati utente della smart card.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**\_proprietà della versione NCRYPT \_**
</dt> <dd> <dl> <dt>

L "versione"
</dt> <dt>



**Valore DWORD** che contiene la versione software del provider. La parola alta contiene la versione principale e la parola bassa contiene la versione secondaria. Ad esempio, 0x00030033 = 3,51. Questa proprietà si applica solo ai provider.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**\_ \_ Proprietà handle finestra \_ NCRYPT**
</dt> <dd> <dl> <dt>

L "handle HWND"
</dt> <dt>



Puntatore all'handle della finestra (**HWND**) da utilizzare come elemento padre di qualsiasi interfaccia utente visualizzata.

Poiché è possibile che si verifichi un comportamento indesiderato quando un'interfaccia utente viene visualizzata utilizzando un handle di finestra **null** per l'elemento padre, è consigliabile che un provider di archiviazione chiavi non visualizzi un'interfaccia utente a meno che questa proprietà non sia impostata.


</dt> </dl> </dd> </dl>

I valori seguenti vengono utilizzati per definire i limiti dei dati della proprietà.



| Costante/valore                                                                                                                                                                                                                                                 | Descrizione                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <dt>**NCRYPT \_ Numero \_ massimo \_**</dt> di <dt>0x100000</dt> dati della proprietà </dl> | Specifica la dimensione massima in byte del valore di una proprietà.<br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <dt>**NCRYPT \_ \_ \_ Nome di proprietà Max**</dt> <dt>64</dt> </dl>       | Specifica la dimensione massima del nome di una proprietà, in caratteri.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>                                      |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Ncrypt. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

