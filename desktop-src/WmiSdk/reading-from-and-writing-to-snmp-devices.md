---
description: È possibile accedere ai dispositivi SNMP leggendo o scrivendo nell'istanza di classe corrispondente in WMI SMIR (SNMP Module Information Repository).
ms.assetid: af5e1321-b552-447e-a217-eecbebe1f203
ms.tgt_platform: multiple
title: Lettura e scrittura in dispositivi SNMP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c0419a5fc426c183ee1eb89a957a0c2f6a210ecd9b5d4612b6c4deb4e0f775a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118554256"
---
# <a name="reading-from-and-writing-to-snmp-devices"></a>Lettura e scrittura in dispositivi SNMP

È possibile accedere ai dispositivi SNMP leggendo o scrivendo nell'istanza di classe corrispondente in WMI SMIR (SNMP Module Information Repository). Quando si lavora con più dispositivi dello stesso tipo, per migliorare l'efficienza, caricare i MIB per un tipo di dispositivo SNMP in SMIR.

> [!Note]  
> Per altre informazioni sull'installazione del provider, vedere [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).

 

Selezionare una delle opzioni seguenti per leggere o scrivere da ogni tipo di dispositivo SNMP aggiornando le informazioni di contesto dell'istanza prima di comunicare con ognuno di essi.

-   Usare un nome DNS anziché l'indirizzo IP quando si fa riferimento a un dispositivo specifico.

    L'esempio seguente illustra come usare il nome DNS per un dispositivo specifico.

    ```VB
    strNamedValue = Context.Add("AgentAddress", "Router1" )
    ```

    

-   Creare uno spazio dei nomi separato e associare un indirizzo del dispositivo all'oggetto spazio dei nomi usando il qualificatore dell'istanza AgentAddress in modo che lo spazio dei nomi sia associato in modo permanente al dispositivo. In questo caso, non è necessario specificare le informazioni sull'oggetto contesto.
-   Leggere da un dispositivo SNMP.

    L'esempio seguente esegue un'operazione Get su una classe di dispositivi.

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

    Nell'esempio seguente viene eseguita un'operazione Set su una classe di dispositivi.

    ```VB
    Set objLocator = CreateObject("wbemscripting.swbemlocator")
    Set objServices = objLocator.ConnectServer(, "root\snmp\mngd_hub")
    objServices.security_.privileges.AddAsString("SeSecurityPrivilege")
    Set obj= objServices.Get("SNMP_NET_DEVICE_123=@")
    obj.deviceLocation = "40/5073"
    obj.put_
    ```

    

Le classi correlate sono quelle supportate da un determinato dispositivo SNMP quando si verifica l'enumerazione. La correlazione influisce sul set di classi restituito da SMIR. L'enumerazione non correlata restituisce tutte le classi presenti all'interno di SMIR, indipendentemente dal fatto che il dispositivo le supporti. Per altre informazioni sull'uso delle tecniche di correlazione WMI, vedere [Correlazione della classe SNMP WMI.](wmi-snmp-class-correlation.md)

 

 



