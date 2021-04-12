---
description: Usare il codice seguente per impostare la frequenza di callback.
ms.assetid: fdcad3c2-7e36-4194-83c7-dccbd50762d5
title: Impostazione della frequenza di callback
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e03c260b6d289e473f27bb3ae6b84a3f42d0878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343866"
---
# <a name="setting-the-callback-frequency"></a><span data-ttu-id="b1d69-103">Impostazione della frequenza di callback</span><span class="sxs-lookup"><span data-stu-id="b1d69-103">Setting the Callback Frequency</span></span>

<span data-ttu-id="b1d69-104">Usare il codice seguente per impostare la frequenza di callback:</span><span class="sxs-lookup"><span data-stu-id="b1d69-104">Use the following code to set the callback frequency:</span></span>

<span data-ttu-id="b1d69-105">**DWORD** Valore = 1;</span><span class="sxs-lookup"><span data-stu-id="b1d69-105">**DWORD** Value = 1;</span></span>


```C++
rc = SetDwordInBlob(hNPPBlob, OWNER_NPP, CATEGORY_CONFIG,
                    TAG_UPDATE_FREQUENCY, Value);
```



<span data-ttu-id="b1d69-106">Questo frammento di codice imposta la frequenza di callback su 1 secondo (valore minimo).</span><span class="sxs-lookup"><span data-stu-id="b1d69-106">This code fragment sets the callback frequency to 1 second (the minimum value).</span></span> <span data-ttu-id="b1d69-107">Il valore massimo deve essere molto maggiore di 1.</span><span class="sxs-lookup"><span data-stu-id="b1d69-107">The maximum value must be much larger than 1.</span></span> <span data-ttu-id="b1d69-108">Se il buffer del provider di pacchetti di rete (NPP) è pieno, l'oggetto NPP chiama prima il monitoraggio.</span><span class="sxs-lookup"><span data-stu-id="b1d69-108">If the network packet provider (NPP) buffer is full, the NPP calls the monitor back sooner.</span></span>

 

 



