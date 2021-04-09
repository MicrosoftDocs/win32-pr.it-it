---
title: Interfacce COM-accesso ai dispositivi
description: Interfacce di Component Object Model (COM) nell'API di accesso ai dispositivi.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 07abbfd15f8383bbbd9cd9d1f5fc4c9fb1f42b9e
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 10/20/2020
ms.locfileid: "104047557"
---
# <a name="com-interfaces---device-access"></a>Interfacce COM-accesso ai dispositivi

Interfacce di Component Object Model (COM) nell'API di accesso ai dispositivi.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|---|---|
| [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | L'interfaccia [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) viene restituita da una chiamata a CreateDeviceAccessInstance. Consente al chiamante di controllare l'operazione di associazione a un'istanza di un dispositivo per recuperare un'altra interfaccia che può essere usata per interagire con tale dispositivo.<br/> |
| [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | Invia un codice di controllo a un driver di dispositivo. Questa azione consente al dispositivo di eseguire l'operazione corrispondente. <br/> |
| [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | Fornisce un metodo per gestire il completamento delle chiamate al metodo [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync).<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Esempio di accesso ai driver personalizzato](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [hardware Dev Center](/windows-hardware/drivers/)
