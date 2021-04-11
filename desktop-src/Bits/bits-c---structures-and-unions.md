---
title: Strutture e unioni BITS
description: Le interfacce di Servizio trasferimento intelligente in background (BITS) utilizzano le strutture seguenti.
ms.assetid: a1b8b4a1-77d6-46ac-96d5-6a0c99cfc643
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 93763daa73bc96e12dd27b862d75fbb23869c20f
ms.sourcegitcommit: 31f494fef71b63ad411b86b22b4cc01af6e37c8d
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/20/2019
ms.locfileid: "104332844"
---
# <a name="bits-structures-and-unions"></a>Strutture e unioni BITS

Le [interfacce](bits-interfaces.md) di servizio trasferimento intelligente in background (BITS) utilizzano le strutture seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**BG_AUTH_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials) | Identifica la destinazione (proxy o server), lo schema di autenticazione e le credenziali dell'utente da usare per le richieste di autenticazione utente. La struttura viene passata al [metodo IBackgroundCopyJob2:: Secredentials](/windows/win32/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials). |
| [**BG_AUTH_CREDENTIALS_UNION**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials_union) | Identifica le credenziali da utilizzare per lo schema di autenticazione specificato nella [struttura BG_AUTH_CREDENTIALS](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials). |
| [**BG_BASIC_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_basic_credentials) | Identifica il nome utente e la password per l'autenticazione. |
| [**BG_FILE_INFO**](/windows/win32/api/bits/ns-bits-bg_file_info) | Fornisce i nomi locali e remoti del file da trasferire. |
| [**BG_FILE_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_file_progress) | Fornisce informazioni sullo stato di avanzamento correlate ai file, ad esempio il numero di byte trasferiti. |
| [**BG_FILE_RANGE**](/windows/win32/api/bits2_0/ns-bits2_0-bg_file_range) | Identifica un intervallo di byte da scaricare da un file. |
| [**BG_JOB_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_job_progress) | Fornisce informazioni sullo stato di avanzamento correlate al processo, ad esempio il numero di byte e i file trasferiti. Per i processi di caricamento, lo stato di avanzamento si applica al file di caricamento, non al file di risposta. Per visualizzare lo stato di avanzamento dei file di risposta, vedere la [struttura BG_JOB_REPLY_PROGRESS](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress). |
| [**BG_JOB_REPLY_PROGRESS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress) | Fornisce informazioni sullo stato di avanzamento correlate alla parte di risposta di un processo di caricamento-risposta. |
| [**BG_JOB_TIMES**](/windows/win32/api/bits/ns-bits-bg_job_times) | Fornisce timestamp correlati al processo. |
| [**Unione BITS_FILE_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Fornisce il valore della proprietà di un file BITS. |
| [**BITS_JOB_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Fornisce il valore della proprietà del processo BITS in base al valore dell' [enumerazione BITS_JOB_PROPERTY_ID](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id). |
