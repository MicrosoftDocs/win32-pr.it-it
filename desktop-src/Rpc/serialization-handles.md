---
title: Handle di serializzazione
description: Un'applicazione usa le stored procedure di serializzazione o le routine di supporto per la serializzazione generate dal compilatore MIDL insieme a un set di funzioni di libreria per modificare un handle di serializzazione.
ms.assetid: 39859846-5b94-447a-a71b-a08b8eb2c4c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5585fc3f34b6cc826c1f8157bd59a144070ea081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104045160"
---
# <a name="serialization-handles"></a>Handle di serializzazione

Un'applicazione usa le stored procedure di serializzazione o le routine di supporto per la serializzazione generate dal compilatore MIDL insieme a un set di funzioni di libreria per modificare un handle di serializzazione. Insieme, queste funzioni forniscono un meccanismo per personalizzare il modo in cui un'applicazione serializza i dati.

Un handle di serializzazione è necessario per qualsiasi operazione di serializzazione e tutti gli handle di serializzazione devono essere gestiti in modo esplicito dall'utente. A tale scopo, creare innanzitutto un handle valido chiamando una delle routine seguenti:

-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)

Rilasciare l'handle con una chiamata a [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree). Una volta che l'handle è stato creato o reinizializzato, rappresenta un contesto di serializzazione valido e può essere usato per codificare o decodificare, a seconda del tipo di handle.

In questa sezione vengono descritti gli handle di serializzazione e il modo in cui utilizzarli negli argomenti seguenti:

-   [Handle impliciti e espliciti](implicit-versus-explicit-handles.md)
-   [Stili di serializzazione](serialization-styles.md)
-   [Ottenere un'identità di codifica](obtaining-an-encoding-identity.md)

 

 




