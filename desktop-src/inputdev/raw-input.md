---
title: Input non elaborato
description: In questa sezione viene descritto il modo in cui il sistema fornisce input non elaborato all'applicazione e il modo in cui un'applicazione riceve ed elabora tale input.
ms.assetid: vs|winui|~\winui\windowsuserinterface\userinput\rawinput.htm
keywords:
- Interfaccia utente di Windows, input utente
- Interfaccia utente di Windows, input non elaborato
- input utente, input non elaborato
- acquisizione dell'input dell'utente, input non elaborato
- input non elaborato
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e88de70dd2b635cf7dda90f23686b9916c99be4f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398953"
---
# <a name="raw-input"></a><span data-ttu-id="981bb-108">Input non elaborato</span><span class="sxs-lookup"><span data-stu-id="981bb-108">Raw Input</span></span>

<span data-ttu-id="981bb-109">In questa sezione viene descritto il modo in cui il sistema fornisce input non elaborato all'applicazione e il modo in cui un'applicazione riceve ed elabora tale input.</span><span class="sxs-lookup"><span data-stu-id="981bb-109">This section describes how the system provides raw input to your application and how an application receives and processes that input.</span></span> <span data-ttu-id="981bb-110">L'input non elaborato viene talvolta definito input generico.</span><span class="sxs-lookup"><span data-stu-id="981bb-110">Raw input is sometimes referred to as generic input.</span></span>

### <a name="in-this-section"></a><span data-ttu-id="981bb-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="981bb-111">In This Section</span></span>



