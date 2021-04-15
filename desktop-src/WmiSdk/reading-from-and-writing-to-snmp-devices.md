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
# <a name="reading-from-and-writing-to-snmp-devices"></a>Lettura e scrittura nei dispositivi SNMP

È possibile accedere ai dispositivi SNMP leggendo o scrivendo nell'istanza della classe corrispondente nel archivio SMIR WMI (archivio informazioni del modulo SNMP). Quando si usano più dispositivi dello stesso tipo, per maggiore efficienza caricare il MIB per un tipo di dispositivo SNMP in archivio SMIR.

> [!Note]  
> Per ulteriori informazioni sull'installazione del provider, vedere [configurazione dell'ambiente WMI SNMP](setting-up-the-wmi-snmp-environment.md).

 

Selezionare una delle opzioni seguenti per leggere o scrivere da ogni tipo di dispositivo SNMP aggiornando le informazioni di contesto dell'istanza prima della comunicazione con ognuna di esse.

-   Usare un nome DNS anziché l'indirizzo IP quando si fa riferimento a un dispositivo specifico.

    L'esempio seguente illustra come usare il nome DNS per un dispositivo specifico.

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   Creare uno spazio dei nomi separato e associare un indirizzo del dispositivo all'oggetto spazio dei nomi utilizzando il qualificatore dell'istanza AgentAddress in modo che lo spazio dei nomi venga associato definitivamente al dispositivo. In questo caso, non è necessario specificare le informazioni sull'oggetto di contesto.
-   Leggere da un dispositivo SNMP.

    Nell'esempio seguente viene eseguita un'operazione get su una classe del dispositivo.

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

    

-   Scrivere in un dispositivo SNMP.

    Nell'esempio seguente viene eseguita un'operazione di impostazione su una classe del dispositivo.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

Le classi correlate sono quelle che un determinato dispositivo SNMP è in grado di supportare quando si verifica l'enumerazione. La correlazione influiscono sul set di classi restituite da archivio SMIR. L'enumerazione non correlata restituisce tutte le classi presenti all'interno di archivio SMIR, indipendentemente dal fatto che siano supportate dal dispositivo. Per ulteriori informazioni sull'utilizzo delle tecniche di correlazione WMI, vedere [WMI SNMP Class Correlation](wmi-snmp-class-correlation.md).

 

 



