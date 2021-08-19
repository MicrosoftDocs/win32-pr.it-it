---
title: Annotazione server
description: In questa sezione vengono fornite informazioni sull'utilizzo dell'annotazione server.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c9438184cf68d4a0f819afcd7e5497e627a0982e0f9fd9784c8a3460ab5121a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052539"
---
# <a name="server-annotation"></a>Annotazione server

In questa sezione vengono fornite informazioni sull'utilizzo dell'annotazione server.

## <a name="summary"></a>Riepilogo

Si definisce una classe che implementa [**IAccPropServer,**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver)ne viene creata un'istanza e si indica al sistema che deve eseguire l'override di proprietà specifiche in elementi dell'interfaccia utente specifici. Quando un client richiede una delle proprietà da uno degli elementi dell'interfaccia utente, l'oggetto viene chiamato e ha la possibilità di fornire un valore. Se l'oggetto restituisce un valore, tale valore viene passato nuovamente al client. Se l'oggetto non restituisce un valore, il valore predefinito per tale elemento dell'interfaccia utente viene restituito al client.

## <a name="when-to-use-this-technique"></a>Quando usare questa tecnica

Usare questa tecnica quando si vuole eseguire l'override delle [**proprietà IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) per un oggetto. Questa tecnica è molto più semplice rispetto alle **tecniche IAccessible** precedenti. Per altre informazioni, vedere [Alternatives to Dynamic Annotation](alternatives-to-dynamic-annotation.md).

Non è possibile utilizzare l'annotazione server per modificare la struttura dell'oggetto esposto. Per modificare la struttura di un oggetto, è necessario implementare un puntatore di [**interfaccia IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) completo.

Per altre informazioni sull'annotazione del server, vedere gli argomenti seguenti:

-   [Uso dell'annotazione server](using-server-annotation.md)
-   [Esempio di annotazione server](server-annotation-sample.md)

 

 




