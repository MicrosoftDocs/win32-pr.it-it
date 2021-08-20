---
title: Pool di sensori di sistema
description: Raccolta di unità biometriche condivisibili che forniscono l'accesso ai Windows di autenticazione. Questo pool viene usato da Winlogon, controllo dell'account utente e da qualsiasi altro client che associa un SID a un modello biometrico specifico.
ms.assetid: 308306a9-e12c-4ff6-92c3-a36667a5e548
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c73a187c81812355d574b6c4fb867aad8f832c504f7ec79289879565cf73bcf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911614"
---
# <a name="system-sensor-pool"></a>Pool di sensori di sistema

Il pool di sensori di sistema è una raccolta di unità biometriche condivisibili che forniscono l'accesso ai Windows di autenticazione. Questo pool viene usato da Winlogon, controllo dell'account utente e da qualsiasi altro client che associa un SID a un modello biometrico specifico. Unità biometriche nel pool di sistema:

-   Può essere condiviso da più applicazioni client.
-   Inviare le notifiche degli eventi generate dal completamento delle operazioni biometriche solo all'applicazione con lo stato attivo della finestra corrente.
-   Usare i SID dell'account per rappresentare le identità del modello. Tutti i modelli associati a un singolo account utente vengono contrassegnati con il SID assegnato a tale account.
-   Dipendere dall'archiviazione dei modelli attendibile fornita dal Windows biometrico.

Un'unità biometrica può essere inclusa nel pool di sistema se può essere:

-   Configurato per operare in modalità di base e fungere solo da dispositivo di acquisizione biometrica.
-   Configurato per operare in modalità avanzata, ma senza archiviazione modello di onboard. Ciò significa che deve usare l'adapter di archiviazione e l'archivio modelli forniti da Microsoft.
-   Configurato per operare in modalità avanzata, contiene l'archiviazione dei modelli di onboarding e può generare gli hash necessari.

Quando un nuovo dispositivo sensore è collegato, il servizio biometrico Windows crea un'unità biometrica per esso e tenta di configurare tale unità per l'uso da parte del pool di sensori di sistema. Se la configurazione non riesce, l'unità biometrica viene inserita nel pool di sensori non assegnati.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Pool di sensori privati](private-sensor-pool.md)
</dt> <dt>

[Pool di sensori](sensor-pools.md)
</dt> <dt>

[Comportamento del pool di sistema](system-pool-behavior.md)
</dt> </dl>

 

 




