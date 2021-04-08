---
description: Definire il set di azioni per l' \_ archiviazione IOCTL \_ gestire il codice di controllo degli attributi del \_ set di dati \_ \_ .
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524d1dbd2ecf09dbcfa66fa766089dde7cf04a0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877749"
---
# <a name="device_data_management_set_action"></a>\_ \_ azione set di gestione dati \_ del \_ dispositivo

I valori costanti seguenti sono il set di valori possibili per il tipo di **\_ \_ \_ \_ azione set di gestione dati del dispositivo** , definito come tipo **DWORD**.

<dl> <dt>

<span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ None**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Non viene eseguita alcuna azione.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction \_ Trim**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Viene eseguita un'azione trim.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**\_Notifica DeviceDsmAction**
</dt> <dd> <dl> <dt>

2 \| **DeviceDsmActionFlag non \_ distruttivo** (0x80000002)
</dt> <dt>



Viene eseguita un'azione di notifica. I parametri si trovano in una struttura di [**\_ \_ \_ parametri di notifica DSM del dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) . Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**\_OffloadRead DeviceDsmAction**
</dt> <dd> <dl> <dt>

3 \| **DeviceDsmActionFlag non \_ distruttivi** (0x80000003)
</dt> <dt>



Viene eseguita un'azione di lettura offload. I parametri si trovano in una struttura di [**\_ parametri di \_ \_ lettura \_ di OFFLOAD DSM del dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) . L'output si trova in una struttura di [**\_ \_ \_ output di lettura OFFLOAD archiviazione**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) . Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**\_OffloadWrite DeviceDsmAction**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Viene eseguita un'azione di scrittura di offload. I parametri si trovano in una struttura di [**\_ parametri di \_ \_ scrittura \_ di OFFLOAD DSM del dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) . L'output si trova in una struttura di [**output di scrittura di OFFLOAD dell'archiviazione \_ \_ \_**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output) .

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**Allocazione DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

5 \| **DeviceDsmActionFlag non \_ distruttivi** (0x80000005)
</dt> <dt>



Viene restituita una bitmap di allocazione per il primo intervallo di set di dati passato. L'output si trova in una struttura di [**\_ \_ \_ \_ \_ stato di provisioning LB del set di dati del dispositivo**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) . Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**\_Ripristino DeviceDsmAction**
</dt> <dd> <dl> <dt>

6 \| **DeviceDsmActionFlag non \_ distruttivi** (0x80000006)
</dt> <dt>



Viene eseguita un'azione di ripristino. Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction \_ scrub**
</dt> <dd> <dl> <dt>

7 \| **DeviceDsmActionFlag non \_ distruttivi** (0x80000007)
</dt> <dt>



Viene eseguita un'azione di scrub. Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**\_Resilienza DeviceDsmAction**
</dt> <dd> <dl> <dt>

8 \| **DeviceDsmActionFlag non \_ distruttivi** (0x80000008)
</dt> <dt>



Viene eseguita un'azione di resilienza. Il **DeviceDsmActionFlag non \_ distruttivo** (0x80000000) è un flag di bit per indicare allo stack del driver che questa operazione non è distruttiva.

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                         |
| Intestazione<br/>                   | <dl> <dt>WinIoCtl. h (include Windows. h)</dt> </dl> |



 

 




