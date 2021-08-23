---
title: Quando usare la tabella di interfaccia globale
description: Quando usare la tabella di interfaccia globale
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37457e0e1b35c0c1acb2c8f84750f3d0f08c1344eaf27e0361c442aea3be23ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119639231"
---
# <a name="when-to-use-the-global-interface-table"></a>Quando usare la tabella di interfaccia globale

Se si annulla ilmarshaling di un puntatore di interfaccia più volte tra gli apartment in un processo, è possibile usare [**l'interfaccia IGlobalInterfaceTable.**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) Con altre tecniche, è necessario eseguire il remarshal ogni volta.

> [!Note]  
> Se il puntatore a interfaccia viene disassociato una sola volta, è possibile usare la [**funzione CoMarshalInterThreadInterfaceInStream.**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) Può anche essere usato per passare un puntatore a interfaccia da un thread a un altro thread nello stesso processo.

 

[**L'interfaccia IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) semplifica anche un altro problema precedentemente difficile per il programmatore. Questo problema si verifica quando si verificano le condizioni seguenti:

-   Un oggetto Agile in-process aggrega il gestore di marshalling a thread libero.
-   Questo stesso oggetto Agile contiene anche (come variabili membro) puntatori a interfaccia ad altri oggetti che non sono Agile e non aggregano il gestore di marshalling a thread libero.

In questo caso, se viene effettuato il marshalling dell'oggetto esterno in un altro apartment e l'applicazione chiama su di esso e l'oggetto tenta di chiamare su uno dei puntatori a interfaccia della variabile membro che non sono a thread libero o sono proxy per oggetti in altri apartment, è possibile che si otterrà un risultato non corretto o l'errore RPC \_ E \_ WRONG \_ THREAD. Questo errore si verifica perché l'interfaccia interna è progettata per essere chiamata solo dall'apartment in cui è stata archiviata per la prima volta nella variabile membro .

Per risolvere questo problema, l'oggetto esterno che aggrega il gestore di marshalling a thread libero deve chiamare [**IGlobalInterfaceTable::RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) sull'interfaccia interna e archiviare il cookie risultante nella variabile membro, anziché archiviare il puntatore di interfaccia effettivo. Quando l'oggetto esterno vuole chiamare sul puntatore a interfaccia di un oggetto interno, deve chiamare [**IGlobalInterfaceTable::GetInterfaceFromGlobal,**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal)usare il puntatore di interfaccia restituito e quindi rilasciarlo. Quando l'oggetto esterno viene rimosso, deve chiamare [**IGlobalInterfaceTable::RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) per rimuovere l'interfaccia dalla tabella di interfaccia globale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione della tabella di interfaccia globale](creating-the-global-interface-table.md)
</dt> </dl>

 

 