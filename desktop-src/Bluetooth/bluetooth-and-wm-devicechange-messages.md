---
title: Messaggi Bluetooth e WM_DEVICECHANGE
description: Bluetooth include \_ messaggi DEVICECHANGE WM specifici che consentono agli sviluppatori di ottenere messaggi quando i dispositivi Bluetooth subiscono modifiche di stato.
ms.assetid: 7dab37a6-63ac-4377-9884-61dd19972433
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d0fe553a91823850b8bc90164c9c79e4e58ed7f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103963170"
---
# <a name="bluetooth-and-wm_devicechange-messages"></a><span data-ttu-id="73e22-103">Messaggi Bluetooth e WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="73e22-103">Bluetooth and WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="73e22-104">Bluetooth include messaggi [**\_ DEVICECHANGE WM**](/windows/desktop/DevIO/wm-devicechange) specifici che consentono agli sviluppatori di ottenere messaggi quando i dispositivi Bluetooth subiscono modifiche di stato.</span><span class="sxs-lookup"><span data-stu-id="73e22-104">Bluetooth includes specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages that enable developers to obtain messages when Bluetooth devices undergo status changes.</span></span> <span data-ttu-id="73e22-105">Questo argomento descrive come ricevere messaggi **WM \_ DEVICECHANGE** specifici di Bluetooth ed elenca i messaggi specifici di Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="73e22-105">This topic describes how to receive Bluetooth-specific **WM\_DEVICECHANGE** messages and lists Bluetooth-specific messages.</span></span>

## <a name="receiving-bluetooth-specific-wm_devicechange-messages"></a><span data-ttu-id="73e22-106">Ricezione di messaggi WM DEVICECHANGE specifici per Bluetooth \_</span><span class="sxs-lookup"><span data-stu-id="73e22-106">Receiving Bluetooth-specific WM\_DEVICECHANGE Messages</span></span>

