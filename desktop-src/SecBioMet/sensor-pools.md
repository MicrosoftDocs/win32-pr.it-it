---
title: Pool di sensori
description: Descrive tre possibili pool di sensori, privato e non assegnato.
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d28bd03d84e2558f0fb1ba090440aa2bda62292c51773d54d5094466ba9e494
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035261"
---
# <a name="sensor-pools"></a>Pool di sensori

Per supportare sia Windows scenari di autenticazione che l'autenticazione definita dal fornitore, il servizio biometrico Windows organizza le unità biometriche in tre possibili pool di sensori:

-   **Pool privato:** raccolta di unità biometriche allocate per l'uso esclusivo da parte di un'applicazione client. I pool privati possono supportare scenari di autenticazione non basati su Windows e rendono possibile per un'applicazione accedere all'hardware di un'unità biometrica in modo definito dal fornitore. Nel sistema possono essere presenti tutti i pool di sensori privati quanti sono le unità biometriche.
-   **Pool di sensori di** sistema una raccolta di unità biometriche condivisibili che forniscono l'accesso Windows servizi di autenticazione. Questo pool viene usato da Winlogon, controllo dell'account utente e da qualsiasi altro client che associa un SID a un modello biometrico specifico. Ogni provider di servizi biometrici ha un pool di sensori di sistema.
-   **Il pool non assegnato** contiene una raccolta (probabilmente vuota) di unità biometriche non assegnate al pool di sistema o al pool privato.

Le applicazioni possono usare il pool di sistema condiviso o creare un pool privato costituito da unità biometriche rimosse dal sistema o da pool non assegnati. Quando un'applicazione rilascia il pool privato, le unità biometriche vengono riconfigurate e restituite ai pool originali. Per evitare attacchi Denial of Service, solo gli utenti con privilegi sono autorizzati a rimuovere l'ultimo sensore dal pool di sistema. Per ulteriori informazioni, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                       | Descrizione                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pool di sensori privati](private-sensor-pool.md)<br/>   | Raccolta di unità biometriche riservate per l'uso esclusivo da parte di un'applicazione client. I pool privati supportano metodi di autenticazione proprietari e consentono a un'applicazione client di accedere a un'unità biometrica usando i comandi di controllo specificati dal fornitore.<br/> |
| [Pool di sensori di sistema](system-sensor-pool.md)<br/>     | Raccolta di unità biometriche condivisibili che forniscono l'accesso Windows servizi di autenticazione. Questo pool viene usato da Winlogon, controllo dell'account utente e da qualsiasi altro client che associa un SID a un modello biometrico specifico.<br/>                                 |
| [Comportamento del pool di sistema](system-pool-behavior.md)<br/> | Discussione sulle azioni eseguite dal pool di sistema quando vengono inviate notifiche di eventi e quando non sono in sospeso operazioni biometriche.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API Windows Biometric Framework](./biometric-service-api-portal.md)
</dt> </dl>

 

