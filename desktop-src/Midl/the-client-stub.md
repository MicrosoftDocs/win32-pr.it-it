---
title: The Client Stub
description: Il modulo stub client fornisce punti di ingresso surrogati nel client per ognuna delle operazioni definite nel file IDL di input.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL e RPC MIDL, interfacce, stub client
- interfacce MIDL
- interfacce MIDL, MIDL e RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260c718f0910c2e6834c93409b6d8cd4969e3d2bbe9c53c65821dc0fe0eb19ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146224"
---
# <a name="the-client-stub"></a>The Client Stub

Il modulo stub client fornisce punti di ingresso surrogati nel client per ognuna delle operazioni definite nel file IDL di input.

Quando l'applicazione client effettua una chiamata alla procedura remota, la chiamata passa prima alla routine surrogata nel file stub del client. La routine stub client esegue le funzioni seguenti:

-   Effettua il marshalling degli argomenti. Lo stub client consente di inserire gli argomenti di input in un formato che può essere trasmesso al server.
-   Chiama la libreria di runtime del client per trasmettere argomenti allo spazio di indirizzi remoto e richiama la procedura remota nello spazio di indirizzi del server.
-   Annulla ilmarshaling degli argomenti di output. Lo stub client decomprime gli argomenti di output e torna al chiamante.

Le opzioni del compilatore [**MIDL /client**](-client.md), [**/cstub**](-cstub.md)e [**/out**](-out.md) influiscono sul file stub del client.

 

 




