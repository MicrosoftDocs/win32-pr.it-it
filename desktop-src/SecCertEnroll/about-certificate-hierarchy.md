---
description: Man mano che il numero di certificati emessi in un'infrastruttura a chiave pubblica (PKI) aumenta, può diventare difficile per una singola autorità di certificazione (CA) rilevare efficacemente i certificati emessi.
ms.assetid: f1642c1c-d2cd-4fa4-8a26-cebf3d6dcf23
title: Gerarchia di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05c4ed9a69ff96ec0904e658444d6a32b65ed82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104552359"
---
# <a name="certificate-hierarchy"></a>Gerarchia di certificati

Man mano che il numero di certificati emessi in un'infrastruttura a chiave pubblica (PKI) aumenta, può diventare difficile per una singola autorità di certificazione (CA) rilevare efficacemente i certificati emessi. Un modo per risolvere questo problema consiste nel creare una gerarchia di certificati in cui la CA delega l'autorità per emettere certificati alle autorità subordinate che possono, a loro volta, delegare l'autorità ai subordinati. Ogni autorità di certificazione delega l'autorità emettendo un certificato CA a un subordinato. La CA iniziale nella catena è denominata radice e non è necessario che un'entità stabilisca una relazione di trust con un'autorità di certificazione che risiede in una [catena di certificati](about-certificate-chain.md) diversa da quella in cui risiede l'entità.

Nella figura seguente viene illustrata una gerarchia di certificati costituita da una CA radice, due CA subordinata alla radice (una per il reparto marketing e una per il reparto produzione) e le autorità di certificazione subordinate.

![diagramma gerarchia certificati](images/certificate-hierarchy.png)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Modelli di attendibilità](about-trust-models.md)
</dt> </dl>

 

 



