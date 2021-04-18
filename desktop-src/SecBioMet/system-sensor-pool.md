---
title: Pool di sensori di sistema
description: Raccolta di unità biometriche condivisibili che consentono di accedere ai servizi di autenticazione di Windows. Questo pool viene usato da Winlogon, UAC e da qualsiasi altro client che associa un SID a un modello biometrico specifico.
ms.assetid: 308306a9-e12c-4ff6-92c3-a36667a5e548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 729ae9487b91b57b2e9568817c92e44b4b7197f7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106298287"
---
# <a name="system-sensor-pool"></a>Pool di sensori di sistema

Il pool di sensori di sistema è una raccolta di unità biometriche condivisibili che consentono di accedere ai servizi di autenticazione di Windows. Questo pool viene usato da Winlogon, UAC e da qualsiasi altro client che associa un SID a un modello biometrico specifico. Unità biometriche nel pool di sistema:

-   Può essere condiviso da più applicazioni client.
-   Inviare notifiche di eventi generate dal completamento delle operazioni biometriche solo all'applicazione con lo stato attivo della finestra corrente.
-   Usare i SID dell'account per rappresentare le identità del modello. Tutti i modelli associati a un singolo account utente sono contrassegnati con il SID assegnato a tale account.
-   Dipende dallo spazio di archiviazione dei modelli attendibile fornito dal servizio biometrico di Windows.

Un'unità biometrica può essere inclusa nel pool di sistema se può essere:

-   Configurato per operare in modalità di base e agire solo come dispositivo di acquisizione biometrico.
-   Configurata per il funzionamento in modalità avanzata ma senza archiviazione del modello di onboarding. Ovvero, deve utilizzare l'adattatore di archiviazione e l'archivio modelli forniti da Microsoft.
-   Configurato per operare in modalità avanzata, contiene l'archiviazione del modello di onboarding e può generare gli hash necessari.

Quando un nuovo dispositivo sensore viene collegato, il servizio biometrico di Windows crea un'unità biometrica e tenta di configurare tale unità per l'uso da parte del pool di sensori di sistema. Se la configurazione ha esito negativo, l'unità biometrica viene posizionata nel pool di sensori non assegnati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pool di sensori privati](private-sensor-pool.md)
</dt> <dt>

[Pool di sensori](sensor-pools.md)
</dt> <dt>

[Comportamento del pool di sistema](system-pool-behavior.md)
</dt> </dl>

 

 




