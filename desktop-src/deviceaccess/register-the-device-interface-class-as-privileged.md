---
title: Registrare l'interfaccia del dispositivo come limitata alle app con privilegi
description: In questo argomento viene illustrato come aggiungere la proprietà Restricted che indica che solo le app con privilegi possono accedere a una classe di interfaccia del dispositivo.
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: e23f8b7f2cc1884e2f878739f56507e79eb1bb69
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047558"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a><span data-ttu-id="c4d00-103">Registrare l'interfaccia del dispositivo come limitata alle app con privilegi</span><span class="sxs-lookup"><span data-stu-id="c4d00-103">Register the device interface as restricted to privileged apps</span></span>

<span data-ttu-id="c4d00-104">Alle applicazioni viene negato l'accesso alla funzionalità di driver personalizzata, a meno che non vengano concesse le autorizzazioni tramite i metadati dei dispositivi firmati.</span><span class="sxs-lookup"><span data-stu-id="c4d00-104">Applications are denied access to custom driver functionality, unless they're granted permissions through signed device metadata.</span></span> <span data-ttu-id="c4d00-105">In questo argomento viene illustrato come aggiungere la proprietà **Restricted** che indica che solo le app con privilegi possono accedere a una classe di interfaccia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4d00-105">This topic shows how to add the **Restricted** property that indicates that only privileged apps can access a device interface class.</span></span> <span data-ttu-id="c4d00-106">I driver di dispositivo personalizzati devono disporre di questa proprietà.</span><span class="sxs-lookup"><span data-stu-id="c4d00-106">Custom device drivers must have this property.</span></span>

## <a name="instructions"></a><span data-ttu-id="c4d00-107">Istruzioni</span><span class="sxs-lookup"><span data-stu-id="c4d00-107">Instructions</span></span>

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a><span data-ttu-id="c4d00-108">Impostazione della proprietà Restricted in un file di informazioni (INF)</span><span class="sxs-lookup"><span data-stu-id="c4d00-108">Setting the Restricted property in an information (INF) file</span></span>

<span data-ttu-id="c4d00-109">Nella `InterfaceInstall32` sezione viene registrato il GUID della classe di interfaccia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4d00-109">In the `InterfaceInstall32` section, the GUID of the device interface class is registered.</span></span>

<span data-ttu-id="c4d00-110">Le righe sotto la direttiva **AddProperty** impostano le proprietà della classe del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4d00-110">The lines under the **AddProperty** directive set the device class properties.</span></span> <span data-ttu-id="c4d00-111">La seconda riga imposta una proprietà personalizzata in una categoria di proprietà personalizzata.</span><span class="sxs-lookup"><span data-stu-id="c4d00-111">The second line sets a custom property in a custom property category.</span></span> <span data-ttu-id="c4d00-112">Il GUID della categoria proprietà è **14c83a99-0b3f-44b7-BE4C-a178d3990564** e l'identificatore di proprietà è **2**.</span><span class="sxs-lookup"><span data-stu-id="c4d00-112">The property-category GUID is **14c83a99-0b3f-44b7-be4c-a178d3990564**, and the property identifier is **2**.</span></span> <span data-ttu-id="c4d00-113">Il `Flags` valore di immissione facoltativo non è presente e il tipo è **17** (**DEVPROP_TYPE_BOOLEAN**).</span><span class="sxs-lookup"><span data-stu-id="c4d00-113">The optional `Flags` entry value is not present, and the type is **17** (**DEVPROP_TYPE_BOOLEAN**).</span></span> <span data-ttu-id="c4d00-114">Il valore della proprietà è **1**.</span><span class="sxs-lookup"><span data-stu-id="c4d00-114">The value of the property is **1**.</span></span>

```Text
; Below, {11111111-0000-1111-0000-111111111111} is the GUID of the
; new device interface class in an AddInterface directive



; -- Interface installation
[InterfaceInstall32]
{11111111-0000-1111-0000-111111111111}=NewInterfaceInstall

[NewInterfaceInstall]
AddProperty=PrivilegedProperties

[PrivilegedProperties]
; DEVPKey_DeviceInterfaceClass_Restricted
{14c83a99-0b3f-44b7-be4c-a178d3990564}, 2, 17,,1 ; -- non-zero indicates privileged
```

## <a name="remarks"></a><span data-ttu-id="c4d00-115">Commenti</span><span class="sxs-lookup"><span data-stu-id="c4d00-115">Remarks</span></span>

<span data-ttu-id="c4d00-116">Al posto della direttiva **AddInterface** , il driver può anche chiamare la routine [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) per registrare la classe dell'interfaccia del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="c4d00-116">Instead of the **AddInterface** directive, the driver can also call the [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine to register the device interface class.</span></span>

<span data-ttu-id="c4d00-117">È anche possibile impostare la proprietà di interfaccia limitata chiamando la routine [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) .</span><span class="sxs-lookup"><span data-stu-id="c4d00-117">You can also set the restricted interface property by calling the [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) routine.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c4d00-118">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="c4d00-118">Related topics</span></span>

<span data-ttu-id="c4d00-119">[Esempio di accesso ai driver personalizzato](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [hardware Dev Center](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="c4d00-119">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
