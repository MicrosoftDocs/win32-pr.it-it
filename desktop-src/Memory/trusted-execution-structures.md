---
description: 'Quando si lavora con enclave usate per creare ambienti di esecuzione attendibili, vengono usate le strutture seguenti:'
ms.assetid: 61F99132-E947-4EA4-86A0-914CE316B53A
title: Strutture di esecuzione attendibili
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9349c8c4e4c04ecc664ccab668abe55cdca1e1720b6fa17fd35bb7139f53f19c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118386252"
---
# <a name="trusted-execution-structures"></a>Strutture di esecuzione attendibili

Quando si lavora con enclave usate per creare ambienti di esecuzione attendibili, vengono usate le strutture seguenti:

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                         | Descrizione                                                                                                                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ENCLAVE \_ CREATE \_ INFO \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_sgx)<br/>                      | Contiene informazioni specifiche dell'architettura da usare per creare un enclave quando il tipo di **enclave è ENCLAVE \_ TYPE \_ SGX,** che specifica un enclave per l'estensione dell'architettura Intel Software Guard Extensions (SGX).<br/>     |
| [**ENCLAVE \_ CREATE \_ INFO \_ VBS**](/windows/desktop/api/winnt/ns-winnt-enclave_create_info_vbs)<br/>                      | Contiene informazioni specifiche dell'architettura da usare per creare un enclave quando il tipo di **enclave è ENCLAVE \_ TYPE \_ VBS,** che specifica un enclave di sicurezza basato sulla virtualizzazione (VBS).<br/>                                       |
| [**IDENTITÀ DELL'ENCLAVE \_**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_identity)<br/>                                      | Descrive l'identità del modulo primario di un enclave. <br/>                                                                                                                                                                 |
| [**INFORMAZIONI SULL'ENCLAVE \_**](/windows/desktop/api/ntenclv/ns-ntenclv-enclave_information)<br/>                                | Contiene informazioni sull'enclave attualmente in esecuzione.<br/>                                                                                                                                                                  |
| [**ENCLAVE \_ INIT \_ INFO \_ SGX**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_sgx)<br/>                          | Contiene informazioni specifiche dell'architettura da usare per inizializzare un enclave quando il tipo di **enclave è ENCLAVE \_ TYPE \_ SGX,** che specifica un enclave per l'estensione dell'architettura Intel Software Guard Extensions (SGX).<br/> |
| [**ENCLAVE \_ INIT \_ INFO \_ VBS**](/windows/desktop/api/winnt/ns-winnt-enclave_init_info_vbs)<br/>                          | Contiene informazioni specifiche dell'architettura da usare per inizializzare un enclave quando il tipo di **enclave è \_ \_ VBS DI TIPO ENCLAVE**, che specifica un enclave di sicurezza basato sulla virtualizzazione ( VBS).<br/>                                   |
| [**IMAGE \_ ENCLAVE \_ CONFIG32**](/windows/desktop/api/winnt/ns-winnt-image_enclave_config32)<br/>                         | Definisce il formato della configurazione dell'enclave per i sistemi che eseguono Windows a 32 bit.<br/>                                                                                                                                          |
| [**IMAGE \_ ENCLAVE \_ CONFIG64**](/previous-versions/windows/desktop/legacy/mt844244(v=vs.85))<br/>                         | Definisce il formato della configurazione dell'enclave per i sistemi che eseguono Windows a 64 bit.<br/>                                                                                                                                          |
| [**IMPORTAZIONE \_ DELL'ENCLAVE \_ IMMAGINE**](/windows/desktop/api/winnt/ns-winnt-image_enclave_import)<br/>                             | Definisce una voce nella matrice di immagini che un enclave può importare.<br/>                                                                                                                                                           |
| [**REPORT \_ DI VBS \_ ENCLAVE**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report)<br/>                                 | Descrive il formato dell'istruzione firmata contenuta in un report generato chiamando la [**funzione EnclaveGetAttestationReport.**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>                                                     |
| [**MODULO DI \_ REPORT DI VBS ENCLAVE \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_module)<br/>                  | Descrive un modulo caricato per l'enclave.<br/>                                                                                                                                                                                   |
| [**INTESTAZIONE \_ PKG DEL \_ REPORT \_ DI VBS ENCLAVE \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_pkg_header)<br/>         | Descrive il contenuto di un report generato chiamando la [**funzione EnclaveGetAttestationReport.**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>                                                                                     |
| [**INTESTAZIONE VARDATA DEL REPORT DI VBS \_ ENCLAVE \_ \_ \_**](/windows/desktop/api/ntenclv/ns-ntenclv-vbs_enclave_report_vardata_header)<br/> | Descrive il formato di un blocco di dati variabile contenuto in un report generato dalla [**funzione EnclaveGetAttestationReport.**](/windows/desktop/api/winenclaveapi/nf-winenclaveapi-enclavegetattestationreport)<br/>                                                          |



 

 

 
