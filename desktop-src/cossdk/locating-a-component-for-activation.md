---
description: Individuazione di un componente per l'attivazione
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Individuazione di un componente per l'attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51badf0b33f7c133cdea1fa95c859c2f36e282bc748c75c560d57abeead802c4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118306220"
---
# <a name="locating-a-component-for-activation"></a>Individuazione di un componente per l'attivazione

Quando COM+ individua la partizione corretta, tramite il set di partizioni predefinito dell'identità utente, un moniker di partizione o l'ID di partizione nel contesto dell'oggetto, COM+ deve quindi individuare il componente corretto all'interno di tale partizione. Nella figura seguente viene illustrato come un componente viene trovato e attivato quando tale componente risiede in una partizione.

> [!Note]  
> Prima dell'attivazione di un componente, COM+ esegue una convalida per verificare che l'identità utente che tenta di attivare il componente abbia i diritti di accesso al set di partizioni in cui risiede il componente.

 

![Diagramma che mostra un albero di risoluzione dei problemi per l'individuazione di un componente per l'attivazione.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

La figura precedente mostra quanto segue:

-   Se il componente chiamato risiede in una partizione e si trova nella stessa applicazione del componente chiamante, il componente viene attivato indipendentemente dal fatto che il componente chiamato sia contrassegnato come pubblico o privato.
-   Se il componente chiamato risiede in una partizione ma non esiste nella stessa applicazione del componente chiamante, COM+ verifica se il componente è contrassegnato come pubblico. Se non viene trovata alcuna versione pubblica, COM+ cerca nella partizione globale per trovare una versione pubblica del componente. Se non viene trovata alcuna versione pubblica del componente nella partizione globale o se l'identità utente non dispone di diritti per la partizione, l'attivazione non riesce.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Individuazione delle partizioni durante l'attivazione](locating-partitions-during-activation.md)
</dt> </dl>

 

 



