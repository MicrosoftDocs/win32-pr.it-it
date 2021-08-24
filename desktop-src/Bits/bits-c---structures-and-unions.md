---
title: Strutture e unioni BITS
description: Le Servizio trasferimento intelligente in background (BITS) usano le strutture seguenti.
ms.assetid: a1b8b4a1-77d6-46ac-96d5-6a0c99cfc643
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 199d5648ba8205d0417304350a104b2e16a607e4d7f1bdce4dfe9ecec34f98dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119702031"
---
# <a name="bits-structures-and-unions"></a>Strutture e unioni BITS

Le Servizio trasferimento intelligente in background (BITS) [](bits-interfaces.md) usano le strutture seguenti.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|-|-|
| [**BG_AUTH_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials) | Identifica la destinazione (proxy o server), lo schema di autenticazione e le credenziali dell'utente da usare per le richieste di autenticazione utente. La struttura viene passata al [metodo IBackgroundCopyJob2::SetCredentials](/windows/win32/api/Bits1_5/nf-bits1_5-ibackgroundcopyjob2-setcredentials). |
| [**BG_AUTH_CREDENTIALS_UNION**](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials_union) | Identifica le credenziali da utilizzare per lo schema di autenticazione specificato nella BG_AUTH_CREDENTIALS [struttura](/windows/win32/api/bits1_5/ns-bits1_5-bg_auth_credentials). |
| [**BG_BASIC_CREDENTIALS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_basic_credentials) | Identifica il nome utente e la password da autenticare. |
| [**BG_FILE_INFO**](/windows/win32/api/bits/ns-bits-bg_file_info) | Fornisce i nomi locali e remoti del file da trasferire. |
| [**BG_FILE_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_file_progress) | Fornisce informazioni sullo stato relative ai file, ad esempio il numero di byte trasferiti. |
| [**BG_FILE_RANGE**](/windows/win32/api/bits2_0/ns-bits2_0-bg_file_range) | Identifica un intervallo di byte da scaricare da un file. |
| [**BG_JOB_PROGRESS**](/windows/win32/api/bits/ns-bits-bg_job_progress) | Fornisce informazioni sullo stato del processo, ad esempio il numero di byte e file trasferiti. Per i processi di caricamento, lo stato di avanzamento si applica al file di caricamento, non al file di risposta. Per visualizzare lo stato del file di risposta, vedere la [BG_JOB_REPLY_PROGRESS struttura](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress). |
| [**BG_JOB_REPLY_PROGRESS**](/windows/win32/api/bits1_5/ns-bits1_5-bg_job_reply_progress) | Fornisce informazioni sullo stato relative alla parte di risposta di un processo di caricamento-risposta. |
| [**BG_JOB_TIMES**](/windows/win32/api/bits/ns-bits-bg_job_times) | Fornisce timestamp correlati al processo. |
| [**BITS_FILE_PROPERTY_VALUE union**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Fornisce il valore della proprietà di un file BITS. |
| [**BITS_JOB_PROPERTY_VALUE**](/windows/win32/api/bits5_0/ns-bits5_0-bits_file_property_value) | Fornisce il valore della proprietà del processo BITS in base al valore [dell'BITS_JOB_PROPERTY_ID enumerazione](/windows/win32/api/bits5_0/ne-bits5_0-bits_job_property_id). |
