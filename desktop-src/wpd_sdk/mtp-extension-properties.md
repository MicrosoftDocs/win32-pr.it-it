---
description: Proprietà estensione MTP
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: Proprietà estensione MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313899"
---
# <a name="mtp-extension-properties"></a><span data-ttu-id="00b73-103">Proprietà estensione MTP</span><span class="sxs-lookup"><span data-stu-id="00b73-103">MTP Extension Properties</span></span>

<span data-ttu-id="00b73-104">Le proprietà descrivono oggetti, proprietà, risorse e dispositivi.</span><span class="sxs-lookup"><span data-stu-id="00b73-104">Properties describe objects, properties, resources, and devices.</span></span>

## <a name="vendor-extended-object-properties"></a><span data-ttu-id="00b73-105">Proprietà degli oggetti estesi del fornitore</span><span class="sxs-lookup"><span data-stu-id="00b73-105">Vendor-Extended Object Properties</span></span>

<span data-ttu-id="00b73-106">Quando un produttore di dispositivi crea una proprietà estesa dal fornitore per un oggetto dispositivo, combina le **\_ Proprietà WPD proprietà \_ MTP \_ fornitore \_ esteso \_ oggetto \_ Props** GUID con il codice di proprietà dell'oggetto per costruire una struttura **PropertyKey** .</span><span class="sxs-lookup"><span data-stu-id="00b73-106">When a device manufacturer creates a vendor-extended property for a device object, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_OBJECT\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="00b73-107">Se, ad esempio, il codice della proprietà dell'oggetto è 0xD801, il **PropertyKey** risultante sarà come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="00b73-107">For example, if the object's property code is 0xD801, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a><span data-ttu-id="00b73-108">Proprietà del dispositivo esteso del fornitore</span><span class="sxs-lookup"><span data-stu-id="00b73-108">Vendor-Extended Device Properties</span></span>

<span data-ttu-id="00b73-109">Quando un produttore di dispositivi crea una proprietà estesa dal fornitore per un dispositivo, combina le **\_ Proprietà WPD \_ MTP \_ Vendor \_ Extended \_ Device \_ Props** GUID con il codice di proprietà dell'oggetto per costruire una struttura **PropertyKey** .</span><span class="sxs-lookup"><span data-stu-id="00b73-109">When a device manufacturer creates a vendor-extended property for a device, they combine the **WPD\_PROPERTIES\_MTP\_VENDOR\_EXTENDED\_DEVICE\_PROPS** GUID with the object's property code to construct a **PROPERTYKEY** structure.</span></span>

<span data-ttu-id="00b73-110">Se, ad esempio, il codice della proprietà dell'oggetto è 0xD001, il **PropertyKey** risultante sarà come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="00b73-110">For example, if the object's property code is 0xD001, the resulting **PROPERTYKEY** would be as shown in the following example:</span></span>


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a><span data-ttu-id="00b73-111">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="00b73-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="00b73-112">Supporto delle estensioni MTP</span><span class="sxs-lookup"><span data-stu-id="00b73-112">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



