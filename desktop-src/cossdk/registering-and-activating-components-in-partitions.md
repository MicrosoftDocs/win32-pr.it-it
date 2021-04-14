---
description: Registrazione e attivazione di componenti nelle partizioni
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Registrazione e attivazione di componenti nelle partizioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523530"
---
# <a name="registering-and-activating-components-in-partitions"></a>Registrazione e attivazione di componenti nelle partizioni

Dopo la creazione di una partizione, il passaggio successivo consiste nel registrare i componenti COM+ all'interno di tale partizione. Un componente viene registrato all'interno di una partizione quando viene creata una nuova applicazione COM+ o quando si installa un'applicazione COM+ esistente nella partizione. Per semplificare l'amministrazione della registrazione quando più partizioni contengono gli stessi componenti COM+, il servizio partizioni consente a un amministratore di copiare applicazioni o componenti da una partizione all'altra. Quando viene copiata un'applicazione COM+ o un componente, vengono copiate tutte le proprietà della partizione associate, ad eccezione dell'identità dell'applicazione o di uno dei membri di un ruolo.

Quando il programma client chiama la funzione [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) o [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) per creare un'istanza di un oggetto, com+ esegue due passaggi distinti, come indicato di seguito:

1.  Individua la partizione in cui risiede il componente
2.  Individua il componente corretto all'interno della partizione

Negli argomenti seguenti di questa sezione vengono descritti in dettaglio i passaggi seguenti:

-   [Individuazione delle partizioni durante l'attivazione](locating-partitions-during-activation.md)
-   [Individuazione di un componente per l'attivazione](locating-a-component-for-activation.md)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Limitazioni relative alla progettazione di applicazioni](application-design-restrictions.md)
</dt> <dt>

[Componenti e partizioni in coda COM+](com--queued-components-and-partitions.md)
</dt> <dt>

[Implementazione della partizione](partition-implementation.md)
</dt> <dt>

[Che cosa sono le partizioni COM+?](what-are-com--partitions-.md)
</dt> </dl>

 

 
