---
description: I tipi di formato dei campi di bit dei dati configurabili possono essere usati in campi di database integer.
ms.assetid: 3b05392e-4276-4970-ae43-9ee00bc9f476
title: Tipi di formato dei campi di bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dd6f4052df6780d88397aa26da66ac9db3755e80cffd70efb642cc5873d216d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145734"
---
# <a name="bitfield-format-types"></a>Tipi di formato dei campi di bit

I tipi di formato dei campi di bit dei dati configurabili possono essere usati in campi di database integer. L'utente deve scegliere un valore da un subset specificato. Questo è solo per convenzione e non viene applicato da Mergemod.dll. L'attributo msmConfigItemNonNullable è implicito in questo formato di dati e non deve essere impostato. Null non è mai un valore valido per questo tipo.

Il tipo di formato del campo di bit seguente esiste.

[Tipo di campo di bit arbitrario](arbitrary-bitfield-type.md)

Gli elementi configurabili del tipo di formato Bitfield vengono usati nelle colonne integer e in generale possono essere sostituiti da qualsiasi numero intero. L'utente deve scegliere un valore da un subset specificato. Questa operazione viene tuttavia applicata solo per convenzione e non viene applicata Mergemod.dll. L'autore deve preparare il modulo per gestire qualsiasi valore.

 

 



