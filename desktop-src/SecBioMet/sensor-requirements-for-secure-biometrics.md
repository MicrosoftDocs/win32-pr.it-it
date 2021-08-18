---
title: Requisiti dei sensori per la biometria sicura
description: Requisiti dei sensori per la biometria sicura
ms.assetid: 6D5709E9-7B6B-4D6C-BF85-C6FB5DF5A7EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba76ee3b114f79d3c60adfa252f59cd2b8f98aa135e50faf93cf5ecf7314ad99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911793"
---
# <a name="sensor-requirements-for-secure-biometrics"></a>Requisiti dei sensori per la biometria sicura

Microsoft sfrutta Trusted Platform Module (TPM) 2.0 per garantire che nell'hardware appropriato, il software (fino al malware a livello di kernel incluso) non possa produrre un'autenticazione biometrica valida se la biometria dell'utente non è stata fornita al momento dell'autenticazione.

A tale scopo, si usano le autorizzazioni basate sulla sessione TPM 2.0 e il sensore che esegue l'estrazione e la corrispondenza delle funzionalità in un ambiente di esecuzione attendibile. La prima volta che Windows Biometric Framework rileva un sensore sicuro (come segnalato dalla funzionalità del sensore sicuro), effettua il provisioning di un segreto condiviso tra il sensore biometrico sicuro e il TPM. Il segreto non viene mai più esposto al sistema operativo ed è univoco per ogni sensore.

Per eseguire un'autenticazione, Windows Biometric Framework apre una sessione con il TPM e ottiene un nonce. Il parametro nonce viene passato al sensore sicuro come parte di un'operazione di corrispondenza sicura. Il sensore esegue la corrispondenza nell'ambiente di esecuzione attendibile e, se ha esito positivo, calcola un HMAC su tale nonce e l'identità dell'utente identificato.

Questo HMAC può essere usato da Windows Biometric Framework per eseguire operazioni di crittografia nel TPM per l'utente identificato. Il valore HMAC è di breve durata e scade dopo alcuni secondi.

Usando questo protocollo, dopo il provisioning iniziale, nel sistema operativo non sono contenuti dati sensibili. I segreti vengono mantenuti dal TPM e dal sensore sicuro e l'unica cosa esposta durante l'autenticazione è l'HMAC di breve durata.

## <a name="secure-sensor-capability"></a>Proteggere la funzionalità del sensore

La funzionalità WINBIO CAPABILITY SECURE SENSOR deve essere segnalata dal sensore se supporta i nuovi metodi dell'adattatore motore nella versione \_ \_ 4.0 dell'interfaccia \_ dell'adattatore del motore.

Per attestare che un sensore è un sensore sicuro, deve soddisfare i requisiti seguenti:

-   Il motore corrispondente del sensore deve essere isolato dal normale sistema operativo (ad esempio, usando un ambiente di esecuzione attendibile)
-   Il sensore deve supportare l'input sicuro di campioni nel motore di corrispondenza isolato; Il contenuto degli esempi non deve mai essere esposto al normale sistema operativo
-   Il motore corrispondente deve supportare il rilascio di credenziali protette implementando i nuovi metodi v4 descritti di seguito
-   Il sensore deve supportare il rilevamento degli attacchi di presentazione.

Il valore \_ WINBIO CAPABILITY \_ SECURE SENSOR è contenuto nella struttura CAPABILITIES \_ [**\_ di WINBIO.**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) Ecco un esempio di come definirlo.


```
#define WINBIO_CAPABILITY_SECURE_SENSOR     ((WINBIO_CAPABILITIES)0x00000100)
```



## <a name="error-codes"></a>Codici errore


```C++
//
// MessageId: WINBIO_E_INVALID_KEY_IDENTIFIER
//
// MessageText:
//
// The key identifier is invalid.
//
#define WINBIO_E_INVALID_KEY_IDENTIFIER ((HRESULT)0x80098052L)

//
// MessageId: WINBIO_E_KEY_CREATION_FAILED
//
// MessageText:
//
// The key cannot be created.
//
#define WINBIO_E_KEY_CREATION_FAILED ((HRESULT)0x80098053L)

// 
// MessageId: WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL 
//
// MessageText: 
// 
// The key identifier buffer is too small. 
// 
#define WINBIO_E_KEY_IDENTIFIER_BUFFER_TOO_SMALL ((HRESULT)0x80098054L)
```



## <a name="engine-adapter-interface-v-40"></a>Interfaccia dell'adattatore motore v 4.0

La versione dell'interfaccia dell'adattatore del motore è stata incrementata alla versione 4.0. Le funzioni aggiuntive nella nuova interfaccia consentono al sensore di partecipare a TPM 2.0. ovvero:

-   [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn)
-   [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)


