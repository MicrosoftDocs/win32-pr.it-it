---
title: Callback Bluetooth
description: Le funzioni di callback Bluetooth in questa sezione vengono usate in combinazione con funzioni che consentono di gestire i dispositivi e i servizi Bluetooth.
ms.assetid: a66f88e2-46f7-4e23-9b61-7ee35abec207
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1afe99dc3fe1bee8f133cddae0e319e6354077e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103708113"
---
# <a name="bluetooth-callbacks"></a><span data-ttu-id="5b355-103">Callback Bluetooth</span><span class="sxs-lookup"><span data-stu-id="5b355-103">Bluetooth Callbacks</span></span>

<span data-ttu-id="5b355-104">Le funzioni di callback Bluetooth in questa sezione vengono usate in combinazione con funzioni che consentono di gestire i dispositivi e i servizi Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="5b355-104">The Bluetooth callback functions in this section are used in combination with functions that make it possible to manage Bluetooth devices and services.</span></span>

<span data-ttu-id="5b355-105">Bluetooth è supportato anche tramite l'interfaccia di programmazione Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="5b355-105">Bluetooth is also supported by using the Windows Sockets programming interface.</span></span> <span data-ttu-id="5b355-106">Per ulteriori informazioni sulla programmazione di Bluetooth utilizzando l'interfaccia Windows Sockets, vedere [supporto di Windows Sockets per Bluetooth](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="5b355-106">For more information about programming Bluetooth by using the Windows Sockets interface, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>



| <span data-ttu-id="5b355-107">Sezione</span><span class="sxs-lookup"><span data-stu-id="5b355-107">Section</span></span>                                                                                      | <span data-ttu-id="5b355-108">Content</span><span class="sxs-lookup"><span data-stu-id="5b355-108">Content</span></span>                                                                                                                                                                  |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5b355-109">**\_callback di autenticazione PFN \_**</span><span class="sxs-lookup"><span data-stu-id="5b355-109">**PFN\_AUTHENTICATION\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback)                         | <span data-ttu-id="5b355-110">Utilizzato in combinazione con la funzione [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .</span><span class="sxs-lookup"><span data-stu-id="5b355-110">Used in conjunction with the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function.</span></span>                                                  |
| [<span data-ttu-id="5b355-111">**\_esempio di \_ callback di autenticazione PFN \_**</span><span class="sxs-lookup"><span data-stu-id="5b355-111">**PFN\_AUTHENTICATION\_CALLBACK\_EX**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_authentication_callback_ex)                  | <span data-ttu-id="5b355-112">Utilizzato in combinazione con la funzione [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) .</span><span class="sxs-lookup"><span data-stu-id="5b355-112">Used in conjunction with the [**BluetoothRegisterForAuthenticationEx**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthenticationex) function.</span></span>                                              |
| [<span data-ttu-id="5b355-113">**\_callback degli \_ attributi di enumerazione Bluetooth \_ PFN \_**</span><span class="sxs-lookup"><span data-stu-id="5b355-113">**PFN\_BLUETOOTH\_ENUM\_ATTRIBUTES\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_bluetooth_enum_attributes_callback) | <span data-ttu-id="5b355-114">Viene chiamato una volta per ogni attributo trovato nel parametro *pSDPStream* passato alla chiamata di funzione [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) .</span><span class="sxs-lookup"><span data-stu-id="5b355-114">Called once for each attribute found in the *pSDPStream* parameter that is passed to the [**BluetoothSdpEnumAttributes**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothsdpenumattributes) function call.</span></span> |
| [<span data-ttu-id="5b355-115">**\_callback del dispositivo PFN \_**</span><span class="sxs-lookup"><span data-stu-id="5b355-115">**PFN\_DEVICE\_CALLBACK**</span></span>](/windows/desktop/api/BluetoothAPIs/nc-bluetoothapis-pfn_device_callback)                                         | <span data-ttu-id="5b355-116">Utilizzato in associazione alla selezione dei dispositivi Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="5b355-116">Used in association with selecting Bluetooth devices.</span></span>                                                                                                                    |



 

 

 




