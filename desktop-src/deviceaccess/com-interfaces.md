---
title: Interfacce COM - Accesso al dispositivo
description: Component Object Model interfacce (COM) nel API di accesso al dispositivo.
ms.assetid: 96F532B7-5CF9-4341-932B-7F8BEDA9551F
ms.topic: article
ms.date: 02/11/2020
ms.openlocfilehash: 22447151b944a2ac5515222eebd528fed11e2479d8a8c4db59e2da46dd07a130
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793386"
---
# <a name="com-interfaces---device-access"></a>Interfacce COM - Accesso al dispositivo

Component Object Model interfacce (COM) nel API di accesso al dispositivo.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento | Descrizione |
|---|---|
| [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | [**L'interfaccia ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) viene restituita da una chiamata a CreateDeviceAccessInstance. Consente al chiamante di controllare il funzionamento dell'associazione a un'istanza di un dispositivo per recuperare un'altra interfaccia che può essere usata per interagire con tale dispositivo.<br/> |
| [**IDeviceIoControl**](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | Invia un codice di controllo a un driver di dispositivo. Questa azione determina l'esecuzione dell'operazione corrispondente da parte del dispositivo. <br/> |
| [**IDeviceRequestCompletionCallback**](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | Fornisce un metodo per gestire il completamento delle chiamate al [**metodo DeviceIoControlAsync.**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)<br/> |

## <a name="related-topics"></a>Argomenti correlati

[Esempio di accesso al](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample)driver personalizzato, [app per dispositivi UWP per dispositivi interni,](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices) [Hardware Dev Center](/windows-hardware/drivers/)
