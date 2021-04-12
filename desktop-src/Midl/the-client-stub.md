---
title: Stub client
description: Il modulo stub client fornisce punti di ingresso surrogati sul client per ogni operazione definita nel file IDL di input.
ms.assetid: 6b16a4ef-fa18-4cd0-b483-1365b8c2528b
keywords:
- MIDL e RPC MIDL, interfacce, Stub client
- interfacce MIDL
- interfacce MIDL, MIDL e RPC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8254915a510e7d176ba315d7a92b049bd0b60926
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104331375"
---
# <a name="the-client-stub"></a>Stub client

Il modulo stub client fornisce punti di ingresso surrogati sul client per ogni operazione definita nel file IDL di input.

Quando l'applicazione client effettua una chiamata alla procedura remota, la relativa chiamata passa prima alla routine surrogata nel file stub del client. La routine stub client esegue le funzioni seguenti:

-   Esegue il marshalling degli argomenti. Il client Stub inserisce gli argomenti di input in un modulo che può essere trasmesso al server.
-   Chiama la libreria di runtime del client per trasmettere argomenti allo spazio di indirizzi remoto e richiama la procedura remota nello spazio degli indirizzi del server.
-   Esegue l'unmarshalling degli argomenti di output. Lo stub client decomprime gli argomenti di output e restituisce al chiamante.

Il compilatore MIDL passa [**/client**](-client.md), [**/cstub**](-cstub.md)e [**/out**](-out.md) influisce sul file stub del client.

 

 




