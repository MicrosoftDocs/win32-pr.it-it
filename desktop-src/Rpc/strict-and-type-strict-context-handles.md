---
title: Handle di contesto Strict e di tipo strict
description: Utilizzare l' \_ attributo Strict Context \_ handle per tutti gli handle di contesto.
ms.assetid: 2483aa76-0814-4f63-9c38-0aa050d73772
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a45b4e7914034e315f2275e1d928293332012fc4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104473694"
---
# <a name="strict-and-type-strict-context-handles"></a>Handle di contesto Strict e di tipo strict

Utilizzare l'attributo [**strict \_ Context \_ handle**](/windows/desktop/Midl/strict-context-handle) per tutti gli handle di contesto. Per impostazione predefinita, un handle di contesto non è associato a un'interfaccia, il che significa che è possibile creare un handle di contesto in un'interfaccia, quindi passarlo a un altro. Si tratta di un semplice attacco e molti server RPC non riescono a impedirlo.

Se due interfacce coesisteranno nello stesso processo, un utente malintenzionato può aprire un handle di contesto in un'interfaccia e passarlo a un altro, che può eseguire il viaggio sui dati imprevisti. Molti sviluppatori ritengono che il software sia l'unica interfaccia di un processo, ma molto spesso non è così, perché sia il sistema che molti componenti di terze parti utilizzano RPC internamente e tali interfacce possono creare handle di contesto. Quando viene utilizzato l'attributo [**strict \_ Context \_ handle**](/windows/desktop/Midl/strict-context-handle) , il runtime RPC garantisce che un contesto creato in un'interfaccia possa essere passato come argomento solo ai metodi di tale interfaccia.

Nelle situazioni in cui viene sviluppata un'applicazione per Windows Vista, l'utilizzo di un [**\_ handle di \_ contesto \_ di tipo strict**](/windows/desktop/Midl/type-strict-context-handle) è disponibile e consigliato. Per impostazione predefinita, gli handle di contesto non sono associati a un tipo specifico. Quando nello stesso processo vengono usati più tipi di handle di contesto, è possibile che un client malintenzionato passi un handle di contesto al posto di un altro per produrre risultati non desiderati. L'utilizzo di **un \_ \_ \_ handle di contesto di tipo strict** consente alle applicazioni di applicare la coerenza del tipo di handle del contesto ed evitare qualsiasi utilizzo del tipo di handle del contesto non corrispondente.

 

 