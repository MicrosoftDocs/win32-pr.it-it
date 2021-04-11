---
title: Annotazione server
description: In questa sezione vengono fornite informazioni sull'utilizzo delle annotazioni server.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044324"
---
# <a name="server-annotation"></a>Annotazione server

In questa sezione vengono fornite informazioni sull'utilizzo delle annotazioni server.

## <a name="summary"></a>Riepilogo

Si definisce una classe che implementa [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), ne crea un'istanza e si indica al sistema che si desidera che esegua l'override di proprietà specifiche su elementi dell'interfaccia utente specifici. Quando un client richiede una delle proprietà di uno degli elementi dell'interfaccia utente, viene chiamato l'oggetto e viene data la possibilità di fornire un valore. Se l'oggetto restituisce un valore, tale valore viene passato nuovamente al client. Se l'oggetto non restituisce un valore, il valore predefinito per tale elemento dell'interfaccia utente viene restituito al client.

## <a name="when-to-use-this-technique"></a>Quando usare questa tecnica

Utilizzare questa tecnica quando si desidera eseguire l'override delle proprietà [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un oggetto. Questa tecnica è molto più semplice rispetto alle tecniche **IAccessible** precedenti. Per ulteriori informazioni, vedere [alternative all'annotazione dinamica](alternatives-to-dynamic-annotation.md).

Non è possibile utilizzare l'annotazione server per modificare la struttura dell'oggetto esposto. Per modificare la struttura di un oggetto, è necessario implementare un puntatore di interfaccia [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) completo.

Per ulteriori informazioni sull'annotazione del server, vedere gli argomenti seguenti:

-   [Uso dell'annotazione server](using-server-annotation.md)
-   [Esempio di annotazione server](server-annotation-sample.md)

 

 




