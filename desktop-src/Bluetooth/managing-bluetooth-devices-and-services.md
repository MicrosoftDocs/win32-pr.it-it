---
title: Gestione dei dispositivi e dei servizi Bluetooth
description: Due approcci di programmazione Bluetooth principali per la programmazione Windows con l'interfaccia Windows Sockets e la gestione diretta dei dispositivi con interfacce Bluetooth non socket.
ms.assetid: 0eb7d339-6d23-4313-b1ed-7ab403a5a81d
keywords:
- Gestione dei dispositivi e dei servizi Bluetooth
- Dispositivi e servizi Bluetooth, gestione
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61cf3657dff2091eda4b26d14f6504b74f943983
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104117807"
---
# <a name="managing-bluetooth-devices-and-services"></a><span data-ttu-id="49564-105">Gestione dei dispositivi e dei servizi Bluetooth</span><span class="sxs-lookup"><span data-stu-id="49564-105">Managing Bluetooth Devices and Services</span></span>

<span data-ttu-id="49564-106">Questa sezione descrive come usare l'API Bluetooth per controllare direttamente i dispositivi e i servizi Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="49564-106">This section describes how to use the Bluetooth API to directly control Bluetooth devices and services.</span></span>

<span data-ttu-id="49564-107">Per informazioni sull'utilizzo dell'interfaccia Windows Sockets per programmare il Bluetooth in Windows, vedere [supporto di Windows Sockets per Bluetooth](windows-sockets-support-for-bluetooth.md).</span><span class="sxs-lookup"><span data-stu-id="49564-107">For information about using the Windows Sockets interface to program Bluetooth on Windows, see [Windows Sockets Support for Bluetooth](windows-sockets-support-for-bluetooth.md).</span></span>

> [!Note]  
> <span data-ttu-id="49564-108">Bluetooth non impedisce che le funzionalità di risparmio energia interrompano le trasmissioni Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="49564-108">Bluetooth does not prevent power management features from interrupting Bluetooth transmissions.</span></span> <span data-ttu-id="49564-109">Le applicazioni abilitate per Bluetooth possono monitorare i messaggi di alimentazione per evitare tale interruzione.</span><span class="sxs-lookup"><span data-stu-id="49564-109">Bluetooth-enabled applications can monitor power messages to prevent such interruption.</span></span> <span data-ttu-id="49564-110">Per altre informazioni, vedere [uso](/windows/desktop/Power/using-power-management)del risparmio energia.</span><span class="sxs-lookup"><span data-stu-id="49564-110">For more information, see [Using Power Management](/windows/desktop/Power/using-power-management).</span></span>

 

<span data-ttu-id="49564-111">In questa sezione vengono trattati gli argomenti seguenti.</span><span class="sxs-lookup"><span data-stu-id="49564-111">This section contains the following topics.</span></span>

| <span data-ttu-id="49564-112">Sezione</span><span class="sxs-lookup"><span data-stu-id="49564-112">Section</span></span>                                                                               | <span data-ttu-id="49564-113">Content</span><span class="sxs-lookup"><span data-stu-id="49564-113">Content</span></span>                                                                       |
|---------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [<span data-ttu-id="49564-114">Selezione di un dispositivo Bluetooth</span><span class="sxs-lookup"><span data-stu-id="49564-114">Selecting a Bluetooth Device</span></span>](selecting-a-bluetooth-device.md)                      | <span data-ttu-id="49564-115">Viene descritto come selezionare un dispositivo Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="49564-115">Describes how to select a Bluetooth device.</span></span>                                   |
| [<span data-ttu-id="49564-116">Messaggi Bluetooth e WM \_ DEVICECHANGE</span><span class="sxs-lookup"><span data-stu-id="49564-116">Bluetooth and WM\_DEVICECHANGE Messages</span></span>](bluetooth-and-wm-devicechange-messages.md) | <span data-ttu-id="49564-117">Viene illustrata l'interazione tra i messaggi Bluetooth e **WM \_ DEVICECHANGE** .</span><span class="sxs-lookup"><span data-stu-id="49564-117">Explains the interaction between Bluetooth and **WM\_DEVICECHANGE** messages.</span></span> |



 

 

 