```
// 

// Additional methods available in V4.0 and later 

// 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_CREATE_KEY_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(KeySize) const UCHAR* Key, 

    _In_ SIZE_T KeySize, 

    _Out_writes_bytes_to_(KeyIdentifierSize, *ResultSize) PUCHAR KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PSIZE_T ResultSize 

    ); 


typedef HRESULT 

(WINAPI *PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN)( 

    _Inout_ PWINBIO_PIPELINE Pipeline, 

    _In_reads_(NonceSize) const UCHAR* Nonce, 

    _In_ SIZE_T NonceSize, 

    _In_reads_(KeyIdentifierSize) const UCHAR* KeyIdentifier, 

    _In_ SIZE_T KeyIdentifierSize, 

    _Out_ PWINBIO_IDENTITY Identity, 

    _Out_ PWINBIO_BIOMETRIC_SUBTYPE SubFactor, 

 _Out_ PWINBIO_REJECT_DETAIL RejectDetail, 

    _Outptr_result_bytebuffer_(*AuthorizationSize) PUCHAR *Authorization, 

    _Out_ PSIZE_T AuthorizationSize 

    ); 


#define WINBIO_ENGINE_INTERFACE_VERSION_4   WINBIO_MAKE_INTERFACE_VERSION(4,0) 


typedef struct _WINBIO_ENGINE_INTERFACE { 

    WINBIO_ADAPTER_INTERFACE_VERSION            Version; 

    WINBIO_ADAPTER_TYPE                         Type; 

    SIZE_T                                      Size; 

    GUID                                        AdapterId; 


    PIBIO_ENGINE_ATTACH_FN                      Attach; 

    PIBIO_ENGINE_DETACH_FN                      Detach; 


    PIBIO_ENGINE_CLEAR_CONTEXT_FN               ClearContext; 


    PIBIO_ENGINE_QUERY_PREFERRED_FORMAT_FN      QueryPreferredFormat; 

    PIBIO_ENGINE_QUERY_INDEX_VECTOR_SIZE_FN     QueryIndexVectorSize; 

    PIBIO_ENGINE_QUERY_HASH_ALGORITHMS_FN       QueryHashAlgorithms; 

    PIBIO_ENGINE_SET_HASH_ALGORITHM_FN          SetHashAlgorithm; 


    PIBIO_ENGINE_QUERY_SAMPLE_HINT_FN           QuerySampleHint; 


    PIBIO_ENGINE_ACCEPT_SAMPLE_DATA_FN          AcceptSampleData;       // PROCESSES CURRENT BUFFER FROM PIPELINE AND GENERATES A FEATURE SET IN THE PIPELINE 

    PIBIO_ENGINE_EXPORT_ENGINE_DATA_FN          ExportEngineData;       // EXPORTS FEATURE SET OR TEMPLATE 


    PIBIO_ENGINE_VERIFY_FEATURE_SET_FN          VerifyFeatureSet; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_FN        IdentifyFeatureSet; 


    PIBIO_ENGINE_CREATE_ENROLLMENT_FN           CreateEnrollment;       // ATTACHES AN EMPTY ENROLLMENT TEMPLATE TO THE PIPELINE 

    PIBIO_ENGINE_UPDATE_ENROLLMENT_FN           UpdateEnrollment;       // CONVERTS CURRENT PIPELINE FEATURE SET INTO SOMETHING THAT CAN BE ADDED TO A TEMPLATE 

    PIBIO_ENGINE_GET_ENROLLMENT_STATUS_FN       GetEnrollmentStatus;    // QUERIES TEMPLATE ATTACHED TO THE PIPELINE TO SEE IF IT IS READY TO COMMIT 

    PIBIO_ENGINE_GET_ENROLLMENT_HASH_FN         GetEnrollmentHash; 

    PIBIO_ENGINE_CHECK_FOR_DUPLICATE_FN         CheckForDuplicate;      // DETERMINES WHETHER TEMPLATE IS ALREADY ENROLLED 

    PIBIO_ENGINE_COMMIT_ENROLLMENT_FN           CommitEnrollment; 

    PIBIO_ENGINE_DISCARD_ENROLLMENT_FN          DiscardEnrollment; 


    PIBIO_ENGINE_CONTROL_UNIT_FN                ControlUnit; 

    PIBIO_ENGINE_CONTROL_UNIT_PRIVILEGED_FN     ControlUnitPrivileged; 


#if (NTDDI_VERSION >= NTDDI_WIN8) 

    // 

    // V2.0 methods begin here... 

    // 

    PIBIO_ENGINE_NOTIFY_POWER_CHANGE_FN         NotifyPowerChange; 

    PIBIO_ENGINE_RESERVED_1_FN                  Reserved_1; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WINTHRESHOLD) 

    // 

    // V3.0 methods begin here... 

    // 

    PIBIO_ENGINE_PIPELINE_INIT_FN                       PipelineInit; 

    PIBIO_ENGINE_PIPELINE_CLEANUP_FN                    PipelineCleanup; 

    PIBIO_ENGINE_ACTIVATE_FN                            Activate; 

    PIBIO_ENGINE_DEACTIVATE_FN                          Deactivate; 

    PIBIO_ENGINE_QUERY_EXTENDED_INFO_FN                 QueryExtendedInfo; 

    PIBIO_ENGINE_IDENTIFY_ALL_FN                        IdentifyAll; 

    PIBIO_ENGINE_SET_ENROLLMENT_SELECTOR_FN             SetEnrollmentSelector; 

    PIBIO_ENGINE_SET_ENROLLMENT_PARAMETERS_FN           SetEnrollmentParameters; 

    PIBIO_ENGINE_QUERY_EXTENDED_ENROLLMENT_STATUS_FN    QueryExtendedEnrollmentStatus; 

    PIBIO_ENGINE_REFRESH_CACHE_FN                       RefreshCache;  

    PIBIO_ENGINE_SELECT_CALIBRATION_FORMAT_FN           SelectCalibrationFormat; 

    PIBIO_ENGINE_QUERY_CALIBRATION_DATA_FN              QueryCalibrationData; 

    PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN                  SetAccountPolicy; 

#endif 


#if (NTDDI_VERSION >= NTDDI_WIN10_RS1) 

    // 

    // V4.0 methods begin here... 

    // 

    PIBIO_ENGINE_CREATE_KEY_FN                     CreateKey; 

    PIBIO_ENGINE_IDENTIFY_FEATURE_SET_SECURE_FN    IdentifyFeatureSetSecure; 

#endif 


} WINBIO_ENGINE_INTERFACE, *PWINBIO_ENGINE_INTERFACE; 
```



## <a name="requirements"></a>Requisiti

Windows 10

 

 