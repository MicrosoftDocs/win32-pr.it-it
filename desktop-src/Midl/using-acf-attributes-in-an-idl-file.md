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
# <a name="using-acf-attributes-in-an-idl-file"></a><span data-ttu-id="6c0cc-105">Utilizzo degli attributi ACF in un file IDL</span><span class="sxs-lookup"><span data-stu-id="6c0cc-105">Using ACF Attributes in an IDL File</span></span>

<span data-ttu-id="6c0cc-106">È possibile usare l'opzione del compilatore MIDL/[**app \_ config**](-app-config.md) per specificare gli attributi di handle del binding nel file IDL anziché in un file ACF separato.</span><span class="sxs-lookup"><span data-stu-id="6c0cc-106">You can use the /[**app\_config**](-app-config.md) MIDL compiler option to specify binding handle attributes in the IDL file rather than in a separate ACF file.</span></span> <span data-ttu-id="6c0cc-107">In particolare, è possibile applicare [**gli \_ attributi handle automatico**](auto-handle.md), [**\_ handle implicito**](implicit-handle.md)e [**\_ handle esplicito**](explicit-handle.md) all'intestazione di un'interfaccia RPC in un file IDL.</span><span class="sxs-lookup"><span data-stu-id="6c0cc-107">Specifically, you can apply the [**auto\_handle**](auto-handle.md), [**implicit\_handle**](implicit-handle.md), and [**explicit\_handle**](explicit-handle.md) attributes to the header of an RPC interface in an IDL file.</span></span> <span data-ttu-id="6c0cc-108">Provare a usare questa opzione se l'applicazione RPC non richiede altri attributi ACF e se non è necessaria la compatibilità strict OSF-DCE.</span><span class="sxs-lookup"><span data-stu-id="6c0cc-108">Consider using this option if your RPC application does not require other ACF attributes, and if you do not require strict OSF-DCE compatibility.</span></span>

 

 




