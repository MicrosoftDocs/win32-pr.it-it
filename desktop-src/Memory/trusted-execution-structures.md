---
description: 'Quando si utilizzano le enclavi utilizzate per creare ambienti di esecuzione attendibili, vengono utilizzate le strutture seguenti:'
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: Strutture di esecuzione attendibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44d934ec26f9973697b987bf3a816e95d94ea591
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311124"
---
# <a name="trusted-execution-structures"></a>Strutture di esecuzione attendibili

Quando si utilizzano le enclavi utilizzate per creare ambienti di esecuzione attendibili, vengono utilizzate le strutture seguenti:

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                         | Descrizione                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENCLAVe \_ Crea \_ informazioni \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx)<br/>                      | Contiene informazioni specifiche dell'architettura da usare per creare un'enclave quando il tipo di enclave è il **tipo di enclave \_ \_ SGX**, che specifica un'enclave per l'estensione dell'architettura Intel Software Guard Extensions (SGX).<br/>     |
| [**informazioni su creazione ENCLAVe \_ \_ \_ vbs**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs)<br/>                      | Contiene informazioni specifiche dell'architettura da usare per creare un'enclave quando il tipo di enclave è il **tipo di enclave \_ \_ vbs**, che specifica un'enclave di sicurezza basata sulla virtualizzazione (VBS).<br/>                                       |
| [**identità ENCLAVe \_**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity)<br/>                                      | Descrive l'identità del modulo principale di un'enclave. <br/>                                                                                                                                                                 |
| [**informazioni ENCLAVe \_**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information)<br/>                                | Contiene informazioni sull'enclave attualmente in esecuzione.<br/>                                                                                                                                                                  |
| [**\_ \_ SGX informazioni init enclave \_**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx)<br/>                          | Contiene informazioni specifiche dell'architettura da usare per inizializzare un'enclave quando il tipo di enclave è il **tipo di enclave \_ \_ SGX**, che specifica un'enclave per l'estensione dell'architettura Intel Software Guard Extensions (SGX).<br/> |
| [**\_ \_ vbs informazioni init enclave \_**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs)<br/>                          | Contiene informazioni specifiche dell'architettura da usare per inizializzare un'enclave quando il tipo di enclave è il **tipo di enclave \_ \_ vbs**, che specifica un'enclave di sicurezza basata sulla virtualizzazione (VBS).<br/>                                   |
| [**\_CONFIG32 enclave immagine \_**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | Definisce il formato della configurazione dell'enclave per i sistemi che eseguono Windows a 32 bit.<br/>                                                                                                                                          |
| [**\_CONFIG64 enclave immagine \_**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | Definisce il formato della configurazione dell'enclave per i sistemi che eseguono Windows a 64 bit.<br/>                                                                                                                                          |
| [**\_importazione dell'enclave dell'immagine \_**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | Definisce una voce nella matrice di immagini che possono essere importate da un enclave.<br/>                                                                                                                                                           |
| [**\_report enclave vbs \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | Descrive il formato dell'istruzione firmata contenuta in un report generato chiamando la funzione [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                     |
| [**\_modulo report enclave vbs \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | Descrive un modulo caricato per l'enclave.<br/>                                                                                                                                                                                   |
| [**\_ \_ intestazione pkg del report dell'ENCLAVe vbs \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | Descrive il contenuto di un report generato chiamando la funzione [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                                                     |
| [**\_ \_ intestazione VARDATA del report dell'ENCLAVe vbs \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | Descrive il formato di un blocco di dati della variabile contenuto in un report generato dalla funzione [**EnclaveGetAttestationReport**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport) .<br/>                                                          |



 

 

 
