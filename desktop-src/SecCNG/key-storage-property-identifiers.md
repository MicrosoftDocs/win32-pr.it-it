---
description: Usato per identificare una proprietà di archiviazione delle chiavi.
ms.assetid: 407f0e42-07c8-4ec6-81c6-f8bde005adb0
title: Identificatori Archiviazione proprietà chiave (Ncrypt.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20b8fca27591837a555e4f75040ba16056c42e16ce488c0bb99f2d8f7de70bd1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118907616"
---
# <a name="key-storage-property-identifiers"></a>Identificatori di Archiviazione chiave

I valori seguenti vengono usati per identificare una proprietà di archiviazione delle chiavi.

<dl> <dt>

<span id="NCRYPT_ALGORITHM_GROUP_PROPERTY"></span><span id="ncrypt_algorithm_group_property"></span>**PROPRIETÀ DEL GRUPPO \_ DI \_ ALGORITMI \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Gruppo di algoritmi"
</dt> <dt>



Stringa Unicode con terminazione Null contenente il nome del gruppo di algoritmi dell'oggetto. Questa proprietà si applica solo alle chiavi. Gli identificatori seguenti vengono restituiti dal provider di archiviazione chiavi Microsoft.



| Identificatore                                     | Valore              | Descrizione                                                   |
|------------------------------------------------|--------------------|---------------------------------------------------------------|
| **GRUPPO DI \_ ALGORITMI NCRYPT \_ \_ RSA**<br/>   | "RSA"<br/>   | Gruppo di algoritmi RSA.<br/>                           |
| **GRUPPO DI ALGORITMI \_ NCRYPT DH \_ \_**<br/>    | "DH"<br/>    | Gruppo Diffie-Hellman algoritmo.<br/>                |
| **GRUPPO DI \_ ALGORITMI DSA NCRYPT \_ \_**<br/>   | "DSA"<br/>   | Gruppo di algoritmi DSA.<br/>                           |
| **GRUPPO DI ALGORITMI \_ NCRYPT ECDSA \_ \_**<br/> | "ECDSA"<br/> | Gruppo di algoritmi DSA a curva ellittica.<br/>            |
| **GRUPPO DI \_ ALGORITMI NCRYPT ECDH \_ \_**<br/>  | "ECDH"<br/>  | La curva ellittica Diffie-Hellman algoritmo.<br/> |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ALGORITHM_PROPERTY"></span><span id="ncrypt_algorithm_property"></span>**PROPRIETÀ \_ ALGORITMO \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Nome algoritmo"
</dt> <dt>



Stringa Unicode con terminazione Null che contiene il nome dell'algoritmo dell'oggetto. Può trattarsi di uno degli identificatori di algoritmo [**CNG predefiniti o**](cng-algorithm-identifiers.md) di un altro identificatore di algoritmo registrato. Questa proprietà si applica solo alle chiavi.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ASSOCIATED_ECDH_KEY"></span><span id="ncrypt_associated_ecdh_key"></span>**CHIAVE \_ \_ ECDH ASSOCIATA \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"SmartCardAssociatedECDHKey"
</dt> <dt>



Valore **LPWSTR** che indica il nome del contenitore della chiave ECDH (Elliptic Curve Diffie-Hellman) da usare durante l'accesso per un handle specificato a una chiave ECDSA (Elliptic Curve Digital Signature Algorithm). Se nella scheda non sono presenti chiavi ECDH, il provider di [*archiviazione chiavi*](/windows/desktop/SecGloss/k-gly) (KSP) restituisce **NTE NOT \_ \_ FOUND**. Questa proprietà si applica alle chiavi ECDSA per l'accesso con smart card. La proprietà è supportata dal provider di archiviazione chiavi smart card Microsoft e non dal provider di archiviazione chiavi del software Microsoft.

**Windows Server 2008 e Windows Vista:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_BLOCK_LENGTH_PROPERTY"></span><span id="ncrypt_block_length_property"></span>**PROPRIETÀ LUNGHEZZA \_ \_ BLOCCO \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Lunghezza blocco"
</dt> <dt>



Valore **DWORD** che contiene la lunghezza, in byte, del blocco di crittografia. Questa proprietà si applica solo alle chiavi che supportano la crittografia.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_CERTIFICATE_PROPERTY"></span><span id="ncrypt_certificate_property"></span>**PROPRIETÀ \_ DEL CERTIFICATO \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"SmartCardKeyCertificate"
</dt> <dt>



BLOB [](/windows/desktop/SecGloss/b-gly) che contiene un certificato X.509 associato alla chiave.

**Windows Server 2008 R2, Windows 7, Windows Server 2008 e Windows Vista:** BLOB [*che*](/windows/desktop/SecGloss/b-gly) contiene il certificato [*smart card*](/windows/desktop/SecGloss/s-gly) [*chiave.*](/windows/desktop/SecGloss/c-gly) Questa proprietà non è supportata da Microsoft Software Key Archiviazione Provider.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DH_PARAMETERS_PROPERTY"></span><span id="ncrypt_dh_parameters_property"></span>**PROPRIETÀ DEI \_ PARAMETRI DH \_ \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"DHParameters"
</dt> <dt>



Specifica i parametri da usare con una Diffie-Hellman chiave. Questo tipo di dati è un puntatore a una [**struttura \_ BCRYPT DH \_ PARAMETER \_ HEADER.**](/windows/desktop/api/Bcrypt/ns-bcrypt-bcrypt_dh_parameter_header) Questa proprietà può essere impostata solo e deve essere impostata per la chiave prima del completamento della chiave.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_EXPORT_POLICY_PROPERTY"></span><span id="ncrypt_export_policy_property"></span>**PROPRIETÀ DEI \_ CRITERI DI \_ ESPORTAZIONE \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Export Policy"
</dt> <dt>



Valore **DWORD che** contiene un set di flag che specificano i criteri di esportazione per una chiave persistente. Questa proprietà si applica solo alle chiavi. Può contenere zero o una combinazione di uno o più dei valori seguenti.



| Identificatore                                    | Valore      | Descrizione                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------|------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **FLAG DI ESPORTAZIONE CONSENTI NCRYPT \_ \_ \_**               | 0x00000001 | La chiave privata può essere esportata.                                                                                                                                                                                                                                                                                 |
| **NCRYPT \_ - CONSENTI FLAG DI ESPORTAZIONE TESTO NON \_ \_ \_ CRITTOGRAFATO**    | 0x00000002 | La chiave privata può essere esportata in formato testo non crittografato.                                                                                                                                                                                                                                                               |
| **FLAG DI ARCHIVIAZIONE CONSENTI NCRYPT \_ \_ \_**            | 0x00000004 | La chiave privata può essere esportata una sola volta ai fini dell'archiviazione. Questo flag si applica solo all'handle di chiave originale su cui è impostato. Questo criterio può essere applicato solo all'handle di chiave originale. Dopo la chiusura dell'handle di chiave, la chiave non può più essere esportata a scopo di archiviazione.                   |
| **NCRYPT \_ - CONSENTI FLAG DI ARCHIVIAZIONE TESTO NON \_ \_ \_ CRITTOGRAFATO** | 0x00000008 | La chiave privata può essere esportata una sola volta in testo non crittografato a scopo di archiviazione. Questo flag si applica solo all'handle di chiave originale su cui è impostato. Questo criterio può essere applicato solo all'handle di chiave originale. Dopo la chiusura dell'handle di chiave, la chiave non può più essere esportata a scopo di archiviazione. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_IMPL_TYPE_PROPERTY"></span><span id="ncrypt_impl_type_property"></span>**PROPRIETÀ \_ DI TIPO IMPL \_ \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Tipo Impl"
</dt> <dt>



Valore **DWORD che** contiene un set di flag che definiscono i dettagli di implementazione del provider. Questa proprietà si applica solo ai provider di archiviazione chiavi. Può contenere zero o una combinazione di uno o più dei valori seguenti.



| Identificatore                            | Valore      | Descrizione                                               |
|---------------------------------------|------------|-----------------------------------------------------------|
| **NCRYPT \_ IMPL \_ HARDWARE \_ FLAG**      | 0x00000001 | Il provider è basato su hardware.                           |
| **NCRYPT \_ IMPL \_ SOFTWARE \_ FLAG**      | 0x00000002 | Il provider è basato su software.                           |
| **FLAG \_ RIMOVIBILE NCRYPT IMPL \_ \_**     | 0x00000008 | Il provider è rimovibile.                                |
| **NCRYPT \_ IMPL \_ HARDWARE \_ RNG \_ FLAG** | 0x00000010 | Il provider è un generatore di numeri casuali basato su hardware. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_TYPE_PROPERTY"></span><span id="ncrypt_key_type_property"></span>**PROPRIETÀ DEL \_ TIPO \_ DI CHIAVE \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Tipo di chiave"
</dt> <dt>



Valore **DWORD che** contiene un set di flag che definiscono il tipo di chiave. Questa proprietà si applica solo alle chiavi. Può contenere zero o il valore seguente.



| Identificatore                     | Valore      | Descrizione                                                                                              |
|--------------------------------|------------|----------------------------------------------------------------------------------------------------------|
| **FLAG DELLA \_ CHIAVE DEL \_ COMPUTER NCRYPT \_** | 0x00000001 | La chiave si applica al computer locale. Se questo flag non è presente, la chiave viene applicata all'utente corrente. |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_USAGE_PROPERTY"></span><span id="ncrypt_key_usage_property"></span>**PROPRIETÀ DI \_ UTILIZZO \_ DELLA CHIAVE \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Utilizzo chiavi"
</dt> <dt>



Valore **DWORD che** contiene un set di flag che definiscono i dettagli di utilizzo per una chiave. Questa proprietà si applica solo alle chiavi. Può contenere zero o una combinazione di uno o più dei valori seguenti.



| Identificatore                              | Valore      | Descrizione                                          |
|-----------------------------------------|------------|------------------------------------------------------|
| **FLAG DI \_ DECRITTOGRAFIA CONSENTI NCRYPT \_ \_**        | 0x00000001 | La chiave può essere usata per la decrittografia.                  |
| **FLAG DI FIRMA CONSENTI NCRYPT \_ \_ \_**        | 0x00000002 | La chiave può essere usata per la firma.                     |
| **FLAG DI \_ CONSENSO \_ CHIAVE \_ NCRYPT \_** | 0x00000004 | La chiave può essere usata per la crittografia del contratto segreto. |
| **NCRYPT \_ - CONSENTI TUTTI GLI \_ \_ UTILIZZI**          | 0x00ffffff | La chiave può essere usata per qualsiasi scopo.                 |



 


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LAST_MODIFIED_PROPERTY"></span><span id="ncrypt_last_modified_property"></span>**PROPRIETÀ \_ DELL'ULTIMA \_ MODIFICA DI \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Modificato"
</dt> <dt>



Indica l'ultima modifica della chiave. Questo tipo di dati è un puntatore a una [**struttura FILETIME.**](/windows/desktop/api/minwinbase/ns-minwinbase-filetime) Questa proprietà si applica solo alle chiavi persistenti.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTH_PROPERTY"></span><span id="ncrypt_length_property"></span>**PROPRIETÀ \_ LENGTH DI \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Length"
</dt> <dt>



Valore **DWORD** che contiene la lunghezza, in bit, della chiave. Questa proprietà si applica solo alle chiavi.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_LENGTHS_PROPERTY"></span><span id="ncrypt_lengths_property"></span>**PROPRIETÀ \_ LENGTHS DI \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Lunghezze"
</dt> <dt>



Indica le dimensioni delle chiavi supportate dalla chiave. Questo tipo di dati è un puntatore a una [**struttura NCRYPT \_ SUPPORTED \_ LENGTHS**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_supported_lengths) che contiene queste informazioni. Questa proprietà si applica solo alle chiavi.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_MAX_NAME_LENGTH_PROPERTY"></span><span id="ncrypt_max_name_length_property"></span>**PROPRIETÀ NCRYPT \_ MAX \_ NAME \_ LENGTH \_**
</dt> <dd> <dl> <dt>

L"Max Name Length"
</dt> <dt>



Valore **DWORD** che contiene la lunghezza massima, in caratteri, del nome di una chiave persistente. Questa proprietà si applica solo a un provider.

Questa proprietà è destinata principalmente all'uso da parte dei provider di archiviazione chiavi che archiviano le chiavi in un dispositivo con una quantità limitata di memoria disponibile, ad esempio un smart card.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_NAME_PROPERTY"></span><span id="ncrypt_name_property"></span>**PROPRIETÀ \_ NOME \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Nome"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione Null che contiene il nome dell'oggetto.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROMPT_PROPERTY"></span><span id="ncrypt_pin_prompt_property"></span>**PROPRIETÀ DI RICHIESTA PIN NCRYPT \_ \_ \_**
</dt> <dd> <dl> <dt>

L"SmartCardPinPrompt"
</dt> <dt>



Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PIN_PROPERTY"></span><span id="ncrypt_pin_property"></span>**PROPRIETÀ PIN NCRYPT \_ \_**
</dt> <dd> <dl> <dt>

L"SmartCardPin"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione Null contenente il PIN. Il PIN viene usato per una chiave smart card o la password per una chiave protetta da password archiviata in un KSP basato su software. Questa proprietà può essere impostata solo. I KSP Microsoft memorizzano nella cache questo valore in modo che all'utente venga richiesto solo una volta per ogni processo.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_PROVIDER_HANDLE_PROPERTY"></span><span id="ncrypt_provider_handle_property"></span>**PROPRIETÀ \_ HANDLE \_ DEL PROVIDER NCRYPT \_**
</dt> <dd> <dl> <dt>

L"Handle provider"
</dt> <dt>



Handle **PROV NCRYPT \_ \_ che** contiene l'handle del provider di archiviazione chiavi CNG. Dopo aver terminato di usare l'handle, è necessario chiamare [**NCryptFreeObject**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfreeobject) per rilasciarlo.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_READER_PROPERTY"></span><span id="ncrypt_reader_property"></span>**PROPRIETÀ READER \_ NCRYPT \_**
</dt> <dd> <dl> <dt>

L"SmartCardReader"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione Null che contiene il nome del smart card lettore. Questa proprietà può essere impostata solo.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_ROOT_CERTSTORE_PROPERTY"></span><span id="ncrypt_root_certstore_property"></span>**PROPRIETÀ \_ \_ CERTSTORE RADICE \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"SmartcardRootCertStore"
</dt> <dt>



**HCERTSTORE che rappresenta** l'smart card archivio certificati radice.


</dt> </dl> </dd> <dt>

<span id="_NCRYPT_SCARD_PIN_ID"></span><span id="_ncrypt_scard_pin_id"></span>**NCRYPT \_ ID \_ PIN \_ SCARD**
</dt> <dd> <dl> <dt>

L"SmartCardPinId"
</dt> <dt>



Puntatore al valore **\_ DELL'ID PIN** associato a una chiave [*crittografica specificata*](/windows/desktop/SecGloss/c-gly) in un [*smart card*](/windows/desktop/SecGloss/s-gly). Questa proprietà è di sola lettura. Il **tipo di dati \_ ID PIN** è definito in Cardmod.h.

**Windows Server 2008 e Windows Vista:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SCARD_PIN_INFO"></span><span id="ncrypt_scard_pin_info"></span>**NCRYPT \_ SCARD \_ PIN \_ INFO**
</dt> <dd> <dl> <dt>

L"SmartCardPinInfo"
</dt> <dt>



Puntatore alla [**struttura \_ PIN INFO**](/windows/desktop/api/mbnapi/ns-mbnapi-mbn_pin_info) del PIN associato a una chiave crittografica specificata nel smart card. Il chiamante fornisce l'handle della chiave. Questa proprietà è di sola lettura. La **struttura \_ PIN INFO** è definita in Cardmod.h.

**Windows Server 2008 e Windows Vista:** Questo valore non è supportato.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURE_PIN_PROPERTY"></span><span id="ncrypt_secure_pin_property"></span>**PROPRIETÀ \_ DEL \_ PIN SICURO \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"SmartCardSecurePin"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione Null che contiene il PIN smart card sessione. Questa proprietà può essere impostata solo.

**Windows Vista:** Questa proprietà non è supportata.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_PROPERTY"></span><span id="ncrypt_security_descr_property"></span>**PROPRIETÀ \_ \_ DESCR DI SICUREZZA \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Security Descr"
</dt> <dt>



Puntatore a una [**struttura SECURITY \_ DESCRIPTOR**](/windows/desktop/api/winnt/ns-winnt-security_descriptor) che contiene informazioni di controllo di accesso per la chiave. Questa proprietà si applica solo alle chiavi persistenti. Il *parametro dwFlags* della funzione [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) o [**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) identifica la parte del descrittore di sicurezza da ottenere o impostare.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SECURITY_DESCR_SUPPORT_PROPERTY"></span><span id="ncrypt_security_descr_support_property"></span>**PROPRIETÀ DI \_ SUPPORTO \_ DESCR \_ DI SICUREZZA \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Security Descr Support"
</dt> <dt>



Indica se il provider supporta descrittori di sicurezza per le chiavi. Questa proprietà è un **valore DWORD** che contiene 1 se il provider supporta descrittori di sicurezza per le chiavi. Se questa proprietà contiene qualsiasi altro valore o se la funzione [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) restituisce **NTE \_ NOT \_ SUPPORTED,** il provider non supporta i descrittori di sicurezza per le chiavi. Questa proprietà si applica solo ai provider.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_SMARTCARD_GUID_PROPERTY"></span><span id="ncrypt_smartcard_guid_property"></span>**PROPRIETÀ \_ GUID DELLA SMART CARD \_ \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"SmartCardGuid"
</dt> <dt>



BLOB che contiene l'identificatore del smart card.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UI_POLICY_PROPERTY"></span><span id="ncrypt_ui_policy_property"></span>**PROPRIETÀ DEI CRITERI \_ \_ DELL'INTERFACCIA \_ UTENTE NCRYPT**
</dt> <dd> <dl> <dt>

L"Criteri dell'interfaccia utente"
</dt> <dt>



Se usato con la [**funzione NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty) o [**NCryptGetProperty,**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) si tratta di un puntatore a una struttura criteri dell'interfaccia utente [**NCRYPT \_ \_**](/windows/desktop/api/Ncrypt/ns-ncrypt-ncrypt_ui_policy) che contiene i criteri dell'interfaccia utente con chiave forte per la chiave. Questa proprietà si applica solo alle chiavi persistenti. Questa proprietà può essere impostata solo quando viene generata la chiave. Dopo aver [**chiamato la funzione NCryptFinalizeKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptfinalizekey) per questa chiave, questa proprietà diventa di sola lettura.

Un provider di archiviazione chiavi può ricevere questo parametro tramite una funzione di callback [**NCryptSetPropertyFn.**](https://www.bing.com/search?q=**NCryptSetPropertyFn**) Il valore del parametro è una struttura BLOB di criteri dell'interfaccia utente NCRYPT \_ che contiene le stesse \_ \_ informazioni. Analogamente, quando un'applicazione effettua una richiesta tramite NCryptSetPropertyFn al provider per restituire questa proprietà, è previsto che il provider restituirà una struttura BLOB di criteri dell'interfaccia utente \_ \_ \_ NCRYPT.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_UNIQUE_NAME_PROPERTY"></span><span id="ncrypt_unique_name_property"></span>**PROPRIETÀ NOME \_ \_ UNIVOCO \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Nome univoco"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione Null contenente il nome univoco dell'oggetto. Si tratta di un nome alternativo che può essere usato quando si accede alla chiave. Questa proprietà viene usata quando si pensa che il nome della chiave originariamente passato a [**NCryptCreatePersistedKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptcreatepersistedkey) non sia sufficientemente univoco da identificare in modo affidabile la chiave persistente. Il provider di archiviazione chiavi Microsoft restituirà il nome file della chiave come questa proprietà.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_CONTEXT_PROPERTY"></span><span id="ncrypt_use_context_property"></span>**PROPRIETÀ DI CONTESTO \_ USE \_ \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"Usa contesto"
</dt> <dt>



Puntatore a una stringa Unicode con terminazione Null che descrive il contesto dell'operazione. Questa proprietà non è persistente e può essere impostata in un provider o in una chiave. Una chiave non ha accesso alla proprietà **NCRYPT \_ USE CONTEXT \_ \_ PROPERTY** del provider perché la proprietà è specifica solo per l'handle per cui è impostato.

Un esempio in cui questa proprietà viene usata nel contesto di un provider è un provider di archiviazione chiavi che deve richiedere all'utente durante una chiamata a [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) (ad esempio, "Inserire il smart card nel lettore"). Poiché l'handle di chiave non è disponibile fino a quando non viene **restituito NCryptOpenKey,** l'applicazione deve impostare questa proprietà sull'handle del provider prima di chiamare **NCryptOpenKey**.

Un esempio in cui questa proprietà viene usata nel contesto di un handle di chiave è un provider di archiviazione chiavi che deve richiedere all'utente durante un'operazione che usa la chiave (ad esempio, "Questa applicazione deve usare questa chiave per firmare un documento"). Il provider può quindi inoltrare queste informazioni di contesto all'utente in qualsiasi interfaccia utente visualizzata durante l'operazione.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_ENABLED_PROPERTY"></span><span id="ncrypt_use_count_enabled_property"></span>**PROPRIETÀ NCRYPT \_ USE \_ COUNT \_ \_ ENABLED**
</dt> <dd> <dl> <dt>

L"Enabled Use Count"
</dt> <dt>



Indica se il provider supporta il conteggio dell'utilizzo per le chiavi. Questa proprietà è un **valore DWORD** che contiene 1 se il provider supporta il conteggio dell'utilizzo per le chiavi. Se questa proprietà contiene qualsiasi altro valore o se la funzione [**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty) restituisce **NTE \_ NOT \_ SUPPORTED,** il provider non supporta il conteggio dell'utilizzo per le chiavi. Questa proprietà si applica solo ai provider.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USE_COUNT_PROPERTY"></span><span id="ncrypt_use_count_property"></span>**NCRYPT \_ USE COUNT - \_ \_ PROPRIETÀ**
</dt> <dd> <dl> <dt>

L"Use Count"
</dt> <dt>



Variabile [**ULARGE \_ INTEGER**](https://docs.microsoft.com/windows/win32/api/winnt/ns-winnt-ularge_integer~r1) che contiene il numero di operazioni eseguite dalla [*chiave privata*](/windows/desktop/SecGloss/p-gly) specificata. Questa proprietà è facoltativa e potrebbe non essere supportata da tutti i provider. I provider che supportano questa proprietà nelle chiavi devono supportare anche la proprietà **NCRYPT \_ USE COUNT ENABLED \_ \_ \_ PROPERTY** nell'handle del provider. Il provider di archiviazione chiavi Microsoft non supporta questa proprietà. Questa proprietà si applica solo alle chiavi persistenti.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_USER_CERTSTORE_PROPERTY"></span><span id="ncrypt_user_certstore_property"></span>**PROPRIETÀ \_ \_ CERTSTORE UTENTE \_ NCRYPT**
</dt> <dd> <dl> <dt>

L"SmartCardUserCertStore"
</dt> <dt>



**HCERTSTORE che** rappresenta l'archivio certificati smart card utente.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_VERSION_PROPERTY"></span><span id="ncrypt_version_property"></span>**PROPRIETÀ NCRYPT \_ \_ VERSION**
</dt> <dd> <dl> <dt>

L"Version"
</dt> <dt>



Valore **DWORD** che contiene la versione software del provider. La parola alta contiene la versione principale e la parola bassa contiene la versione secondaria. Ad esempio, 0x00030033 = 3,51. Questa proprietà si applica solo ai provider.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_WINDOW_HANDLE_PROPERTY"></span><span id="ncrypt_window_handle_property"></span>**PROPRIETÀ HANDLE FINESTRA NCRYPT \_ \_ \_**
</dt> <dd> <dl> <dt>

L"Handle HWND"
</dt> <dt>



Puntatore all'handle della finestra (**HWND**) da utilizzare come padre di qualsiasi interfaccia utente visualizzata.

Poiché un comportamento indesiderato può verificarsi quando un'interfaccia utente viene visualizzata usando un handle di finestra **NULL** per l'elemento padre, è consigliabile che un provider di archiviazione chiavi non visualizza un'interfaccia utente a meno che questa proprietà non sia impostata.


</dt> </dl> </dd> </dl>

I valori seguenti vengono usati per definire i limiti dei dati delle proprietà.



| Costante/valore                                                                                                                                                                                                                                                 | Descrizione                                                              |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------|
| <span id="NCRYPT_MAX_PROPERTY_DATA"></span><span id="ncrypt_max_property_data"></span><dl> <dt>**NCRYPT \_ DATI \_ MAX \_ PROPERTY**</dt> <dt>0x100000</dt> </dl> | Specifica le dimensioni massime, in byte, di un valore di proprietà.<br/>     |
| <span id="NCRYPT_MAX_PROPERTY_NAME"></span><span id="ncrypt_max_property_name"></span><dl> <dt>**NCRYPT \_ NOME \_ MASSIMO \_ PROPRIETÀ**</dt> <dt>64</dt> </dl>       | Specifica la dimensione massima in caratteri del nome di una proprietà.<br/> |



## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>                                      |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/>                                |
| Intestazione<br/>                   | <dl> <dt>Ncrypt.h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**NCryptGetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptgetproperty)
</dt> <dt>

[**NCryptSetProperty**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptsetproperty)
</dt> </dl>

 

