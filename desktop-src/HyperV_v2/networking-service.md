---
description: Il profilo di rete descrive gli oggetti utilizzati per configurare il sistema in modo da consentire alle macchine virtuali di comunicare in rete.
ms.assetid: A5C4866B-0F65-47B5-8FC4-B92943842B86
title: Servizio di rete
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc85b7a5121a3e7e42f333f829816184b57bd8eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106306626"
---
# <a name="networking-service"></a>Servizio di rete

Il profilo di rete descrive gli oggetti utilizzati per configurare il sistema in modo da consentire alle macchine virtuali di comunicare in rete. Gli oggetti di rete globali, usati per configurare lo switch di rete nel sistema operativo di gestione, includono le classi [**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md), [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)e [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) . Gli oggetti di rete della macchina virtuale, usati per configurare la scheda di interfaccia di rete (NIC) nella macchina virtuale, includono le classi [**MSVM \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md), [**MSVM \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md)e [**MSVM \_ LANEndpoint**](msvm-lanendpoint.md) .

La radice del profilo di rete globale è la classe [**MSVM \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) . Questa classe rappresenta un dispositivo switch virtuale nel sistema operativo di gestione. **MSVM \_ VirtualEthernetSwitch** è associato a istanze della classe [**\_ SwitchPort di MSVM**](https://www.bing.com/search?q=**Msvm\_SwitchPort**) , che rappresenta le porte nel commutire virtuale. Le istanze delle classi **MSVM \_ VirtualEthernetSwitch** e [**MSVM \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) vengono create, eliminate e connesse tramite la classe MSVM [**\_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) (non illustrato nella figura precedente).

Il servizio di gestione del commutatore virtuale (VSMS) rappresenta il servizio di rete presente in un singolo host Hyper-V e contiene metodi per [**MSVM \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md) utilizzati per controllare la definizione, la modifica e la distruzione delle risorse di rete globali, ad esempio commutatori virtuali, porte del commutatore e porte Ethernet interne.

La rappresentazione del dispositivo NIC Ethernet nella macchina virtuale ha un aspetto molto simile a quello di qualsiasi altro dispositivo, come descritto nel [**servizio Virtual System Management**](virtual-system-management-service.md). Le classi [**MSVM \_ EmulatedEthernetPort**](msvm-emulatedethernetport.md) e [**MSVM \_ SyntheticEthernetPort**](msvm-syntheticethernetport.md) rappresentano il dispositivo NIC virtuale e vengono configurate tramite un' [**istanza \_ MSVM ResourceAllocationSettingData (RASD**](msvm-resourceallocationsettingdata.md) ) associata. L'unica caratteristica insolita di questa rappresentazione è che, quando viene creata un'istanza della macchina virtuale e crea a sua volta i dispositivi **MSVM \_ EmulatedEthernetPort** e **MSVM \_ SyntheticEthernetPort** , viene creata anche [**un'istanza MSVM LANEndpoint associata \_**](msvm-lanendpoint.md) per la scheda di interfaccia di rete virtuale. Analogamente, quando la macchina virtuale viene salvata o disattivata e le istanze **MSVM \_ EmulatedEthernetPort** e **MSVM \_ SyntheticEthernetPort** vengono distrutte, viene distrutta anche [**l'istanza di MSVM VmLANEndpoint \_**](https://www.bing.com/search?q=**Msvm\_VmLANEndpoint**) associata. Lo scopo di **MSVM \_ LANEndpoint** è di fungere da Bridge per la connessione tra due porte di rete. In questo caso, viene usato per connettere una scheda di interfaccia di rete virtuale a una porta sul dispositivo del Commuter virtuale. In altre parole, connette le istanze **MSVM \_ EmulatedEthernetPort** e **MSVM \_ SyntheticEthernetPort** nella macchina virtuale a una particolare istanza di [**MSVM \_ EthernetSwitchPort nel**](msvm-ethernetswitchport.md) Commuter virtuale. Per connettere un'opzione all'esterno, è necessario associare la porta Ethernet fisica a [**MSVM \_ VirtualSwitch**](https://www.bing.com/search?q=**Msvm\_VirtualSwitch**) tramite [**BindExternalEthernetPort**](https://www.bing.com/search?q=**BindExternalEthernetPort**). Quando si connette un comportatore allo stack di rete host o una scheda di interfaccia di rete interna, è possibile usare ConnectInternal per fare in modo che una macchina virtuale comunichi con l'host e non con il mondo esterno. [**MSVM \_ ActiveConnection**](msvm-activeconnection.md) connette una porta di commutazione alla [**\_ SwitchLANEndpoint MSVM**](https://www.bing.com/search?q=**Msvm\_SwitchLANEndpoint**) a cui è connessa la porta all'interno di Hyper-V. L'esistenza di questo oggetto significa che la porta di commutazione e **il \_ SwitchLANEndpoint MSVM** sono connessi attivamente e la porta Ethernet associata **a \_ MSVM LANEndpoint** può comunicare con la rete tramite la porta di commutazione.

 

 



