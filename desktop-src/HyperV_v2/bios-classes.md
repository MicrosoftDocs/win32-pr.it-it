---
description: Il BIOS virtuale è un'immagine software caricata in RAM per configurare alcuni degli aspetti di base di e avviare un sistema di computer. È presente un solo elemento BIOS per computer e tale elemento non può essere sostituito o rimosso.
ms.assetid: EC691401-947F-4B56-A8A7-F0ECBF01677B
title: Classi BIOS
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e725910bbeb1032f876b5e4fcf08da4a6ea60bc1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967556"
---
# <a name="bios-classes"></a><span data-ttu-id="9cb59-104">Classi BIOS</span><span class="sxs-lookup"><span data-stu-id="9cb59-104">BIOS classes</span></span>

<span data-ttu-id="9cb59-105">Il BIOS virtuale è un'immagine software caricata in RAM per configurare alcuni degli aspetti di base di e avviare un sistema di computer.</span><span class="sxs-lookup"><span data-stu-id="9cb59-105">The virtual BIOS is a software image that is loaded into RAM to configure some of the basic aspects of and boot a computer system.</span></span> <span data-ttu-id="9cb59-106">È presente un solo elemento BIOS per computer e tale elemento non può essere sostituito o rimosso.</span><span class="sxs-lookup"><span data-stu-id="9cb59-106">There is one BIOS element per computer system and that element cannot be replaced or removed.</span></span> <span data-ttu-id="9cb59-107">Non è quindi disponibile alcun pool di risorse per l'aggiunta di nuovi elementi BIOS alla macchina virtuale.</span><span class="sxs-lookup"><span data-stu-id="9cb59-107">Thus, there is no resource pool for adding new BIOS elements to the virtual machine.</span></span> <span data-ttu-id="9cb59-108">L'elemento BIOS non dispone inoltre di una propria classe SettingData per descrivere le impostazioni per il BIOS.</span><span class="sxs-lookup"><span data-stu-id="9cb59-108">The BIOS element also does not have its own SettingData class to describe the settings for the BIOS.</span></span> <span data-ttu-id="9cb59-109">Le impostazioni per il BIOS, ad esempio i numeri di serie, l'ordine di avvio e lo stato di blocco num, si trovano nella classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="9cb59-109">Settings for the BIOS, such as serial numbers, boot order, and num lock state, are found in the [**Msvm\_VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) class.</span></span>

<span data-ttu-id="9cb59-110">Di seguito sono riportate le classi WMI di virtualizzazione correlate al BIOS.</span><span class="sxs-lookup"><span data-stu-id="9cb59-110">The following are virtualization WMI classes related to the BIOS.</span></span> <span data-ttu-id="9cb59-111">Queste classi si trovano in \\ \\ . \\ \\Spazio dei nomi di virtualizzazione radice.</span><span class="sxs-lookup"><span data-stu-id="9cb59-111">These classes are in the \\\\.\\Root\\Virtualization namespace.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="9cb59-112">Contenuto della sezione</span><span class="sxs-lookup"><span data-stu-id="9cb59-112">In this section</span></span>



| <span data-ttu-id="9cb59-113">Argomento</span><span class="sxs-lookup"><span data-stu-id="9cb59-113">Topic</span></span>                                                    | <span data-ttu-id="9cb59-114">Descrizione</span><span class="sxs-lookup"><span data-stu-id="9cb59-114">Description</span></span>                                                                                             |
|----------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9cb59-115">**MSVM \_ bioselement**</span><span class="sxs-lookup"><span data-stu-id="9cb59-115">**Msvm\_BIOSElement**</span></span>](msvm-bioselement.md)<br/> | <span data-ttu-id="9cb59-116">Rappresenta il software di basso livello caricato in RAM per configurare e avviare il sistema.</span><span class="sxs-lookup"><span data-stu-id="9cb59-116">Represents the low-level software that is loaded into RAM to configure and start the system.</span></span><br/> |
| [<span data-ttu-id="9cb59-117">**\_SystemBIOS MSVM**</span><span class="sxs-lookup"><span data-stu-id="9cb59-117">**Msvm\_SystemBIOS**</span></span>](msvm-systembios.md)<br/>   | <span data-ttu-id="9cb59-118">Utilizzato per associare una macchina virtuale al relativo BIOS.</span><span class="sxs-lookup"><span data-stu-id="9cb59-118">Used to associate a virtual machine with its BIOS.</span></span><br/>                                           |



 

 

 




