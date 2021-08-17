---
description: Con l'aumentare del numero di certificati emessi in un'infrastruttura a chiave pubblica (PKI), può diventare difficile per una singola autorità di certificazione (CA) tenere traccia in modo efficace dei certificati rilasciati.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Gerarchia di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abc3420e3f0f09f88b4b9e7157ec8abacc9516520de4472a48189520e3e0e567
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904977"
---
# <a name="certificate-hierarchy"></a>Gerarchia di certificati

Con l'aumentare del numero di certificati emessi in un'infrastruttura a chiave pubblica (PKI), può diventare difficile per una singola autorità di certificazione (CA) tenere traccia in modo efficace dei certificati rilasciati. Un modo per risolvere questo problema è creare una gerarchia di certificati in cui la CA delega l'autorità di certificazione per rilasciare certificati alle autorità subordinate che possono, a sua volta, delegare l'autorità ai propri subordinati. Ogni autorità di certificazione delega l'autorità emettendo un certificato della CA a un subordinato. La CA iniziale nella catena è denominata radice e non è necessario che un'entità stabilirà una relazione di trust con qualsiasi CA che risiede in una catena di certificati diversa da quella in cui risiede l'entità. [](about-certificate-chain.md)

La figura seguente mostra una gerarchia di certificati che è costituito da una CA radice, due CA subordinate alla radice (una per il reparto marketing e una per il reparto di produzione) e ca ca subordinate a queste.

![diagramma della gerarchia di certificati](images/certificate-hierarchy.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli di attendibilità](about-trust-models.md)
</dt> </dl>

 

 



