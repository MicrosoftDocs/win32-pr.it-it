---
description: L'interfaccia IWiaPropertyStorage fornisce metodi per la lettura e la scrittura delle proprietà di un elemento di acquisizione immagini Windows (WIA). Le proprietà dell'elemento includono comandi del dispositivo, informazioni sul formato dell'elemento e informazioni sul dispositivo.
ms.assetid: 268d2298-bc9c-479b-b078-a8180cd38bc3
title: Lettura e impostazione delle proprietà WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51df3e8fdb4b29abb6f64743ab8f7f2dd3776358
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129402"
---
# <a name="reading-and-setting-wia-properties"></a><span data-ttu-id="1b657-104">Lettura e impostazione delle proprietà WIA</span><span class="sxs-lookup"><span data-stu-id="1b657-104">Reading and Setting WIA Properties</span></span>

<span data-ttu-id="1b657-105">L'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) fornisce metodi per la lettura e la scrittura delle proprietà di un elemento di acquisizione immagini Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="1b657-105">The [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface provides methods for reading and writing a Windows Image Acquisition (WIA) item's properties.</span></span> <span data-ttu-id="1b657-106">Le proprietà dell'elemento includono comandi del dispositivo, informazioni sul formato dell'elemento e informazioni sul dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1b657-106">Item properties include device commands, item format information, and device information.</span></span>

<span data-ttu-id="1b657-107">Un'applicazione può ottenere un puntatore a un'interfaccia [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) di un elemento enumerando le informazioni sul dispositivo dell'elemento o le informazioni sull'evento chiamando [**IWiaItem:: EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) o [**IWiaItem:: EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) o eseguendo una query sull'interfaccia [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) dell'elemento.</span><span class="sxs-lookup"><span data-stu-id="1b657-107">An application can obtain a pointer to an [**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) interface of an item either by enumerating the item's device information or event information by calling [**IWiaItem::EnumDeviceCapabilities**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumdevicecapabilities) or [**IWiaItem::EnumRegisterEventInfo**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-enumregistereventinfo) or by querying the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) interface of the item.</span></span> <span data-ttu-id="1b657-108">(In WIA 2,0, effettuare questa operazione chiamando [**IWiaItem2:: EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) o [**IWiaItem2:: EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) o eseguendo una query sull'interfaccia [**IWiaItem2**](-wia-iwiaitem2.md) dell'elemento).</span><span class="sxs-lookup"><span data-stu-id="1b657-108">(In WIA 2.0, do this by calling [**IWiaItem2::EnumDeviceCapabilities**](-wia-iwiaitem2-enumdevicecapabilities.md) or [**IWiaItem2::EnumRegisterEventInfo**](-wia-iwiaitem2-enumregistereventinfo.md) or by querying the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the item.)</span></span>

<span data-ttu-id="1b657-109">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) eredita da [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) e i metodi ereditati vengono implementati come descritto nella sezione di riferimento di archiviazione strutturata in Windows Software Development Kit (SDK).</span><span class="sxs-lookup"><span data-stu-id="1b657-109">[**IWiaPropertyStorage**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage) inherits from [IPropertyStorage](/windows/win32/api/propidlbase/nn-propidlbase-ipropertystorage) and the inherited methods are implemented as described in the reference section of Structured Storage in the Windows Software Development Kit (SDK).</span></span>

> [!Note]
>
> <span data-ttu-id="1b657-110">Le applicazioni WIA devono leggere sempre le intestazioni dei dati dell'immagine per ottenere informazioni accurate sulle immagini.</span><span class="sxs-lookup"><span data-stu-id="1b657-110">WIA applications should always read image data headers for accurate image information.</span></span> <span data-ttu-id="1b657-111">Il driver WIA può modificare le proprietà WIA e le intestazioni dei dati di immagine durante il trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="1b657-111">The WIA driver can alter the WIA properties and image data headers during data transfer.</span></span>
>
> <span data-ttu-id="1b657-112">Se non è presente alcuna intestazione dati immagine fornita con il formato specificato, l'applicazione WIA deve usare le proprietà WIA come origine informazioni sul trasferimento dei dati.</span><span class="sxs-lookup"><span data-stu-id="1b657-112">If there is no image data header supplied with the specified format, the WIA application should use the WIA properties as an information source about the data transfer.</span></span> <span data-ttu-id="1b657-113">L'applicazione WIA deve rileggere le proprietà WIA necessarie dopo il completamento dell'analisi o dell'acquisizione per ottenere le impostazioni aggiornate.</span><span class="sxs-lookup"><span data-stu-id="1b657-113">The WIA application should reread the needed WIA properties after the scan or capture completes to get the updated settings.</span></span>

 

<span data-ttu-id="1b657-114">Le sezioni seguenti descrivono le varie proprietà WIA:</span><span class="sxs-lookup"><span data-stu-id="1b657-114">The following sections describe the various WIA properties:</span></span>

-   [<span data-ttu-id="1b657-115">Convalida della proprietà WIA</span><span class="sxs-lookup"><span data-stu-id="1b657-115">WIA Property Validation</span></span>](-wia-wia-property-validation.md)
-   [<span data-ttu-id="1b657-116">Proprietà informazioni sul dispositivo</span><span class="sxs-lookup"><span data-stu-id="1b657-116">Device Information Properties</span></span>](-wia-device-information-properties-wia-dip-xxxx.md)
-   [<span data-ttu-id="1b657-117">Proprietà dispositivo</span><span class="sxs-lookup"><span data-stu-id="1b657-117">Device Properties</span></span>](-wia-device-properties.md)
-   [<span data-ttu-id="1b657-118">Proprietà degli elementi</span><span class="sxs-lookup"><span data-stu-id="1b657-118">Item Properties</span></span>](-wia-item-properties.md)
-   [<span data-ttu-id="1b657-119">Proprietà WIA aggiuntive</span><span class="sxs-lookup"><span data-stu-id="1b657-119">Additional WIA Properties</span></span>](-wia-additional-wia-properties.md)
-   [<span data-ttu-id="1b657-120">Definizione di proprietà personalizzate</span><span class="sxs-lookup"><span data-stu-id="1b657-120">Defining Custom Properties</span></span>](-wia-defining-custom-properties.md)
-   [<span data-ttu-id="1b657-121">Utilizzo di proprietà personalizzate</span><span class="sxs-lookup"><span data-stu-id="1b657-121">Using Custom Properties</span></span>](-wia-using-custom-properties.md)
-   [<span data-ttu-id="1b657-122">Schema del profilo di analisi</span><span class="sxs-lookup"><span data-stu-id="1b657-122">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)

 

 
