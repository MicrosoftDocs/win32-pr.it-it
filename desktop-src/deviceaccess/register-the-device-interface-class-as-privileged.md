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
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a>Registrare l'interfaccia del dispositivo come limitata alle app con privilegi

Alle applicazioni viene negato l'accesso alla funzionalità di driver personalizzata, a meno che non vengano concesse le autorizzazioni tramite i metadati dei dispositivi firmati. In questo argomento viene illustrato come aggiungere la proprietà **Restricted** che indica che solo le app con privilegi possono accedere a una classe di interfaccia del dispositivo. I driver di dispositivo personalizzati devono disporre di questa proprietà.

## <a name="instructions"></a>Istruzioni

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a>Impostazione della proprietà Restricted in un file di informazioni (INF)

Nella `InterfaceInstall32` sezione viene registrato il GUID della classe di interfaccia del dispositivo.

Le righe sotto la direttiva **AddProperty** impostano le proprietà della classe del dispositivo. La seconda riga imposta una proprietà personalizzata in una categoria di proprietà personalizzata. Il GUID della categoria proprietà è **14c83a99-0b3f-44b7-BE4C-a178d3990564** e l'identificatore di proprietà è **2**. Il `Flags` valore di immissione facoltativo non è presente e il tipo è **17** (**DEVPROP_TYPE_BOOLEAN**). Il valore della proprietà è **1**.

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

## <a name="remarks"></a>Commenti

Al posto della direttiva **AddInterface** , il driver può anche chiamare la routine [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) per registrare la classe dell'interfaccia del dispositivo.

È anche possibile impostare la proprietà di interfaccia limitata chiamando la routine [**IoSetDeviceInterfacePropertyData**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) .

## <a name="related-topics"></a>Argomenti correlati

[Esempio di accesso ai driver personalizzato](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [hardware Dev Center](/windows-hardware/drivers/)
