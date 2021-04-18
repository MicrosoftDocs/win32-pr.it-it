---
description: Una catena di certificati è una raccolta gerarchica di certificati che conduce dall'utente finale o dal computer a una radice di attendibilità, in genere l'autorità di certificazione radice (CA) di un'organizzazione.
ms.assetid: 53701ede-269c-4949-b839-3f2b64cb5510
title: Catena di certificati
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e7509adb164c98cf07912af00af0d91c27ab8df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319383"
---
# <a name="certificate-chain"></a>Catena di certificati

Una catena di certificati è una raccolta gerarchica di certificati che conduce dall'utente finale o dal computer a una radice di attendibilità, in genere l'autorità di certificazione radice (CA) di un'organizzazione. Poiché tutte le entità considerano presumibilmente attendibile il certificato radice, un'entità può ottenere l'attendibilità in un certificato dell'entità finale verificando la catena di certificati. Per la verifica in genere è necessario stabilire che ogni certificato nella catena:

-   Viene firmato dalla chiave pubblica nel certificato precedente.
-   Non è scaduto.
-   Non è stato revocato.
-   È conforme ai criteri specificati dai certificati precedenti.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gerarchia di certificati](about-certificate-hierarchy.md)
</dt> <dt>

[Certificazione incrociata](about-cross-certification.md)
</dt> <dt>

[Modelli di attendibilità](about-trust-models.md)
</dt> </dl>

 

 



