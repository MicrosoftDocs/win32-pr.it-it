---
description: È possibile accedere ai dispositivi SNMP leggendo o scrivendo nell'istanza della classe corrispondente nel archivio SMIR WMI (archivio informazioni del modulo SNMP).
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Lettura e scrittura nei dispositivi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8fc25f384d499e16e19c5e909f7d091ea34f9a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104528603"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a><span data-ttu-id="da444-103">Lettura e scrittura nei dispositivi SNMP</span><span class="sxs-lookup"><span data-stu-id="da444-103">Reading from and Writing to SNMP Devices</span></span>

<span data-ttu-id="da444-104">È possibile accedere ai dispositivi SNMP leggendo o scrivendo nell'istanza della classe corrispondente nel archivio SMIR WMI (archivio informazioni del modulo SNMP).</span><span class="sxs-lookup"><span data-stu-id="da444-104">SNMP devices can be accessed by reading from or writing to their corresponding class instance in the WMI SMIR (SNMP Module Information Repository).</span></span> <span data-ttu-id="da444-105">Quando si usano più dispositivi dello stesso tipo, per maggiore efficienza caricare il MIB per un tipo di dispositivo SNMP in archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="da444-105">When you are working with multiple devices of the same type, for efficiency, load the MIBs for one SNMP device type into the SMIR.</span></span>

> [!Note]  
> <span data-ttu-id="da444-106">Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="da444-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="da444-107">Selezionare una delle opzioni seguenti per leggere o scrivere da ogni tipo di dispositivo SNMP aggiornando le informazioni di contesto dell'istanza prima della comunicazione con ognuna di esse.</span><span class="sxs-lookup"><span data-stu-id="da444-107">Select one of the following options to read to or write from each SNMP device type by updating the context information of the instance before communicating with each one.</span></span>

-   <span data-ttu-id="da444-108">Usare un nome DNS anziché l'indirizzo IP quando si fa riferimento a un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="da444-108">Use a DNS name instead of the IP address when referencing a specific device.</span></span>

    <span data-ttu-id="da444-109">L'esempio seguente illustra come usare il nome DNS per un dispositivo specifico.</span><span class="sxs-lookup"><span data-stu-id="da444-109">The following example shows how to use the DNS name for a specific device.</span></span>

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   <span data-ttu-id="da444-110">Creare uno spazio dei nomi separato e associare un indirizzo del dispositivo all'oggetto spazio dei nomi utilizzando il qualificatore dell'istanza AgentAddress in modo che lo spazio dei nomi venga associato definitivamente al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da444-110">Create a separate namespace and associate a device address to the namespace object using the AgentAddress instance qualifier so that the namespace is permanently bound to the device.</span></span> <span data-ttu-id="da444-111">In questo caso, non è necessario specificare le informazioni sull'oggetto di contesto.</span><span class="sxs-lookup"><span data-stu-id="da444-111">In this case, you need not specify the context object information.</span></span>
-   <span data-ttu-id="da444-112">Leggere da un dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="da444-112">Read from an SNMP device.</span></span>

    <span data-ttu-id="da444-113">Nell'esempio seguente viene eseguita un'operazione get su una classe del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da444-113">The following example performs a Get operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set objSet = objServices.ExecQuery _
        ("SELECT * FROM SNMP_NET_DEVICE_123 WHERE hdwr_idx>1",, _
          wbemFlagReturnWhenComplete)
    for each obj in objset 
      'do whatever 
    next
    ```

    

-   <span data-ttu-id="da444-114">Scrivere in un dispositivo SNMP.</span><span class="sxs-lookup"><span data-stu-id="da444-114">Write to an SNMP device.</span></span>

    <span data-ttu-id="da444-115">Nell'esempio seguente viene eseguita un'operazione di impostazione su una classe del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da444-115">The following example performs a Set operation on a device class.</span></span>

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

<span data-ttu-id="da444-116">Le classi correlate sono quelle che un determinato dispositivo SNMP è in grado di supportare quando si verifica l'enumerazione.</span><span class="sxs-lookup"><span data-stu-id="da444-116">Correlated classes are those that a given SNMP device is known to support when enumeration occurs.</span></span> <span data-ttu-id="da444-117">La correlazione influiscono sul set di classi restituite da archivio SMIR.</span><span class="sxs-lookup"><span data-stu-id="da444-117">Correlation affects the set of classes returned from the SMIR.</span></span> <span data-ttu-id="da444-118">L'enumerazione non correlata restituisce tutte le classi presenti all'interno di archivio SMIR, indipendentemente dal fatto che siano supportate dal dispositivo.</span><span class="sxs-lookup"><span data-stu-id="da444-118">Noncorrelated enumeration returns all classes present within the SMIR, regardless of whether the device supports them.</span></span> <span data-ttu-id="da444-119">Per ulteriori informazioni sull'utilizzo delle tecniche di correlazione WMI, vedere [WMI SNMP Class Correlation](wmi-snmp-class-correlation.md).</span><span class="sxs-lookup"><span data-stu-id="da444-119">For more information about using WMI correlation techniques, see [WMI SNMP Class Correlation](wmi-snmp-class-correlation.md).</span></span>

 

 