| <span data-ttu-id="981bb-112">Nome</span><span class="sxs-lookup"><span data-stu-id="981bb-112">Name</span></span>                                           | <span data-ttu-id="981bb-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="981bb-113">Description</span></span>                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="981bb-114">Informazioni sull'input non elaborato</span><span class="sxs-lookup"><span data-stu-id="981bb-114">About Raw Input</span></span>](about-raw-input.md)         | <span data-ttu-id="981bb-115">Viene illustrato l'input dell'utente da dispositivi quali joystick, touch screen e microfoni.</span><span class="sxs-lookup"><span data-stu-id="981bb-115">Discusses user-input from devices such as joysticks, touch screens, and microphones.</span></span><br/> |
| [<span data-ttu-id="981bb-116">Uso dell'input non elaborato</span><span class="sxs-lookup"><span data-stu-id="981bb-116">Using Raw Input</span></span>](using-raw-input.md)         | <span data-ttu-id="981bb-117">Fornisce il codice di esempio per le attività relative all'input non elaborato.</span><span class="sxs-lookup"><span data-stu-id="981bb-117">Provides sample code for tasks relating to raw input.</span></span><br/>                                |
| [<span data-ttu-id="981bb-118">Riferimento input non elaborato</span><span class="sxs-lookup"><span data-stu-id="981bb-118">Raw Input Reference</span></span>](raw-input-reference.md) | <span data-ttu-id="981bb-119">Contiene il riferimento all'API.</span><span class="sxs-lookup"><span data-stu-id="981bb-119">Contains the API reference.</span></span><br/>                                                          |



 

### <a name="functions"></a><span data-ttu-id="981bb-120">Funzioni</span><span class="sxs-lookup"><span data-stu-id="981bb-120">Functions</span></span>



| <span data-ttu-id="981bb-121">Nome</span><span class="sxs-lookup"><span data-stu-id="981bb-121">Name</span></span>                                                                 | <span data-ttu-id="981bb-122">Descrizione</span><span class="sxs-lookup"><span data-stu-id="981bb-122">Description</span></span>                                                                                                                                                                                                                                                                                                             |
|----------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="981bb-123">**DefRawInputProc**</span><span class="sxs-lookup"><span data-stu-id="981bb-123">**DefRawInputProc**</span></span>](/windows/win32/api/winuser/nf-winuser-defrawinputproc)                           | <span data-ttu-id="981bb-124">Chiama la procedura di input non elaborato predefinita per fornire l'elaborazione predefinita per tutti i messaggi di input non elaborati che un'applicazione non elabora.</span><span class="sxs-lookup"><span data-stu-id="981bb-124">Calls the default raw input procedure to provide default processing for any raw input messages that an application does not process.</span></span> <span data-ttu-id="981bb-125">Questa funzione garantisce che ogni messaggio venga elaborato.</span><span class="sxs-lookup"><span data-stu-id="981bb-125">This function ensures that every message is processed.</span></span> <span data-ttu-id="981bb-126">[**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) viene chiamato con gli stessi parametri ricevuti dalla routine della finestra.</span><span class="sxs-lookup"><span data-stu-id="981bb-126">[**DefRawInputProc**](/windows/win32/api/winuser/nf-winuser-defrawinputproc) is called with the same parameters received by the window procedure.</span></span> <br/> |
| [<span data-ttu-id="981bb-127">**GetRawInputBuffer**</span><span class="sxs-lookup"><span data-stu-id="981bb-127">**GetRawInputBuffer**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputbuffer)                       | <span data-ttu-id="981bb-128">Esegue una lettura con memorizzazione nel buffer dei dati di input non elaborati.</span><span class="sxs-lookup"><span data-stu-id="981bb-128">Performs a buffered read of the raw input data.</span></span><br/>                                                                                                                                                                                                                                                              |
| [<span data-ttu-id="981bb-129">**GetRawInputData**</span><span class="sxs-lookup"><span data-stu-id="981bb-129">**GetRawInputData**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdata)                           | <span data-ttu-id="981bb-130">Ottiene l'input non elaborato dal dispositivo specificato.</span><span class="sxs-lookup"><span data-stu-id="981bb-130">Gets the raw input from the specified device.</span></span><br/>                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="981bb-131">**GetRawInputDeviceInfo**</span><span class="sxs-lookup"><span data-stu-id="981bb-131">**GetRawInputDeviceInfo**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdeviceinfoa)               | <span data-ttu-id="981bb-132">Ottiene informazioni sul dispositivo di input non elaborato.</span><span class="sxs-lookup"><span data-stu-id="981bb-132">Gets information about the raw input device.</span></span><br/>                                                                                                                                                                                                                                                                 |
| [<span data-ttu-id="981bb-133">**GetRawInputDeviceList**</span><span class="sxs-lookup"><span data-stu-id="981bb-133">**GetRawInputDeviceList**</span></span>](/windows/win32/api/winuser/nf-winuser-getrawinputdevicelist)               | <span data-ttu-id="981bb-134">Enumera i dispositivi di input non elaborati collegati al sistema.</span><span class="sxs-lookup"><span data-stu-id="981bb-134">Enumerates the raw input devices attached to the system.</span></span> <br/>                                                                                                                                                                                                                                                    |
| [<span data-ttu-id="981bb-135">**GetRegisteredRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="981bb-135">**GetRegisteredRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-getregisteredrawinputdevices) | <span data-ttu-id="981bb-136">Ottiene le informazioni sui dispositivi di input non elaborati per l'applicazione corrente.</span><span class="sxs-lookup"><span data-stu-id="981bb-136">Gets the information about the raw input devices for the current application.</span></span><br/>                                                                                                                                                                                                                                |
| [<span data-ttu-id="981bb-137">**RegisterRawInputDevices**</span><span class="sxs-lookup"><span data-stu-id="981bb-137">**RegisterRawInputDevices**</span></span>](/windows/win32/api/winuser/nf-winuser-registerrawinputdevices)           | <span data-ttu-id="981bb-138">Registra i dispositivi che forniscono i dati di input non elaborati.</span><span class="sxs-lookup"><span data-stu-id="981bb-138">Registers the devices that supply the raw input data.</span></span><br/>                                                                                                                                                                                                                                                        |



 

### <a name="macros"></a><span data-ttu-id="981bb-139">Macro</span><span class="sxs-lookup"><span data-stu-id="981bb-139">Macros</span></span>



