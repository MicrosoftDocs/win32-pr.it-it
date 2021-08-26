---
title: Registrare l'interfaccia del dispositivo come limitata alle app con privilegi
description: Questo argomento illustra come aggiungere la proprietà Restricted che indica che solo le app con privilegi possono accedere a una classe di interfaccia del dispositivo.
ms.assetid: BCEB1FBF-3D3F-45B8-A92B-7C5FBF6745C0
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 62bca034a2edab9b31267f14672b4821ca6569dead0fd645d98c52c234c24cb6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029051"
---
# <a name="register-the-device-interface-as-restricted-to-privileged-apps"></a>Registrare l'interfaccia del dispositivo come limitata alle app con privilegi

Alle applicazioni viene negato l'accesso alla funzionalità del driver personalizzato, a meno che non vengano concesse autorizzazioni tramite i metadati del dispositivo firmato. Questo argomento illustra come aggiungere la **proprietà Restricted** che indica che solo le app con privilegi possono accedere a una classe di interfaccia del dispositivo. I driver di dispositivo personalizzati devono avere questa proprietà.

## <a name="instructions"></a>Istruzioni

### <a name="setting-the-restricted-property-in-an-information-inf-file"></a>Impostazione della proprietà Restricted in un file di informazioni (INF)

Nella sezione `InterfaceInstall32` viene registrato il GUID della classe dell'interfaccia del dispositivo.

Le righe nella direttiva **AddProperty** impostano le proprietà della classe del dispositivo. La seconda riga imposta una proprietà personalizzata in una categoria di proprietà personalizzate. Il GUID della categoria di proprietà **è 14c83a99-0b3f-44b7-be4c-a178d3990564** e l'identificatore della proprietà **è 2**. Il valore `Flags` di voce facoltativo non è presente e il tipo è **17** (**DEVPROP_TYPE_BOOLEAN**). Il valore della proprietà è **1**.

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

Invece della direttiva **AddInterface,** il driver può anche chiamare la routine [**IoRegisterDeviceInterface**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata) per registrare la classe dell'interfaccia di dispositivo.

È anche possibile impostare la proprietà dell'interfaccia con restrizioni chiamando la routine [**IoSetDeviceInterfacePropertyData.**](/windows-hardware/drivers/ddi/wdm/nf-wdm-iosetdeviceinterfacepropertydata)

## <a name="related-topics"></a>Argomenti correlati

[Esempio di accesso al driver personalizzato,](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample) [app per dispositivi UWP per dispositivi interni,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Hardware Dev Center](/windows-hardware/drivers/)
