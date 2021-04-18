---
description: Utilizzo di proprietà personalizzate.
ms.assetid: 09b30c95-0ce2-401c-a4ae-99c801a2048a
title: Utilizzo di proprietà personalizzate
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eca9f8092afa5b8af22080b154fff79a32a6f304
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307324"
---
# <a name="using-custom-properties"></a><span data-ttu-id="46224-103">Utilizzo di proprietà personalizzate</span><span class="sxs-lookup"><span data-stu-id="46224-103">Using Custom Properties</span></span>

<span data-ttu-id="46224-104">**Utilizzo di proprietà personalizzate**.</span><span class="sxs-lookup"><span data-stu-id="46224-104">**Using Custom Properties**.</span></span>

<span data-ttu-id="46224-105">Un driver Windows Image Acquisition (WIA) può definire proprietà personalizzate.</span><span class="sxs-lookup"><span data-stu-id="46224-105">A Windows Image Acquisition (WIA) driver can define its own custom properties.</span></span> <span data-ttu-id="46224-106">I chiamanti possono modificare le proprietà personalizzate in modo analogo alle normali proprietà WIA.</span><span class="sxs-lookup"><span data-stu-id="46224-106">Callers can manipulate custom properties just as they would normal WIA properties.</span></span> <span data-ttu-id="46224-107">Tuttavia, solo l'applicazione o il modulo dell'interfaccia utente personalizzata può accedere a queste proprietà personalizzate.</span><span class="sxs-lookup"><span data-stu-id="46224-107">However, only your application or custom UI module can access these custom properties.</span></span>

<span data-ttu-id="46224-108">I driver WIA devono definire le proprietà personalizzate in modo da avere identificatori di proprietà di cui è stato spostato il \_ DEVPROP privato WIA \_ per le proprietà del dispositivo e usare \_ \_ il ITEMPROP privato WIA per le proprietà degli elementi normali, ad esempio all'interno di [IWiaMiniDrv::d rvinititemproperties](https://msdn.microsoft.com/library/ms794131.aspx).</span><span class="sxs-lookup"><span data-stu-id="46224-108">WIA drivers should define the custom properties to have property identifiers that are offset by WIA\_PRIVATE\_DEVPROP for device properties, and use WIA\_PRIVATE\_ITEMPROP for normal item properties, such as inside [IWiaMiniDrv::drvInitItemProperties](https://msdn.microsoft.com/library/ms794131.aspx).</span></span> <span data-ttu-id="46224-109">Per ulteriori informazioni, vedere [definizione delle proprietà personalizzate](-wia-defining-custom-properties.md).</span><span class="sxs-lookup"><span data-stu-id="46224-109">For more information, see [Defining Custom Properties](-wia-defining-custom-properties.md).</span></span>

<span data-ttu-id="46224-110">Esistono due modi per passare parametri personalizzati ai driver WIA.</span><span class="sxs-lookup"><span data-stu-id="46224-110">There are two ways to pass custom parameters to WIA drivers.</span></span>

<span data-ttu-id="46224-111">La prima opzione consiste nell'usare il metodo **IWiaItemExtras:: Escape** (descritto nella documentazione di Platform SDK).</span><span class="sxs-lookup"><span data-stu-id="46224-111">The first option is to use the **IWiaItemExtras::Escape** method (described in the Platform SDK documentation).</span></span> <span data-ttu-id="46224-112">Questa operazione è simile al metodo [IStiUSD:: Escape](https://msdn.microsoft.com/library/ms794396.aspx) , ma consente ai chiamanti di usare direttamente WIA, anziché usare i metodi STI.</span><span class="sxs-lookup"><span data-stu-id="46224-112">This is similar to the [IStiUSD::Escape](https://msdn.microsoft.com/library/ms794396.aspx) method, but it allows callers to use WIA directly, instead of using STI methods.</span></span> <span data-ttu-id="46224-113">Se si usa **IWiaItemExtras:: Escape**, è possibile passare qualsiasi informazione al driver e il driver può passare le informazioni.</span><span class="sxs-lookup"><span data-stu-id="46224-113">Using **IWiaItemExtras::Escape**, you can pass any information to the driver, and the driver can pass any information back.</span></span> <span data-ttu-id="46224-114">Il servizio WIA gestisce solo i buffer passati tra il chiamante e il driver.</span><span class="sxs-lookup"><span data-stu-id="46224-114">The WIA service manages only those buffers passed between the caller and the driver.</span></span>

<span data-ttu-id="46224-115">La seconda opzione consiste nell'usare proprietà personalizzate.</span><span class="sxs-lookup"><span data-stu-id="46224-115">The second option is to use custom properties.</span></span> <span data-ttu-id="46224-116">L'utilizzo del metodo **IWiaItemExtras:: Escape** è più flessibile rispetto all'utilizzo di proprietà WIA personalizzate, ma le proprietà WIA personalizzate consentono di archiviare le informazioni nel flusso di proprietà dell'elemento, in modo che il driver possa leggere le informazioni in un secondo momento.</span><span class="sxs-lookup"><span data-stu-id="46224-116">Using the **IWiaItemExtras::Escape** method is more flexible than using custom WIA properties, but custom WIA properties allow you to store information in the item's property stream so that the driver can read the information at another time.</span></span>

 

 



