---
title: Requisiti dei sensori per la biometria sicura
description: Requisiti dei sensori per la biometria sicura
ms.assetid: 6D5709E9-7B6B-4D6C-BF85-C6FB5DF5A7EE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82f4e41f8300a124115c2b6cd380f904f216f491
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "106300026"
---
# <a name="sensor-requirements-for-secure-biometrics"></a><span data-ttu-id="4a0a9-103">Requisiti dei sensori per la biometria sicura</span><span class="sxs-lookup"><span data-stu-id="4a0a9-103">Sensor requirements for secure biometrics</span></span>

<span data-ttu-id="4a0a9-104">Microsoft si avvale di Trusted Platform Module (TPM) 2,0 per garantire che l'hardware, il software, fino a un malware a livello di kernel appropriato, non possa produrre un'autenticazione biometrica valida se la biometria dell'utente non è stata fornita al momento dell'autenticazione.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-104">Microsoft leverages Trusted Platform Module (TPM) 2.0 to ensure that on appropriate hardware, software (up to and including kernel-level malware) cannot produce a valid biometric authentication if the user’s biometric was not provided at the time of authentication.</span></span>

<span data-ttu-id="4a0a9-105">A tale scopo, vengono usate le autorizzazioni basate sulla sessione TPM 2,0 e il sensore che esegue l'estrazione delle funzionalità e la corrispondenza in un ambiente di esecuzione attendibile.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-105">To do this, we use TPM 2.0 session-based authorizations and the sensor performing feature extraction and matching in a trusted execution environment.</span></span> <span data-ttu-id="4a0a9-106">La prima volta che il Windows Biometric Framework rileva un sensore sicuro (come segnalato dalla funzionalità di sensore protetto), effettua il provisioning di un segreto condiviso tra il sensore biometrico sicuro e il TPM.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-106">The first time the Windows Biometric Framework sees a secure sensor (as reported by the secure sensor capability), it provisions a secret that is shared between the secure biometric sensor and the TPM.</span></span> <span data-ttu-id="4a0a9-107">Il segreto non viene mai esposto al sistema operativo ed è univoco per ogni sensore.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-107">That secret is never again exposed to the OS, and it is unique to each sensor.</span></span>

<span data-ttu-id="4a0a9-108">Per eseguire un'autenticazione, il Windows Biometric Framework apre una sessione con il TPM e ottiene un parametro nonce.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-108">To perform an authentication, the Windows Biometric Framework opens a session with the TPM and obtains a nonce.</span></span> <span data-ttu-id="4a0a9-109">Il parametro nonce viene passato nel sensore sicuro come parte di un'operazione di corrispondenza sicura.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-109">The nonce is passed into the secure sensor as part of a secure match operation.</span></span> <span data-ttu-id="4a0a9-110">Il sensore esegue la corrispondenza nell'ambiente di esecuzione attendibile e, in caso di esito positivo, calcola un HMAC su tale nonce e l'identità dell'utente identificato.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-110">The sensor performs the match in the trusted execution environment, and if it is successful, calculates an HMAC over that nonce and the identity of the user who was identified.</span></span>

<span data-ttu-id="4a0a9-111">Questo HMAC può essere utilizzato dal Windows Biometric Framework per eseguire operazioni di crittografia nel TPM per l'utente identificato.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-111">This HMAC can be used by the Windows Biometric Framework to perform cryptographic operations in the TPM for the user who was identified.</span></span> <span data-ttu-id="4a0a9-112">Il valore HMAC è di breve durata e scade dopo pochi secondi.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-112">The HMAC is short-lived, and expires after a few seconds.</span></span>

<span data-ttu-id="4a0a9-113">Con questo protocollo, dopo il provisioning iniziale, non sono contenuti dati sensibili nel sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-113">Using this protocol, after the initial provisioning, no sensitive data is contained in the OS.</span></span> <span data-ttu-id="4a0a9-114">I segreti sono conservati dal TPM e dal sensore protetto e l'unica cosa che viene esposta durante l'autenticazione è il HMAC di breve durata.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-114">Secrets are held by the TPM and the secure sensor, and the only thing that is exposed during the authentication is the short-lived HMAC.</span></span>

## <a name="secure-sensor-capability"></a><span data-ttu-id="4a0a9-115">Funzionalità di sensore sicuro</span><span class="sxs-lookup"><span data-stu-id="4a0a9-115">Secure sensor capability</span></span>