<span data-ttu-id="73e22-107">Per ricevere i messaggi [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) , è necessario innanzitutto aprire un handle per la radio locale.</span><span class="sxs-lookup"><span data-stu-id="73e22-107">To receive [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages, a handle to the local radio must first be opened.</span></span> <span data-ttu-id="73e22-108">A tale scopo, adottare uno dei metodi seguenti:</span><span class="sxs-lookup"><span data-stu-id="73e22-108">To do this, use one of the following methods:</span></span>

-   <span data-ttu-id="73e22-109">Usare la funzione [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) con i parametri seguenti: ( \_ interfaccia del dispositivo GUID bthport \_ \_ ,..., DIGCF \_ presente \| DIGCF \_ DEVICEINTERFACE), quindi usare le funzioni [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)e [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) .</span><span class="sxs-lookup"><span data-stu-id="73e22-109">Use the [SetupDiGetClassDevs](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw) function with the following parameters: (GUID\_BTHPORT\_DEVICE\_INTERFACE, …, DIGCF\_PRESENT \| DIGCF\_DEVICEINTERFACE), then use the [SetupDiEnumDeviceInterfaces](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces), [SetupDiGetDeviceInterfaceDetail](https://msdn.microsoft.com/library/ms792901.aspx), [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea), and the [SetupDiDestroyDeviceInfoList](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist) functions.</span></span>
-   <span data-ttu-id="73e22-110">Usare le funzioni [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)e [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) .</span><span class="sxs-lookup"><span data-stu-id="73e22-110">Use the [**BluetoothFindFirstRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio), [**BluetoothFindNextRadio**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio), and [**BluetoothFindRadioClose**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose) functions.</span></span>

<span data-ttu-id="73e22-111">Quando viene aperto l'handle di radio Bluetooth, chiamare la funzione [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) e registrarsi per le notifiche sull'handle usando l' **\_ \_ handle DBT DEVTYP** come DeviceType.</span><span class="sxs-lookup"><span data-stu-id="73e22-111">When the Bluetooth radio handle is opened, call the [**RegisterDeviceNotification**](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa) function and register for notifications on the handle using **DBT\_DEVTYP\_HANDLE** as the devicetype.</span></span> <span data-ttu-id="73e22-112">Una volta registrati, vengono inviati i GUID seguenti e il membro **\_ dati** [**dev \_ broadcast \_ handle**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle):: dbch è il buffer associato.</span><span class="sxs-lookup"><span data-stu-id="73e22-112">When registered, the following GUIDs are sent, and the [**DEV\_BROADCAST\_HANDLE**](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)::**dbch\_data** member is the associated buffer.</span></span>

## <a name="bluetooth-specific-messages"></a><span data-ttu-id="73e22-113">Messaggi specifici di Bluetooth</span><span class="sxs-lookup"><span data-stu-id="73e22-113">Bluetooth-specific Messages</span></span>

<span data-ttu-id="73e22-114">La tabella seguente elenca i messaggi [**WM \_ DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) specifici per Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="73e22-114">The following table lists Bluetooth-specific [**WM\_DEVICECHANGE**](/windows/desktop/DevIO/wm-devicechange) messages.</span></span>

| <span data-ttu-id="73e22-115">GUID</span><span class="sxs-lookup"><span data-stu-id="73e22-115">GUID</span></span>                                   | <span data-ttu-id="73e22-116">BUFFER</span><span class="sxs-lookup"><span data-stu-id="73e22-116">BUFFER</span></span>                                                  | <span data-ttu-id="73e22-117">Descrizione</span><span class="sxs-lookup"><span data-stu-id="73e22-117">Description</span></span>                                                                                                                                                                                                                                                                                                                                                      |
|----------------------------------------|---------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73e22-118">\_ \_ evento HCI Bluetooth \_ GUID</span><span class="sxs-lookup"><span data-stu-id="73e22-118">GUID\_BLUETOOTH\_HCI\_EVENT</span></span>            | [<span data-ttu-id="73e22-119">**\_ \_ informazioni evento BTH \_ HCI**</span><span class="sxs-lookup"><span data-stu-id="73e22-119">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)     | <span data-ttu-id="73e22-120">Questo messaggio viene inviato quando un dispositivo Bluetooth remoto si connette o si disconnette a livello di ACL.</span><span class="sxs-lookup"><span data-stu-id="73e22-120">This message is sent when a remote Bluetooth device connects or disconnects at the ACL level.</span></span>                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="73e22-121">\_ \_ Evento L2CAP Bluetooth \_ GUID</span><span class="sxs-lookup"><span data-stu-id="73e22-121">GUID\_BLUETOOTH\_L2CAP\_EVENT</span></span>          | [<span data-ttu-id="73e22-122">**\_Informazioni sull' \_ evento \_ L2CAP di BTH**</span><span class="sxs-lookup"><span data-stu-id="73e22-122">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info) | <span data-ttu-id="73e22-123">Questo messaggio viene inviato quando viene stabilito o terminato un canale L2CAP tra la radio locale e un dispositivo Bluetooth remoto.</span><span class="sxs-lookup"><span data-stu-id="73e22-123">This message is sent when an L2CAP channel between the local radio and a remote Bluetooth device has been established or terminated.</span></span> <span data-ttu-id="73e22-124">Per i canali L2CAP che sono multiplexer, ad esempio RFCOMM, questo messaggio viene inviato solo quando viene stabilito il canale sottostante, non quando viene stabilito o terminato ogni canale multiplex, ad esempio un canale RFCOMM.</span><span class="sxs-lookup"><span data-stu-id="73e22-124">For L2CAP channels that are multiplexers, such as RFCOMM, this message is only sent when the underlying channel is established, not when each multiplexed channel, such as an RFCOMM channel, is established or terminated.</span></span> |
| <span data-ttu-id="73e22-125">\_ \_ richiesta PIN Bluetooth \_ GUID</span><span class="sxs-lookup"><span data-stu-id="73e22-125">GUID\_BLUETOOTH\_PIN\_REQUEST</span></span>          | <span data-ttu-id="73e22-126">Non applicabile.</span><span class="sxs-lookup"><span data-stu-id="73e22-126">Not applicable.</span></span>                                         | <span data-ttu-id="73e22-127">Questo messaggio deve essere ignorato dall'applicazione.</span><span class="sxs-lookup"><span data-stu-id="73e22-127">This message should be ignored by the application.</span></span> <span data-ttu-id="73e22-128">Se l'applicazione deve ricevere richieste PIN, è necessario usare la funzione [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) .</span><span class="sxs-lookup"><span data-stu-id="73e22-128">If the application must receive PIN requests, the [**BluetoothRegisterForAuthentication**](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothregisterforauthentication) function should be used.</span></span>                                                                                                                                                   |
| <span data-ttu-id="73e22-129">\_radio Bluetooth \_ GUID \_ nell' \_ intervallo</span><span class="sxs-lookup"><span data-stu-id="73e22-129">GUID\_BLUETOOTH\_RADIO\_IN\_RANGE</span></span>      | [<span data-ttu-id="73e22-130">**BTH \_ Radio \_ nell' \_ intervallo**</span><span class="sxs-lookup"><span data-stu-id="73e22-130">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)     | <span data-ttu-id="73e22-131">Questo messaggio viene inviato quando uno degli attributi seguenti di un dispositivo Bluetooth remoto è stato modificato: il dispositivo è stato individuato, la classe del dispositivo, il nome, lo stato connesso o lo stato del dispositivo memorizzato.</span><span class="sxs-lookup"><span data-stu-id="73e22-131">This message is sent when any of the following attributes of a remote Bluetooth device has changed: the device has been discovered, the class of device, name, connected state, or device remembered state.</span></span> <span data-ttu-id="73e22-132">Questo messaggio viene inviato anche quando questi attributi sono impostati o cancellati.</span><span class="sxs-lookup"><span data-stu-id="73e22-132">This message is also sent when these attributes are set or cleared.</span></span>                                                                                  |
| <span data-ttu-id="73e22-133">\_radio Bluetooth GUID non \_ compresa nell' \_ \_ \_ intervallo</span><span class="sxs-lookup"><span data-stu-id="73e22-133">GUID\_BLUETOOTH\_RADIO\_OUT\_OF\_RANGE</span></span> | [<span data-ttu-id="73e22-134">**\_Indirizzo Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="73e22-134">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)         | <span data-ttu-id="73e22-135">Questo messaggio viene inviato quando un dispositivo individuato in precedenza non è stato trovato dopo il completamento dell'ultima richiesta.</span><span class="sxs-lookup"><span data-stu-id="73e22-135">This message is sent when a previously discovered device has not been found after the completion of the last inquiry.</span></span> <span data-ttu-id="73e22-136">Questo messaggio non verrà inviato per i dispositivi memorizzati.</span><span class="sxs-lookup"><span data-stu-id="73e22-136">This message will not be sent for remembered devices.</span></span> <span data-ttu-id="73e22-137">La struttura dell' **\_ Indirizzo BTH** è l'indirizzo del dispositivo che non è stato trovato.</span><span class="sxs-lookup"><span data-stu-id="73e22-137">The **BTH\_ADDRESS** structure is the address of the device that was not found.</span></span>                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="73e22-138">Argomenti correlati</span><span class="sxs-lookup"><span data-stu-id="73e22-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="73e22-139">**BluetoothFindFirstRadio**</span><span class="sxs-lookup"><span data-stu-id="73e22-139">**BluetoothFindFirstRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindfirstradio)
</dt> <dt>

[<span data-ttu-id="73e22-140">**BluetoothFindNextRadio**</span><span class="sxs-lookup"><span data-stu-id="73e22-140">**BluetoothFindNextRadio**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindnextradio)
</dt> <dt>

[<span data-ttu-id="73e22-141">**BluetoothFindRadioClose**</span><span class="sxs-lookup"><span data-stu-id="73e22-141">**BluetoothFindRadioClose**</span></span>](/windows/desktop/api/BluetoothAPIs/nf-bluetoothapis-bluetoothfindradioclose)
</dt> <dt>

[<span data-ttu-id="73e22-142">**RegisterDeviceNotification**</span><span class="sxs-lookup"><span data-stu-id="73e22-142">**RegisterDeviceNotification**</span></span>](/windows/desktop/api/winuser/nf-winuser-registerdevicenotificationa)
</dt> <dt>

[<span data-ttu-id="73e22-143">SetupDiDestroyDeviceInfoList</span><span class="sxs-lookup"><span data-stu-id="73e22-143">SetupDiDestroyDeviceInfoList</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdidestroydeviceinfolist)
</dt> <dt>

[<span data-ttu-id="73e22-144">SetupDiEnumDeviceInterfaces</span><span class="sxs-lookup"><span data-stu-id="73e22-144">SetupDiEnumDeviceInterfaces</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdienumdeviceinterfaces)
</dt> <dt>

[<span data-ttu-id="73e22-145">SetupDiGetClassDevs</span><span class="sxs-lookup"><span data-stu-id="73e22-145">SetupDiGetClassDevs</span></span>](/windows/win32/api/setupapi/nf-setupapi-setupdigetclassdevsw)
</dt> <dt>

[<span data-ttu-id="73e22-146">**\_Indirizzo Bluetooth**</span><span class="sxs-lookup"><span data-stu-id="73e22-146">**BLUETOOTH\_ADDRESS**</span></span>](/windows/win32/api/bluetoothapis/ns-bluetoothapis-bluetooth_address_struct)
</dt> <dt>

[<span data-ttu-id="73e22-147">**\_ \_ informazioni evento BTH \_ HCI**</span><span class="sxs-lookup"><span data-stu-id="73e22-147">**BTH\_HCI\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_hci_event_info)
</dt> <dt>

[<span data-ttu-id="73e22-148">**\_Informazioni sull' \_ evento \_ L2CAP di BTH**</span><span class="sxs-lookup"><span data-stu-id="73e22-148">**BTH\_L2CAP\_EVENT\_INFO**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_l2cap_event_info)
</dt> <dt>

[<span data-ttu-id="73e22-149">**BTH \_ Radio \_ nell' \_ intervallo**</span><span class="sxs-lookup"><span data-stu-id="73e22-149">**BTH\_RADIO\_IN\_RANGE**</span></span>](/windows/desktop/api/Bthdef/ns-bthdef-bth_radio_in_range)
</dt> <dt>

[<span data-ttu-id="73e22-150">**\_handle broadcast \_ dev**</span><span class="sxs-lookup"><span data-stu-id="73e22-150">**DEV\_BROADCAST\_HANDLE**</span></span>](/windows/desktop/api/dbt/ns-dbt-dev_broadcast_handle)
</dt> <dt>

[<span data-ttu-id="73e22-151">**\_DEVICECHANGE WM**</span><span class="sxs-lookup"><span data-stu-id="73e22-151">**WM\_DEVICECHANGE**</span></span>](/windows/desktop/DevIO/wm-devicechange)
</dt> </dl>

 

 