| <span data-ttu-id="981bb-140">Nome</span><span class="sxs-lookup"><span data-stu-id="981bb-140">Name</span></span>                                                            | <span data-ttu-id="981bb-141">Descrizione</span><span class="sxs-lookup"><span data-stu-id="981bb-141">Description</span></span>                                                                                                 |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="981bb-142">**OTTENERE \_ il \_ codice rawinput \_ wParam**</span><span class="sxs-lookup"><span data-stu-id="981bb-142">**GET\_RAWINPUT\_CODE\_WPARAM**</span></span>](/windows/win32/api/winuser/nf-winuser-get_rawinput_code_wparam) | <span data-ttu-id="981bb-143">Ottiene il codice di input da *wParam* nell' [**\_ input WM**](wm-input.md).</span><span class="sxs-lookup"><span data-stu-id="981bb-143">Gets the input code from *wParam* in [**WM\_INPUT**](wm-input.md).</span></span><br/>                              |
| [<span data-ttu-id="981bb-144">**NEXTRAWINPUTBLOCK**</span><span class="sxs-lookup"><span data-stu-id="981bb-144">**NEXTRAWINPUTBLOCK**</span></span>](/windows/win32/api/winuser/nf-winuser-nextrawinputblock)                  | <span data-ttu-id="981bb-145">Ottiene la posizione della struttura successiva in una matrice di strutture [**rawinput**](/windows/win32/api/winuser/ns-winuser-rawinput) .</span><span class="sxs-lookup"><span data-stu-id="981bb-145">Gets the location of the next structure in an array of [**RAWINPUT**](/windows/win32/api/winuser/ns-winuser-rawinput) structures.</span></span> <br/> |



 

### <a name="notifications"></a><span data-ttu-id="981bb-146">Notifiche</span><span class="sxs-lookup"><span data-stu-id="981bb-146">Notifications</span></span>



| <span data-ttu-id="981bb-147">Nome</span><span class="sxs-lookup"><span data-stu-id="981bb-147">Name</span></span>                                                        | <span data-ttu-id="981bb-148">Descrizione</span><span class="sxs-lookup"><span data-stu-id="981bb-148">Description</span></span>                                                          |
|-------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="981bb-149">**\_input WM**</span><span class="sxs-lookup"><span data-stu-id="981bb-149">**WM\_INPUT**</span></span>](wm-input.md)                               | <span data-ttu-id="981bb-150">Inviato alla finestra che sta ricevendo l'input non elaborato.</span><span class="sxs-lookup"><span data-stu-id="981bb-150">Sent to the window that is getting raw input.</span></span> <br/>            |
| [<span data-ttu-id="981bb-151">**\_modifica del \_ dispositivo di input WM \_**</span><span class="sxs-lookup"><span data-stu-id="981bb-151">**WM\_INPUT\_DEVICE\_CHANGE**</span></span>](wm-input-device-change.md) | <span data-ttu-id="981bb-152">Inviato alla finestra registrata per ricevere input non elaborato.</span><span class="sxs-lookup"><span data-stu-id="981bb-152">Sent to the window that registered to receive raw input.</span></span> <br/> |



 

### <a name="structures"></a><span data-ttu-id="981bb-153">Strutture</span><span class="sxs-lookup"><span data-stu-id="981bb-153">Structures</span></span>



