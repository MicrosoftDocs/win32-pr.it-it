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
# <a name="com-interfaces---device-access"></a><span data-ttu-id="dc37b-103">Interfacce COM-accesso ai dispositivi</span><span class="sxs-lookup"><span data-stu-id="dc37b-103">COM Interfaces - Device Access</span></span>

<span data-ttu-id="dc37b-104">Interfacce di Component Object Model (COM) nell'API di accesso ai dispositivi.</span><span class="sxs-lookup"><span data-stu-id="dc37b-104">Component Object Model (COM)interfaces in the Device Access API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="dc37b-105">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="dc37b-105">In this section</span></span>

| <span data-ttu-id="dc37b-106">Argomento</span><span class="sxs-lookup"><span data-stu-id="dc37b-106">Topic</span></span> | <span data-ttu-id="dc37b-107">Descrizione</span><span class="sxs-lookup"><span data-stu-id="dc37b-107">Description</span></span> |
|---|---|
| [<span data-ttu-id="dc37b-108">**ICreateDeviceAccessAsync**</span><span class="sxs-lookup"><span data-stu-id="dc37b-108">**ICreateDeviceAccessAsync**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync)<br/> | <span data-ttu-id="dc37b-109">L'interfaccia [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) viene restituita da una chiamata a CreateDeviceAccessInstance.</span><span class="sxs-lookup"><span data-stu-id="dc37b-109">The [**ICreateDeviceAccessAsync**](/windows/win32/api/Deviceaccess/nn-deviceaccess-icreatedeviceaccessasync) interface is returned from a call to CreateDeviceAccessInstance.</span></span> <span data-ttu-id="dc37b-110">Consente al chiamante di controllare l'operazione di associazione a un'istanza di un dispositivo per recuperare un'altra interfaccia che può essere usata per interagire con tale dispositivo.</span><span class="sxs-lookup"><span data-stu-id="dc37b-110">It enables the caller to control the operation of binding to an instance of a device in order to retrieve another interface that can be used to interact with that device.</span></span><br/> |
| [<span data-ttu-id="dc37b-111">**IDeviceIoControl**</span><span class="sxs-lookup"><span data-stu-id="dc37b-111">**IDeviceIoControl**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-ideviceiocontrol)<br/> | <span data-ttu-id="dc37b-112">Invia un codice di controllo a un driver di dispositivo. Questa azione consente al dispositivo di eseguire l'operazione corrispondente.</span><span class="sxs-lookup"><span data-stu-id="dc37b-112">Sends a control code to a device driver.This action causes the device to perform the corresponding operation.</span></span> <br/> |
| [<span data-ttu-id="dc37b-113">**IDeviceRequestCompletionCallback**</span><span class="sxs-lookup"><span data-stu-id="dc37b-113">**IDeviceRequestCompletionCallback**</span></span>](/windows/win32/api/Deviceaccess/nn-deviceaccess-idevicerequestcompletioncallback)<br/> | <span data-ttu-id="dc37b-114">Fornisce un metodo per gestire il completamento delle chiamate al metodo [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync).</span><span class="sxs-lookup"><span data-stu-id="dc37b-114">Provides a method to handle the completion of calls to the [**DeviceIoControlAsync**](/windows/win32/api/Deviceaccess/nf-deviceaccess-ideviceiocontrol-deviceiocontrolasync)method.</span></span><br/> |

## <a name="related-topics"></a><span data-ttu-id="dc37b-115">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="dc37b-115">Related topics</span></span>

<span data-ttu-id="dc37b-116">[Esempio di accesso ai driver personalizzato](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [app per dispositivi UWP per dispositivi interni](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [hardware Dev Center](/windows-hardware/drivers/)</span><span class="sxs-lookup"><span data-stu-id="dc37b-116">[Custom Driver Access Sample](https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Custom%20driver%20access%20sample), [UWP device apps for internal devices](/windows-hardware/drivers/devapps/uwp-device-apps-for-specialized-devices), [Hardware Dev Center](/windows-hardware/drivers/)</span></span>
