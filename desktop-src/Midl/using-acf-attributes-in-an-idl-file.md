---
title: Utilizzo degli attributi ACF in un file IDL
description: È possibile usare l' \_ opzione del compilatore MIDL/app config per specificare gli attributi di handle del binding nel file IDL anziché in un file ACF separato.
ms.assetid: 3558e818-b39f-42a4-842f-05970296da0e
keywords:
- ACF MIDL, attributi, uso di ACF in IDL
- MIDL MIDL, uso di ACF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 712dde95201bc2c729ac126b35e04919fd196cbb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103709814"
---
# <a name="using-acf-attributes-in-an-idl-file"></a>Utilizzo degli attributi ACF in un file IDL

È possibile usare l'opzione del compilatore MIDL/[**app \_ config**](-app-config.md) per specificare gli attributi di handle del binding nel file IDL anziché in un file ACF separato. In particolare, è possibile applicare [**gli \_ attributi handle automatico**](auto-handle.md), [**\_ handle implicito**](implicit-handle.md)e [**\_ handle esplicito**](explicit-handle.md) all'intestazione di un'interfaccia RPC in un file IDL. Provare a usare questa opzione se l'applicazione RPC non richiede altri attributi ACF e se non è necessaria la compatibilità strict OSF-DCE.

 

 




