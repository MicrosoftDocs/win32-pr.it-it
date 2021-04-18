---
description: Eventi di estensione MTP
ms.assetid: c04554cd-d68d-455e-afa3-29d4186dad65
title: Eventi di estensione MTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 10389df9105615befa9ba0f32824615977cc3cb7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319085"
---
# <a name="mtp-extension-events"></a><span data-ttu-id="372e4-103">Eventi di estensione MTP</span><span class="sxs-lookup"><span data-stu-id="372e4-103">MTP Extension Events</span></span>

<span data-ttu-id="372e4-104">Gli eventi notificano a un'applicazione che si sono verificate modifiche in o con un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="372e4-104">Events notify an application that changes have occurred on, or with, a device.</span></span> <span data-ttu-id="372e4-105">Ad esempio, un'applicazione può registrarsi per ricevere notifica che un dispositivo è stato rimosso.</span><span class="sxs-lookup"><span data-stu-id="372e4-105">For example, an application can register to receive notfications that a device has been removed .</span></span>

## <a name="vendor-extended-event-codes"></a><span data-ttu-id="372e4-106">Fornitori-codici evento esteso</span><span class="sxs-lookup"><span data-stu-id="372e4-106">Vendor-Extended Event Codes</span></span>

<span data-ttu-id="372e4-107">Quando un produttore di dispositivi supporta un evento esteso del fornitore, il driver combina il codice evento (UINT16) del fornitore con i 16 bit più alti del GUID degli **\_ \_ \_ \_ \_ eventi estesi del fornitore dell'evento MTP WPD** .</span><span class="sxs-lookup"><span data-stu-id="372e4-107">When a device manufacturer supports a vendor-extended event, their driver combines the vendor's event code (UINT16) with the highest 16 bits of the **WPD\_EVENT\_MTP\_VENDOR\_EXTENDED\_EVENTS** GUID.</span></span>

<span data-ttu-id="372e4-108">Se, ad esempio, il codice esteso del fornitore è 0xC001, il GUID risultante sarà come illustrato nell'esempio seguente:</span><span class="sxs-lookup"><span data-stu-id="372e4-108">For example, if the vendor-extended code is 0xC001, the resulting GUID would be as shown in the following example:</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="vendor-extended-event-parameters"></a><span data-ttu-id="372e4-109">Fornitori-parametri eventi estesi</span><span class="sxs-lookup"><span data-stu-id="372e4-109">Vendor-Extended Event Parameters</span></span>

<span data-ttu-id="372e4-110">I parametri per un evento di fornitore esteso vengono segnalati dal **parametro di evento WPD \_ \_ \_ \_ ID** GUID e la **\_ Proprietà WPD \_ MTP \_ ext \_ Event \_ params**, che è una raccolta di **PROPVARIANTS**.</span><span class="sxs-lookup"><span data-stu-id="372e4-110">The parameters for a vendor-extended event are reported by the **WPD\_EVENT\_PARAMETER\_EVENT\_ID** GUID and the **WPD\_PROPERTY\_MTP\_EXT\_EVENT\_PARAMS**, which is a collection of **PROPVARIANTS**.</span></span> <span data-ttu-id="372e4-111">Questi **PROPVARIANTS** corrispondono ai parametri dell'evento.</span><span class="sxs-lookup"><span data-stu-id="372e4-111">These **PROPVARIANTS** correspond to the event parameters.</span></span> <span data-ttu-id="372e4-112">Se non sono presenti parametri, questa raccolta è vuota.</span><span class="sxs-lookup"><span data-stu-id="372e4-112">If there are no parameters, this collection is empty.</span></span>


```C++
{C0010000-5738-4ff2-8445-BE3126691059}
```



## <a name="related-topics"></a><span data-ttu-id="372e4-113">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="372e4-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="372e4-114">Supporto delle estensioni MTP</span><span class="sxs-lookup"><span data-stu-id="372e4-114">Supporting MTP Extensions</span></span>](supporting-mtp-extensions.md)
</dt> </dl>

 

 



