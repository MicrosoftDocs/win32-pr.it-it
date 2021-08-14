---
title: Attributi ACF di ottimizzazione stub
description: Questi attributi consentono di ottimizzare le dimensioni e la velocità del codice stub.
ms.assetid: 8c98b9ff-d91c-4a17-90c9-298f588e46c5
keywords:
- ACF MIDL , attributi, ottimizzazione stub
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f8386eb6a6077a994b6f9800ff237a9966e97bff5eb0d6d865ea313634790f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118383193"
---
# <a name="stub-optimization-acf-attributes"></a>Attributi ACF di ottimizzazione stub

Questi attributi consentono di ottimizzare le dimensioni e la velocità del codice stub.



| Attributo                                    | Utilizzo                                                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**code**](code.md)[**nocode**](nocode.md) | Usare il [**codice**](code.md) e [**gli attributi nocode**](nocode.md) insieme per evitare di generare codice stub per le funzioni inutilizzate. Applicare **l'attributo nocode** all'intestazione dell'interfaccia e applicare l'attributo **di codice** alle procedure che verranno implementate dall'applicazione client. Il codice stub del client verrà generato solo per le procedure selezionate.                                                                |
| [**Ottimizzare**](optimize.md)                 | Consente di ottimizzare il livello di ottimizzazione eseguito dal compilatore MIDL durante la generazione di codice stub, specificando che i dati devono essere sottoposti a marshalling tramite il metodo in modalità mista o interpretato. È possibile applicare [**l'attributo optimize**](optimize.md) a un'interfaccia o a funzioni selezionate all'interno dell'interfaccia. In entrambi i casi, l'uso di eseguirà l'override delle ottimizzazioni della riga di comando ed eventuali impostazioni predefinite preesistnti. |



 

 

 




