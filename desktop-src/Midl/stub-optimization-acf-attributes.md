---
title: Attributi ACF di ottimizzazione Stub
description: Questi attributi consentono di ottimizzare le dimensioni e la velocità del codice stub.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- ACF MIDL, attributi, Stub-ottimizzazione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 209490d6064d134a51492afee39c501059879bab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855882"
---
# <a name="stub-optimization-acf-attributes"></a>Attributi ACF di ottimizzazione Stub

Questi attributi consentono di ottimizzare le dimensioni e la velocità del codice stub.



| Attributo                                    | Utilizzo                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**codice**](code.md)[**NoCode**](nocode.md) | Usare insieme gli attributi [**Code**](code.md) e [**NoCode**](nocode.md) per evitare la generazione di codice stub per le funzioni inutilizzate. Applicare l'attributo **NoCode** all'intestazione dell'interfaccia e applicare l'attributo **Code** a tali procedure che verranno implementate dall'applicazione client. Il codice stub client verrà generato solo per le procedure selezionate.                                                                |
| [**ottimizzare**](optimize.md)                 | Consente di ottimizzare il livello di ottimizzazione eseguito dal compilatore MIDL durante la generazione di codice stub, specificando che è necessario effettuare il marshalling dei dati tramite il metodo misto o interpretato. È possibile applicare l'attributo [**optimize**](optimize.md) a un'interfaccia o a funzioni selezionate all'interno dell'interfaccia. In entrambi i casi, il relativo utilizzo eseguirà l'override delle ottimizzazioni della riga di comando e di eventuali impostazioni predefinite preesistenti. |



 

 

 




