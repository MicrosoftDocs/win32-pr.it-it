---
title: Uso di attributi ACF in un file IDL
description: È possibile usare l'opzione del compilatore MIDL /app config per specificare gli attributi dell'handle di associazione nel file IDL anziché \_ in un file ACF separato.
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- ACF MIDL , attributi, usando ACF in IDL
- IDL MIDL , con ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bda925a3b3242072f297c8828427ae4f7a488d1f3b002e05ace6bec45a46d2d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120105521"
---
# <a name="using-acf-attributes-in-an-idl-file"></a>Uso di attributi ACF in un file IDL

È possibile usare l'opzione del compilatore MIDL [**/app \_ config**](-app-config.md) per specificare gli attributi dell'handle di associazione nel file IDL anziché in un file ACF separato. In particolare, è possibile applicare gli [**\_**](explicit-handle.md) attributi [**\_ di handle**](auto-handle.md)automatico , [**\_ handle implicito**](implicit-handle.md)e handle esplicito all'intestazione di un'interfaccia RPC in un file IDL. È consigliabile usare questa opzione se l'applicazione RPC non richiede altri attributi ACF e se non è necessaria una compatibilità OSF-DCE rigida.

 

 




