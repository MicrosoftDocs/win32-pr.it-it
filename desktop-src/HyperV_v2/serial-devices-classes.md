---
description: I dispositivi seriali in una macchina virtuale sono costituiti da controller seriali e porte seriali. Ogni macchina virtuale ha esattamente un controller seriale e ogni controller seriale ha esattamente due porte seriali.
ms.assetid: BA24BD74-D80C-4C5C-891F-5F17CDED2EC6
title: Classi di dispositivi seriali
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10ae796b86837372d60bba83e51e0190b9c7d3f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313837"
---
# <a name="serial-devices-classes"></a><span data-ttu-id="2b48b-104">Classi di dispositivi seriali</span><span class="sxs-lookup"><span data-stu-id="2b48b-104">Serial devices classes</span></span>

<span data-ttu-id="2b48b-105">I dispositivi seriali in una macchina virtuale sono costituiti da controller seriali e porte seriali.</span><span class="sxs-lookup"><span data-stu-id="2b48b-105">The serial devices in a virtual machine consist of serial controllers and serial ports.</span></span> <span data-ttu-id="2b48b-106">Ogni macchina virtuale ha esattamente un controller seriale e ogni controller seriale ha esattamente due porte seriali.</span><span class="sxs-lookup"><span data-stu-id="2b48b-106">Each virtual machine has exactly one serial controller, and each serial controller has exactly two serial ports.</span></span>

<span data-ttu-id="2b48b-107">Le impostazioni per il controller seriale non sono configurabili; Pertanto, non è associata alcuna istanza di dati di impostazione.</span><span class="sxs-lookup"><span data-stu-id="2b48b-107">The settings for the serial controller are not configurable; therefore, there is no setting data instance associated with it.</span></span> <span data-ttu-id="2b48b-108">Inoltre, non è possibile aggiungere o rimuovere controller seriali o porte seriali da una macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="2b48b-108">Also, you cannot add or remove serial controllers or serial ports from a virtual machine.</span></span> <span data-ttu-id="2b48b-109">Non sono pertanto disponibili istanze del pool di risorse per i dispositivi seriali.</span><span class="sxs-lookup"><span data-stu-id="2b48b-109">Therefore, there are no resource pool instances for serial devices.</span></span>

<span data-ttu-id="2b48b-110">Di seguito sono riportate le classi WMI di virtualizzazione correlate ai dispositivi seriali.</span><span class="sxs-lookup"><span data-stu-id="2b48b-110">The following are virtualization WMI classes related to serial devices.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="2b48b-111">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="2b48b-111">In this section</span></span>



| <span data-ttu-id="2b48b-112">Argomento</span><span class="sxs-lookup"><span data-stu-id="2b48b-112">Topic</span></span>                                                                                      | <span data-ttu-id="2b48b-113">Descrizione</span><span class="sxs-lookup"><span data-stu-id="2b48b-113">Description</span></span>                                                                     |
|--------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="2b48b-114">**\_Controller seriale MSVM**</span><span class="sxs-lookup"><span data-stu-id="2b48b-114">**Msvm\_SerialController**</span></span>](msvm-serialcontroller.md)<br/>                         | <span data-ttu-id="2b48b-115">Rappresenta le funzionalità e la gestione del controller seriale.</span><span class="sxs-lookup"><span data-stu-id="2b48b-115">Represents the capabilities and management of the serial controller.</span></span><br/> |
| [<span data-ttu-id="2b48b-116">**MSVM \_ SerialPort**</span><span class="sxs-lookup"><span data-stu-id="2b48b-116">**Msvm\_SerialPort**</span></span>](msvm-serialport.md)<br/>                                     | <span data-ttu-id="2b48b-117">Rappresenta una porta seriale associata al controller seriale.</span><span class="sxs-lookup"><span data-stu-id="2b48b-117">Represents a serial port associated with the serial controller.</span></span><br/>      |
| [<span data-ttu-id="2b48b-118">**\_SerialPortOnSerialController MSVM**</span><span class="sxs-lookup"><span data-stu-id="2b48b-118">**Msvm\_SerialPortOnSerialController**</span></span>](msvm-serialportonserialcontroller.md)<br/> | <span data-ttu-id="2b48b-119">Associa una porta seriale a un controller seriale.</span><span class="sxs-lookup"><span data-stu-id="2b48b-119">Associates a serial port with a serial controller.</span></span><br/>                   |



 

 

 