| <span data-ttu-id="981bb-154">Nome</span><span class="sxs-lookup"><span data-stu-id="981bb-154">Name</span></span>                                                            | <span data-ttu-id="981bb-155">Descrizione</span><span class="sxs-lookup"><span data-stu-id="981bb-155">Description</span></span>                                                                            |
|-----------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="981bb-156">**RAWHID**</span><span class="sxs-lookup"><span data-stu-id="981bb-156">**RAWHID**</span></span>](/windows/win32/api/winuser/ns-winuser-rawhid)                                        | <span data-ttu-id="981bb-157">Descrive il formato dell'input non elaborato da un dispositivo di interfaccia umana (HID).</span><span class="sxs-lookup"><span data-stu-id="981bb-157">Describes the format of the raw input from a Human Interface Device (HID).</span></span> <br/> |
| [<span data-ttu-id="981bb-158">**RAWINPUT**</span><span class="sxs-lookup"><span data-stu-id="981bb-158">**RAWINPUT**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinput)                                    | <span data-ttu-id="981bb-159">Contiene l'input non elaborato da un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="981bb-159">Contains the raw input from a device.</span></span> <br/>                                      |
| [<span data-ttu-id="981bb-160">**RAWINPUTDEVICE**</span><span class="sxs-lookup"><span data-stu-id="981bb-160">**RAWINPUTDEVICE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevice)                        | <span data-ttu-id="981bb-161">Definisce le informazioni per i dispositivi di input non elaborati.</span><span class="sxs-lookup"><span data-stu-id="981bb-161">Defines information for the raw input devices.</span></span> <br/>                             |
| [<span data-ttu-id="981bb-162">**RAWINPUTDEVICELIST**</span><span class="sxs-lookup"><span data-stu-id="981bb-162">**RAWINPUTDEVICELIST**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputdevicelist)                | <span data-ttu-id="981bb-163">Contiene informazioni su un dispositivo di input non elaborato.</span><span class="sxs-lookup"><span data-stu-id="981bb-163">Contains information about a raw input device.</span></span><br/>                              |
| [<span data-ttu-id="981bb-164">**RAWINPUTHEADER**</span><span class="sxs-lookup"><span data-stu-id="981bb-164">**RAWINPUTHEADER**</span></span>](/windows/win32/api/winuser/ns-winuser-rawinputheader)                        | <span data-ttu-id="981bb-165">Contiene le informazioni di intestazione che fanno parte dei dati di input non elaborati.</span><span class="sxs-lookup"><span data-stu-id="981bb-165">Contains the header information that is part of the raw input data.</span></span> <br/>        |
| [<span data-ttu-id="981bb-166">**RAWKEYBOARD**</span><span class="sxs-lookup"><span data-stu-id="981bb-166">**RAWKEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rawkeyboard)                              | <span data-ttu-id="981bb-167">Contiene informazioni sullo stato della tastiera.</span><span class="sxs-lookup"><span data-stu-id="981bb-167">Contains information about the state of the keyboard.</span></span> <br/>                      |
| [<span data-ttu-id="981bb-168">**RAWMOUSE**</span><span class="sxs-lookup"><span data-stu-id="981bb-168">**RAWMOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rawmouse)                                    | <span data-ttu-id="981bb-169">Contiene informazioni sullo stato del mouse.</span><span class="sxs-lookup"><span data-stu-id="981bb-169">Contains information about the state of the mouse.</span></span> <br/>                         |
| [<span data-ttu-id="981bb-170">**\_informazioni sul dispositivo RID \_**</span><span class="sxs-lookup"><span data-stu-id="981bb-170">**RID\_DEVICE\_INFO**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info)                    | <span data-ttu-id="981bb-171">Definisce i dati di input non elaborati provenienti da qualsiasi dispositivo.</span><span class="sxs-lookup"><span data-stu-id="981bb-171">Defines the raw input data coming from any device.</span></span> <br/>                         |
| [<span data-ttu-id="981bb-172">**\_informazioni sul dispositivo RID \_ \_ nascoste**</span><span class="sxs-lookup"><span data-stu-id="981bb-172">**RID\_DEVICE\_INFO\_HID**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_hid)           | <span data-ttu-id="981bb-173">Definisce i dati di input non elaborati provenienti dall'oggetto nascosto specificato.</span><span class="sxs-lookup"><span data-stu-id="981bb-173">Defines the raw input data coming from the specified HID.</span></span> <br/>                  |
| [<span data-ttu-id="981bb-174">**\_ \_ tastiera informazioni sul dispositivo RID \_**</span><span class="sxs-lookup"><span data-stu-id="981bb-174">**RID\_DEVICE\_INFO\_KEYBOARD**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_keyboard) | <span data-ttu-id="981bb-175">Definisce i dati di input non elaborati provenienti dalla tastiera specificata.</span><span class="sxs-lookup"><span data-stu-id="981bb-175">Defines the raw input data coming from the specified keyboard.</span></span> <br/>             |
| [<span data-ttu-id="981bb-176">**\_ \_ mouse informazioni sul dispositivo RID \_**</span><span class="sxs-lookup"><span data-stu-id="981bb-176">**RID\_DEVICE\_INFO\_MOUSE**</span></span>](/windows/win32/api/winuser/ns-winuser-rid_device_info_mouse)       | <span data-ttu-id="981bb-177">Definisce i dati di input non elaborati provenienti dal mouse specificato.</span><span class="sxs-lookup"><span data-stu-id="981bb-177">Defines the raw input data coming from the specified mouse.</span></span><br/>                 |



 

 

