---
title: Classi, oggetti e interfacce
description: Classi, oggetti e interfacce
ms.assetid: 52e48402-32d5-46b0-8eb9-46432e59e36a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d4892a805c87122ff7fb6db80feb52a7dcd7625
ms.sourcegitcommit: 52d79b29f3b9933c8bef43207ff80c668a81cb73
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104474615"
---
# <a name="classes-objects-and-interfaces"></a>Classi, oggetti e interfacce

Nel linguaggio di programmazione C++, una *classe* è costituita da *Proprietà* (o dati membro) e *Metodi* (o funzioni membro). Le proprietà sono elementi dati, ad esempio quelli contenuti in una struttura. I metodi vengono utilizzati per diversi scopi, ad esempio l'inizializzazione, l'assegnazione, le operazioni e l'accesso ai dati. Usare una dichiarazione di classe nello stesso modo in cui si usa una dichiarazione della struttura. La memoria viene allocata per una classe quando si definisce un *oggetto* classe. Ogni oggetto classe dispone di un'area dati per le relative proprietà e una tabella di puntatori ai metodi supportati.

In OLE un oggetto è costituito da dati e metodi, come avviene in C++. Tuttavia, un oggetto OLE rispetta regole più restrittive. I dati sono strettamente interni. Un oggetto espone solo le interfacce. Un' *interfaccia* è un set di metodi correlati per un oggetto. Ogni oggetto può supportare più interfacce. Tutte le interfacce OLE supportano l'interfaccia [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) .

 

 




