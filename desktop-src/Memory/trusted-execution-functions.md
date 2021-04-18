---
description: 'Quando si utilizzano le enclavi utilizzate per creare ambienti di esecuzione attendibili, vengono utilizzate le funzioni seguenti:'
ms.assetid: DF6CDEE1-CAAA-429C-9939-DDC844302027
title: Funzioni di esecuzione attendibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4b1bd2411d0448346f0a8afcca870c26b4a61ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307845"
---
# <a name="trusted-execution-functions"></a>Funzioni di esecuzione attendibili

Quando si utilizzano le enclavi utilizzate per creare ambienti di esecuzione attendibili, vengono utilizzate le funzioni seguenti:

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                               | Descrizione                                                                                                                                                                                                                    |
|-------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CallEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-callenclave)<br/>                                       | Chiama una funzione all'interno di un'enclave. <br/>                                                                                                                                                                                |
| [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave)<br/>                                   | Crea una nuova enclave non inizializzata. Un enclave è un'area isolata del codice e dei dati all'interno dello spazio di indirizzi per un'applicazione. Solo il codice eseguito all'interno dell'enclave può accedere ai dati all'interno della stessa enclave.<br/> |
| [**DeleteEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-deleteenclave)<br/>                                   | Elimina l'enclave specificata.<br/>                                                                                                                                                                                      |
| [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>       | Ottiene un report di attestazione dell'enclave che descrive l'enclave corrente ed è firmato dall'autorità responsabile del tipo di enclave. <br/>                                                              |
| [**EnclaveGetEnclaveInformation**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetenclaveinformation)<br/>     | Ottiene informazioni sull'enclave attualmente in esecuzione.<br/>                                                                                                                                                             |
| [**EnclaveSealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavesealdata)<br/>                               | Genera un BLOB (Binary Large Object) crittografato da dati unencypted.<br/>                                                                                                                                             |
| [**EnclaveUnsealData**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveunsealdata)<br/>                           | Decrittografa un BLOB (Binary Large Object) crittografato.<br/>                                                                                                                                                                   |
| [**EnclaveVerifyAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclaveverifyattestationreport)<br/> | Verifica un rapporto di attestazione generato nel sistema corrente. <br/>                                                                                                                                           |
| [**InitializeEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-initializeenclave)<br/>                           | Inizializza un enclave creato e caricato con i dati.<br/>                                                                                                                                                       |
| [**IsEnclaveTypeSupported**](/windows/desktop/api/enclaveapi/nf-enclaveapi-isenclavetypesupported)<br/>                 | Recupera un valore che indica se il tipo di enclave specificato è supportato.<br/>                                                                                                                                                       |
| [**LoadEnclaveData**](/windows/desktop/api/enclaveapi/nf-enclaveapi-loadenclavedata)<br/>                               | Carica i dati in un'enclave non inizializzata creata chiamando [**CreateEnclave**](/windows/desktop/api/enclaveapi/nf-enclaveapi-createenclave).<br/>                                                                                                        |
| [**LoadEnclaveImage**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-loadenclaveimagew)<br/>                             | Carica un'immagine e tutte le relative importazioni in un'enclave.<br/>                                                                                                                                                              |
| [**TerminateEnclave**](/windows/desktop/api/Enclaveapi/nf-enclaveapi-terminateenclave)<br/>                             | Termina l'esecuzione dei thread in esecuzione all'interno di un'enclave.<br/>                                                                                                                                               |



 

 

 




