---
title: /version_stamp opzione
description: L' \_ interruttore/Version Stamp disattiva la generazione di macro che specificano il numero minimo di versione necessario del file di intestazione RPC, Rpcndr. h.
ms.assetid: ec03f68b-60f7-431e-9fba-4434ef082058
keywords:
- /version_stamp switch MIDL
topic_type:
- apiref
api_name:
- /version_stamp
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 704393dce869df4e5f715a1157cdb57967135e42
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "106299170"
---
# <a name="version_stamp-switch"></a><span data-ttu-id="371a8-104">\_opzione Stamp/Version</span><span class="sxs-lookup"><span data-stu-id="371a8-104">/version\_stamp switch</span></span>

<span data-ttu-id="371a8-105">L'interruttore **/version \_ Stamp** disattiva la generazione di macro che specificano il numero minimo di versione necessario del file di intestazione RPC, Rpcndr. h.</span><span class="sxs-lookup"><span data-stu-id="371a8-105">The **/version\_stamp** switch suppresses the generation of macros that specify the minimum required version number of the RPC header file, Rpcndr.h.</span></span>

<span data-ttu-id="371a8-106">Le nuove funzionalità MIDL potrebbero richiedere definizioni aggiuntive per compilare correttamente lo stub, quindi lo stub include macro che controllano la compatibilità tra i file binari MIDL e l'ambiente di compilazione.</span><span class="sxs-lookup"><span data-stu-id="371a8-106">New MIDL features might require additional definitions to compile the stub correctly, so the stub has macros that check compatibility between MIDL binary files and the build environment.</span></span> <span data-ttu-id="371a8-107">Potrebbe essere necessario usare questa opzione se si sposta MIDL in un ambiente di compilazione diverso da quello in cui sono stati installati prima i file binari MIDL.</span><span class="sxs-lookup"><span data-stu-id="371a8-107">You might need to use this switch if you move MIDL to a different build environment than the one in which you first installed the MIDL binary files.</span></span>

<span data-ttu-id="371a8-108">Si noti che la combinazione di ambienti di compilazione non è supportata.</span><span class="sxs-lookup"><span data-stu-id="371a8-108">Note that mixing build environments is not supported.</span></span>

``` syntax
midl /version_stamp
```

## <a name="switch-options"></a><span data-ttu-id="371a8-109">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="371a8-109">Switch Options</span></span>

<span data-ttu-id="371a8-110">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="371a8-110">This switch has no parameters.</span></span>

 

 




