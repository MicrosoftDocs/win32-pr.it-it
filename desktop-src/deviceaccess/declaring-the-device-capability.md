---
title: Dichiarazione della funzionalità del dispositivo
description: In questo argomento viene illustrato come dichiarare il GUID della funzionalità del dispositivo.
ms.assetid: C663F8D2-2CB6-4C3C-A1EB-A3D93AA71FC8
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 0b1f98717c7e9487874aa71691beefbac635660a
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "103963544"
---
# <a name="declaring-the-device-capability"></a><span data-ttu-id="6ec30-103">Dichiarazione della funzionalità del dispositivo</span><span class="sxs-lookup"><span data-stu-id="6ec30-103">Declaring the Device Capability</span></span>

<span data-ttu-id="6ec30-104">In questo argomento viene illustrato come dichiarare il GUID della funzionalità del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ec30-104">This topic explains how to declare the device capability GUID.</span></span> <span data-ttu-id="6ec30-105">Tutte le applicazioni destinate a driver personalizzati devono dichiarare questa funzionalità.</span><span class="sxs-lookup"><span data-stu-id="6ec30-105">All applications that target custom drivers must declare this capability.</span></span>

<span data-ttu-id="6ec30-106">Nel manifesto dell'applicazione è necessario aggiungere una funzionalità del dispositivo, come indicato di seguito:</span><span class="sxs-lookup"><span data-stu-id="6ec30-106">In your application manifest, you'll need to add a device capability, as follows:</span></span>

<span data-ttu-id="6ec30-107">Questo è un esempio di dichiarazione di funzionalità per un dispositivo personalizzato.</span><span class="sxs-lookup"><span data-stu-id="6ec30-107">This is an example of a capability declaration for a custom device.</span></span> <span data-ttu-id="6ec30-108">Il GUID è il GUID della classe di interfaccia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="6ec30-108">The GUID is the GUID of the device interface class.</span></span>

```XML
<DeviceCapability Name="0B1F1048-B64B-FC9A-CED7-7E4FED3A0DEB" />
```

## <a name="related-topics"></a><span data-ttu-id="6ec30-109">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="6ec30-109">Related topics</span></span>

<span data-ttu-id="6ec30-110">[Esempio di accesso ai driver personalizzato](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [hardware Dev Center](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="6ec30-110">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
