---
title: Client moniker
description: I client moniker devono iniziare ottenendo un moniker e esistono diversi modi per ottenere un moniker da un client moniker.
ms.assetid: ab1758c4-8dfc-47f6-8e1b-875e033a54d6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8435389539f39d8ce71246267cd265c3e4edb9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297747"
---
# <a name="moniker-clients"></a>Client moniker

I client moniker devono iniziare ottenendo un moniker e esistono diversi modi per ottenere un moniker da un client moniker. Ad esempio, nei documenti compositi OLE, quando l'utente finale crea un elemento collegato (usando la finestra di dialogo **Inserisci oggetto** , gli Appunti o il trascinamento della selezione), un moniker viene incorporato come parte dell'elemento collegato. In tal caso, il programmatore ha un contatto minimo con i moniker. A livello di codice, se si dispone di un puntatore di interfaccia a un oggetto che implementa l'interfaccia [**IMoniker**](/windows/desktop/api/ObjIdl/nn-objidl-imoniker) , è possibile utilizzarlo per ottenere un moniker e sono presenti metodi su altre interfacce definite per restituire moniker.

Sono disponibili tipi diversi di moniker, usati per identificare tipi diversi di oggetti, ma a un client moniker, tutti i moniker hanno lo stesso aspetto. Un client moniker chiama semplicemente [**IMoniker:: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) su un moniker e ottiene un puntatore di interfaccia all'oggetto identificato dal moniker. La chiamata di **BindToObject** restituirà un puntatore a tale oggetto, indipendentemente dal fatto che il moniker identifichi un oggetto di grandi dimensioni come un intero foglio di calcolo o una singola cella in un foglio di calcolo. Se l'oggetto è già in esecuzione, **BindToObject** lo troverà in memoria. Se l'oggetto viene archiviato passivamente sul disco, **BindToObject** individuerà un server per tale oggetto, eseguirà il server e consentirà al server di portare l'oggetto in stato di esecuzione. Tutti i dettagli del processo di associazione sono nascosti dal client del moniker. Pertanto, per un client moniker, l'utilizzo del moniker è molto semplice.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Provider moniker](moniker-providers.md)
</dt> <dt>

[Implementazioni del moniker OLE](ole-moniker-implementations.md)
</dt> </dl>

 

 




