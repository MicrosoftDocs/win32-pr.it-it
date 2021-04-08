---
title: opzione/savePP
description: Quando si specifica la direttiva/savePP, il compilatore MIDL non elimina l'output del preprocessore C/C++.
ms.assetid: 65a687a5-55ec-4e76-bcfc-38c0a317b85b
keywords:
- /savePP switch MIDL
topic_type:
- apiref
api_name:
- /savePP
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d3ab7032768cacfab6415548a09def453ab4f9
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/25/2019
ms.locfileid: "104045759"
---
# <a name="savepp-switch"></a><span data-ttu-id="09e39-104">opzione/savePP</span><span class="sxs-lookup"><span data-stu-id="09e39-104">/savePP switch</span></span>

<span data-ttu-id="09e39-105">Quando si specifica la direttiva **/savePP** , il compilatore MIDL non elimina l'output del preprocessore C/C++.</span><span class="sxs-lookup"><span data-stu-id="09e39-105">When the **/savePP** directive is specified, the MIDL compiler does not delete the output of the C/C++ preprocessor.</span></span>

``` syntax
midl /savePP
```

## <a name="switch-options"></a><span data-ttu-id="09e39-106">Opzioni switch</span><span class="sxs-lookup"><span data-stu-id="09e39-106">Switch Options</span></span>

<span data-ttu-id="09e39-107">Questa opzione non ha parametri.</span><span class="sxs-lookup"><span data-stu-id="09e39-107">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="09e39-108">Commenti</span><span class="sxs-lookup"><span data-stu-id="09e39-108">Remarks</span></span>

<span data-ttu-id="09e39-109">Questa opzione consente agli sviluppatori di discernere gli elementi analizzati dal compilatore MIDL ed è utile per il debug.</span><span class="sxs-lookup"><span data-stu-id="09e39-109">This switch enables developers to discern what is being parsed by the MIDL compiler, and is useful for debugging.</span></span> <span data-ttu-id="09e39-110">L'output del preprocessore viene scritto in uno o più file temporanei nella directory indicata dalla variabile di ambiente TEMP.</span><span class="sxs-lookup"><span data-stu-id="09e39-110">The output of the preprocessor is written to one or more temporary files in the directory indicated by the TEMP environment variable.</span></span> <span data-ttu-id="09e39-111">Il nome del file di output, o file, segue una convenzione di denominazione di MID \* . tmp.</span><span class="sxs-lookup"><span data-stu-id="09e39-111">The name of the output file, or files, follows a naming convention of MID\*.tmp.</span></span> <span data-ttu-id="09e39-112">Si noti che una singola compilazione può generare diversi flussi di input pre-elaborati. Ciò è dovuto al fatto che l'importazione di un file IDL, anziché l'utilizzo di **\# include**, comporta l'esecuzione di un preprocessore separato.</span><span class="sxs-lookup"><span data-stu-id="09e39-112">Note that a single compile may generate several preprocessed input streams; this is because importing an IDL file, as opposed to using **\#include**, causes a separate preprocessor run.</span></span>

## <a name="see-also"></a><span data-ttu-id="09e39-113">Vedi anche</span><span class="sxs-lookup"><span data-stu-id="09e39-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09e39-114">**/cpp \_ cmd**</span><span class="sxs-lookup"><span data-stu-id="09e39-114">**/cpp\_cmd**</span></span>](-cpp-cmd.md)
</dt> <dt>

[<span data-ttu-id="09e39-115">**/cpp \_ opt**</span><span class="sxs-lookup"><span data-stu-id="09e39-115">**/cpp\_opt**</span></span>](-cpp-opt.md)
</dt> <dt>

[<span data-ttu-id="09e39-116">/No \_ cpp,/nocpp</span><span class="sxs-lookup"><span data-stu-id="09e39-116">/no\_cpp, /nocpp</span></span>](-no-cpp-nocpp.md)
</dt> </dl>

 

 




