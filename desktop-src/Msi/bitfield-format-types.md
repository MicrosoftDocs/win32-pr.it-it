---
description: I tipi di formato bit dei dati configurabili possono essere utilizzati in campi di database di tipo Integer.
ms.assetid: 3b05392e-4276-4970-ae43-9ee00bc9f476
title: Tipi di formato bit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b443f7ee363d1a2b48eb580623018264df8d50be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106311011"
---
# <a name="bitfield-format-types"></a>Tipi di formato bit

I tipi di formato bit dei dati configurabili possono essere utilizzati in campi di database di tipo Integer. L'utente deve scegliere un valore da un subset specificato. Questo è solo per convenzione e non viene applicato da Mergemod.dll. L'attributo msmConfigItemNonNullable è implicito in questo formato dati e non è necessario impostarlo. Null non è mai un valore valido per questo tipo.

Il tipo di formato bit seguente esiste.

[Tipo bit arbitrario](arbitrary-bitfield-type.md)

Gli elementi configurabili del tipo di formato bit vengono usati nelle colonne integer e in generale potrebbero essere sostituiti da qualsiasi numero intero. L'utente deve scegliere un valore da un subset specificato. Questa operazione è tuttavia solo per convenzione e non viene applicata da Mergemod.dll. L'autore deve preparare il modulo per gestire qualsiasi valore.

 

 



