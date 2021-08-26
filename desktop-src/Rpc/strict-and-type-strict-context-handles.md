---
title: Handle di contesto Strict e Type Strict
description: Usare l'attributo \_ strict context handle per tutti gli handle di \_ contesto.
ms.assetid: 2483aa76-0814-4f63-9c38-0aa050d73772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91c266fb70b540e08d066e51f61a921b8f88819456e83b909e3be31bb1f518c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120017511"
---
# <a name="strict-and-type-strict-context-handles"></a>Handle di contesto Strict e Type Strict

Usare [**l'attributo strict \_ context \_ handle**](/windows/desktop/Midl/strict-context-handle) per tutti gli handle di contesto. Per impostazione predefinita, un handle di contesto non è associato a un'interfaccia, ovvero un handle di contesto può essere creato in un'interfaccia e quindi passato a un'altra. Si tratta di un attacco semplice e molti server RPC non riescono a impedirlo.

Se due interfacce coesistono nello stesso processo, un utente malintenzionato può aprire un handle di contesto su un'interfaccia e passarlo a un'altra, che potrebbe superare i dati imprevisti. Molti sviluppatori ritengono che il software sia l'unica interfaccia in un processo, ma molto spesso non è così, perché sia il sistema che molti componenti di terze parti usano RPC internamente e tali interfacce possono creare handle di contesto. Quando si usa l'attributo strict [**\_ context \_ handle,**](/windows/desktop/Midl/strict-context-handle) il run-time RPC garantisce che un contesto creato in un'interfaccia possa essere passato come argomento solo ai metodi di tale interfaccia.

Nelle situazioni in cui un'applicazione viene sviluppata per Windows Vista, è disponibile e consigliato l'uso di [**\_ \_ \_ handle**](/windows/desktop/Midl/type-strict-context-handle) di contesto strict di tipo. Gli handle di contesto non sono associati a un tipo specifico per impostazione predefinita. Quando nello stesso processo vengono usati più tipi di handle di contesto, è possibile che un client dannoso passi un handle di contesto al posto di un altro per produrre risultati indesiderati. L'uso di **handle di contesto strict di \_ \_ \_** tipo consente alle applicazioni di applicare la coerenza del tipo di handle di contesto e impedire qualsiasi utilizzo del tipo di handle di contesto non corrispondente.

 

 