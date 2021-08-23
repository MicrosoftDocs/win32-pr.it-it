---
title: Handle di serializzazione
description: Un'applicazione usa le routine di serializzazione o le routine di supporto di serializzazione generate dal compilatore MIDL insieme a un set di funzioni di libreria per modificare un handle di serializzazione.
ms.assetid: 39859846-5b94-447a-a71b-a08b8eb2c4c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 12995144e44fa6b4b91f021d544b53c03d732df22d46489ccc2cefe8d34c0fa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925477"
---
# <a name="serialization-handles"></a>Handle di serializzazione

Un'applicazione usa le routine di serializzazione o le routine di supporto di serializzazione generate dal compilatore MIDL insieme a un set di funzioni di libreria per modificare un handle di serializzazione. Insieme, queste funzioni forniscono un meccanismo per personalizzare il modo in cui un'applicazione serializza i dati.

Un handle di serializzazione è necessario per qualsiasi operazione di serializzazione e tutti gli handle di serializzazione devono essere gestiti in modo esplicito dall'utente. A tale scopo, creare prima un handle valido chiamando una delle routine seguenti:

-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)

L'handle viene rilasciato con una chiamata a [**MesHandleFree.**](/windows/desktop/api/Midles/nf-midles-meshandlefree) Dopo che l'handle è stato creato o reinizializzato, rappresenta un contesto di serializzazione valido e può essere usato per codificare o decodificare, a seconda del tipo di handle.

In questa sezione vengono descritti gli handle di serializzazione e come usarli negli argomenti seguenti:

-   [Handle impliciti ed espliciti](implicit-versus-explicit-handles.md)
-   [Stili di serializzazione](serialization-styles.md)
-   [Recupero di un'identità di codifica](obtaining-an-encoding-identity.md)

 

 




