---
description: Individuazione di un componente per l'attivazione
ms.assetid: 2ba9484a-c646-4a35-8b32-268fe7a9520f
title: Individuazione di un componente per l'attivazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bd90068c34469d61af36e6de8c409cb02e078c
ms.sourcegitcommit: bf526e267d3991892733bdd229c66d5365cf244a
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/05/2021
ms.locfileid: "104556574"
---
# <a name="locating-a-component-for-activation"></a>Individuazione di un componente per l'attivazione

Quando COM+ individua la partizione corretta, tramite il set di partizioni predefinito dell'identità utente, un moniker di partizione o l'ID di partizione nel contesto dell'oggetto, COM + deve quindi individuare il componente corretto all'interno della partizione. Nella figura seguente viene illustrato come viene individuato e attivato un componente quando tale componente risiede in una partizione.

> [!Note]  
> Prima dell'attivazione di un componente, COM+ esegue una convalida per verificare che l'identità utente che tenta di attivare il componente disponga dei diritti di accesso al set di partizioni in cui risiede il componente.

 

![Diagramma che mostra un albero per la risoluzione dei problemi per l'individuazione di un componente per l'attivazione.](images/26c26a37-ec95-4f9f-aa59-4d84a7bb0fa3.png)

L'illustrazione precedente mostra quanto segue:

-   Se il componente chiamato risiede in una partizione e si trova nella stessa applicazione del componente chiamante, il componente viene attivato se il componente chiamato è contrassegnato come pubblico o privato.
-   Se il componente chiamato si trova in una partizione ma non esiste nella stessa applicazione del componente chiamante, COM+ verifica se il componente è contrassegnato come Public. Se non viene trovata alcuna versione pubblica, COM+ esegue una ricerca nella partizione globale per trovare una versione pubblica del componente. Se non viene trovata alcuna versione pubblica del componente nella partizione globale o se l'identità dell'utente non dispone di diritti per la partizione, l'attivazione avrà esito negativo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Individuazione delle partizioni durante l'attivazione](locating-partitions-during-activation.md)
</dt> </dl>

 

 



