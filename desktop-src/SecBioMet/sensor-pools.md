---
title: Pool di sensori
description: Descrive tre possibili pool di sensori di sistema, privati e non assegnati.
ms.assetid: d7fd3c39-d719-4cfd-9af0-a87837f3f328
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 263275af5c7decff37ef70ad3a5396ec562562f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104399261"
---
# <a name="sensor-pools"></a>Pool di sensori

Per supportare sia gli scenari di autenticazione di Windows che l'autenticazione definita dal fornitore, il servizio biometrico di Windows organizza le unità biometriche in tre possibili pool di sensori:

-   **Pool privato** raccolta di unità biometriche allocate per l'utilizzo esclusivo da un'applicazione client. I pool privati possono supportare scenari di autenticazione che non sono basati su Windows e consentono a un'applicazione di accedere all'hardware di un'unità biometrica in modo definito dal fornitore. Nel sistema possono essere presenti molti pool di sensori privati, perché sono presenti unità biometriche.
-   Il **pool di sensori di sistema** è una raccolta di unità biometriche condivisibili che consentono di accedere ai servizi di autenticazione di Windows. Questo pool viene usato da Winlogon, UAC e da qualsiasi altro client che associa un SID a un modello biometrico specifico. Ogni provider di servizi biometrico ha un pool di sensori di sistema.
-   Il **pool non assegnato** contiene una raccolta (possibilmente vuota) di unità biometriche che non sono assegnate al pool di sistema o al pool privato.

Le applicazioni possono usare il pool di sistema condiviso oppure creare un pool privato costituito da unità biometriche rimosse dal sistema o da pool non assegnati. Quando un'applicazione rilascia il proprio pool privato, le unità biometriche vengono riconfigurate e restituite ai pool originali. Per evitare attacchi di tipo Denial of Service, solo gli utenti con privilegi possono rimuovere l'ultimo sensore dal pool di sistema. Per ulteriori informazioni, vedere gli argomenti seguenti.

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                       | Descrizione                                                                                                                                                                                                                                                    |
|-------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Pool di sensori privati](private-sensor-pool.md)<br/>   | Raccolta di unità biometriche riservate per l'utilizzo esclusivo da un'applicazione client. I pool privati supportano i metodi di autenticazione proprietari e consentono a un'applicazione client di accedere a un'unità biometrica usando i comandi di controllo specificati dal fornitore.<br/> |
| [Pool di sensori di sistema](system-sensor-pool.md)<br/>     | Raccolta di unità biometriche condivisibili che consentono di accedere ai servizi di autenticazione di Windows. Questo pool viene usato da Winlogon, UAC e da qualsiasi altro client che associa un SID a un modello biometrico specifico.<br/>                                 |
| [Comportamento del pool di sistema](system-pool-behavior.md)<br/> | Discussione sulle azioni eseguite dal pool di sistema quando si inviano notifiche degli eventi e quando non sono in sospeso operazioni biometriche.<br/>                                                                                                                     |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sull'API Windows Biometric Framework](./biometric-service-api-portal.md)
</dt> </dl>

 

