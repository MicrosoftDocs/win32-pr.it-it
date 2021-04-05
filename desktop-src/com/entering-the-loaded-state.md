---
title: Immissione dello stato caricato
description: Immissione dello stato caricato
ms.assetid: 841b6f1a-cf9d-4a7e-9732-0701777a9617
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: add74927d107d7f6b9fe2d76856adec6697a00c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709442"
---
# <a name="entering-the-loaded-state"></a>Immissione dello stato caricato

Quando un oggetto passa allo stato Loaded, vengono create le strutture in memoria che rappresentano l'oggetto, in modo che sia possibile richiamare le operazioni su di esso. Il gestore dell'oggetto o il server in-process viene caricato. Questo processo, denominato creazione di *istanza*, si verifica quando un oggetto viene caricato dall'archivio permanente (una transizione dallo stato passivo a quello caricato) o quando viene creato un oggetto per la prima volta.

Internamente, la creazione di istanze è un processo in due fasi. Viene creato un oggetto della classe appropriata, dopo il quale viene chiamato un metodo su tale oggetto per eseguire l'inizializzazione e consentire l'accesso ai dati dell'oggetto. Il metodo di inizializzazione è definito in una delle interfacce supportate dell'oggetto. Il metodo di inizializzazione specifico chiamato dipende dal contesto in cui viene creata un'istanza dell'oggetto e dal percorso dei dati di inizializzazione.

 

 