<span data-ttu-id="4a0a9-116">La \_ funzionalità di \_ sensore sicuro per la funzionalità WINBIO \_ deve essere segnalata dal sensore se supporta i nuovi metodi di adattatore del motore nella v 4,0 dell'interfaccia dell'adattatore del motore.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-116">The WINBIO\_CAPABILITY\_SECURE\_SENSOR capability must be reported by the sensor if it supports the new engine adapter methods in v 4.0 of the engine adapter interface.</span></span>

<span data-ttu-id="4a0a9-117">Per richiedere che un sensore sia un sensore sicuro, deve soddisfare i requisiti seguenti:</span><span class="sxs-lookup"><span data-stu-id="4a0a9-117">To claim that a sensor is a secure sensor it must meet the following requirements:</span></span>

-   <span data-ttu-id="4a0a9-118">Il motore di corrispondenza del sensore deve essere isolato dal normale sistema operativo, ad esempio usando un ambiente di esecuzione attendibile.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-118">The matching engine of the sensor must be isolated from the normal OS (for example, using a trusted execution environment)</span></span>
-   <span data-ttu-id="4a0a9-119">Il sensore deve supportare l'input protetto degli esempi nel motore corrispondente isolato; il contenuto degli esempi non deve mai essere esposto al normale sistema operativo</span><span class="sxs-lookup"><span data-stu-id="4a0a9-119">The sensor must support secure input of samples to the isolated matching engine; the content of the samples must never be exposed to the normal OS</span></span>
-   <span data-ttu-id="4a0a9-120">Il motore di corrispondenza deve supportare la versione di credenziali sicure implementando i nuovi metodi V4 descritti di seguito</span><span class="sxs-lookup"><span data-stu-id="4a0a9-120">The matching engine must support secure credential release by implementing the new v4 methods outlined below</span></span>
-   <span data-ttu-id="4a0a9-121">Il sensore deve supportare il rilevamento degli attacchi di presentazione.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-121">The sensor must support presentation attack detection.</span></span>

<span data-ttu-id="4a0a9-122">Il \_ valore del \_ sensore sicuro per la funzionalità WINBIO \_ è contenuto nella struttura delle [**\_ funzionalità di WINBIO**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) .</span><span class="sxs-lookup"><span data-stu-id="4a0a9-122">The WINBIO\_CAPABILITY\_SECURE\_SENSOR value is contained in the [**WINBIO\_CAPABILITIES**](/windows-hardware/drivers/ddi/winbio_ioctl/ns-winbio_ioctl-_winbio_sensor_attributes) structure.</span></span> <span data-ttu-id="4a0a9-123">Di seguito è riportato un esempio di come definirlo.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-123">Here's an example of how to define it.</span></span>


```
#define WINBIO_CAPABILITY_SECURE_SENSOR     ((WINBIO_CAPABILITIES)0x00000100)
```



## <a name="error-codes"></a><span data-ttu-id="4a0a9-124">Codici errore</span><span class="sxs-lookup"><span data-stu-id="4a0a9-124">Error Codes</span></span>


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



## <a name="engine-adapter-interface-v-40"></a><span data-ttu-id="4a0a9-125">Interfaccia adattatore motore v 4,0</span><span class="sxs-lookup"><span data-stu-id="4a0a9-125">Engine adapter interface v 4.0</span></span>

<span data-ttu-id="4a0a9-126">La versione dell'interfaccia dell'adattatore del motore è stata incrementata a 4,0.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-126">The engine adapter interface version has been incremented to 4.0.</span></span> <span data-ttu-id="4a0a9-127">Le funzioni aggiuntive nella nuova interfaccia consentono al sensore di partecipare al TPM 2,0.</span><span class="sxs-lookup"><span data-stu-id="4a0a9-127">The additional functions in the new interface allow the sensor to participate in TPM 2.0.</span></span> <span data-ttu-id="4a0a9-128">Ad esempio:</span><span class="sxs-lookup"><span data-stu-id="4a0a9-128">They are:</span></span>

-   [<span data-ttu-id="4a0a9-129">**EngineAdapterCreateKey**</span><span class="sxs-lookup"><span data-stu-id="4a0a9-129">**EngineAdapterCreateKey**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn)
-   [<span data-ttu-id="4a0a9-130">**EngineAdapterIdentifyFeatureSetSecure**</span><span class="sxs-lookup"><span data-stu-id="4a0a9-130">**EngineAdapterIdentifyFeatureSetSecure**</span></span>](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)


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



## <a name="requirements"></a><span data-ttu-id="4a0a9-131">Requisiti</span><span class="sxs-lookup"><span data-stu-id="4a0a9-131">Requirements</span></span>

<span data-ttu-id="4a0a9-132">Windows 10</span><span class="sxs-lookup"><span data-stu-id="4a0a9-132">Windows 10</span></span>

 

 