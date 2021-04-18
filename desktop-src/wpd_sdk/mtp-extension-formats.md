---
description: Formati di estensione MTP
ms.assetid: 318b7267-f4ba-43ad-aa24-8cfacf056558
title: Formati di estensione MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff86265e47071fce9fe523cfbb64f2e355ed541e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313900"
---
# <a name="mtp-extension-formats"></a><span data-ttu-id="70e0f-103">Formati di estensione MTP</span><span class="sxs-lookup"><span data-stu-id="70e0f-103">MTP Extension Formats</span></span>

<span data-ttu-id="70e0f-104">Il formato di un file in un dispositivo può essere descritto da un valore GUID.</span><span class="sxs-lookup"><span data-stu-id="70e0f-104">The format of a file on a device can be described by a GUID value.</span></span> <span data-ttu-id="70e0f-105">Questo valore viene specificato dalla proprietà del \_ formato dell'oggetto WPD \_ .</span><span class="sxs-lookup"><span data-stu-id="70e0f-105">This value is specified by the WPD\_OBJECT\_FORMAT property.</span></span>

## <a name="vendor-extended-formats"></a><span data-ttu-id="70e0f-106">Formati estesi fornitore</span><span class="sxs-lookup"><span data-stu-id="70e0f-106">Vendor-Extended Formats</span></span>

<span data-ttu-id="70e0f-107">Quando un produttore di dispositivi supporta un formato esteso dal fornitore, il driver combina il codice del formato del fornitore (UINT16) con i 16 bit più alti del GUID del **formato dell'oggetto WPD non \_ \_ \_ specificato** .</span><span class="sxs-lookup"><span data-stu-id="70e0f-107">When a device manufacturer supports a vendor-extended format, their driver combines the vendor's format code (UINT16) with the highest 16 bits of the **WPD\_OBJECT\_FORMAT\_UNSPECIFIED** GUID.</span></span>

<span data-ttu-id="70e0f-108">Se, ad esempio, il codice esteso del fornitore è 0xB001, il GUID risultante sarà come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="70e0f-108">For example, if the vendor-extended code is 0xB001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{B0010000-AE6C-4804-98BA-C57B46965FE7}
```



## <a name="related-topics"></a><span data-ttu-id="70e0f-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="70e0f-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70e0f-110">Supporto delle estensioni MTP</span><span class="sxs-lookup"><span data-stu-id="70e0f-110">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



