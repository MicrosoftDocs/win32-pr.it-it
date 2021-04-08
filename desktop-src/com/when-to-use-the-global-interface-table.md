---
title: Quando usare la tabella dell'interfaccia globale
description: Quando usare la tabella dell'interfaccia globale
ms.assetid: def8f7f8-9d0d-49a4-9d5c-40233903eea5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f89bbd7437b65c85abe89e8d647cbd73555c2d6a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/21/2020
ms.locfileid: "104047405"
---
# <a name="when-to-use-the-global-interface-table"></a>Quando usare la tabella dell'interfaccia globale

Se si esegue l'unmarshalling di un puntatore di interfaccia più volte tra gli Apartment in un processo, è possibile usare l'interfaccia [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) . Con altre tecniche, è necessario eseguire il marshalling ogni volta.

> [!Note]  
> Se viene eseguito l'unmarshalling del puntatore a interfaccia solo una volta, è possibile usare la funzione [**CoMarshalInterThreadInterfaceInStream**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterthreadinterfaceinstream) . Può anche essere usato per passare un puntatore di interfaccia da un thread a un altro thread nello stesso processo.

 

L'interfaccia [**IGlobalInterfaceTable**](/windows/desktop/api/ObjIdl/nn-objidl-iglobalinterfacetable) rende anche un altro problema più difficile in precedenza per il programmatore. Questo problema si verifica quando si applicano le condizioni seguenti:

-   Un oggetto agile in-process aggrega il gestore di marshalling a thread libero.
-   Questo stesso oggetto Agile include anche i puntatori di interfaccia (come variabili membro) per gli altri oggetti che non sono agile e non aggregano il gestore di marshalling a thread libero.

In questa situazione, se l'oggetto esterno viene sottoposto a marshalling in un altro Apartment e l'applicazione chiama su di esso e l'oggetto tenta di chiamare su uno dei puntatori a interfaccia della variabile membro che non sono a thread libero o che sono proxy di oggetti in altri Apartment, potrebbe ottenere risultati non corretti o il thread RPC di errore \_ e un \_ \_ thread errato. Questo errore si verifica perché l'interfaccia interna è progettata per essere richiamabile solo dall'Apartment in cui è stata prima archiviata nella variabile membro.

Per risolvere questo problema, è necessario che l'oggetto esterno che aggrega il gestore di marshalling a thread libero chiami [**IGlobalInterfaceTable:: RegisterInterfaceInGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-registerinterfaceinglobal) sull'interfaccia interna e memorizzi il cookie risultante nella variabile membro, anziché archiviare il puntatore di interfaccia effettivo. Quando l'oggetto esterno desidera chiamare sul puntatore a interfaccia di un oggetto interno, deve chiamare [**IGlobalInterfaceTable:: GetInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-getinterfacefromglobal), utilizzare il puntatore di interfaccia restituito e quindi rilasciarlo. Quando l'oggetto esterno viene rimosso, è necessario chiamare [**IGlobalInterfaceTable:: RevokeInterfaceFromGlobal**](/windows/win32/api/objidl/nf-objidl-iglobalinterfacetable-revokeinterfacefromglobal) per rimuovere l'interfaccia dalla tabella dell'interfaccia globale.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Creazione della tabella dell'interfaccia globale](creating-the-global-interface-table.md)
</dt> </dl>

 

 