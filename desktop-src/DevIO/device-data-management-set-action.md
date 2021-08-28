---
description: Definire il set di azioni per il codice di controllo IOCTL \_ STORAGE MANAGE DATA SET \_ \_ \_ \_ ATTRIBUTES.
ms.assetid: ff688c9a-8669-4699-aab9-1e2e3a5c7fca
title: DEVICE_DATA_MANAGEMENT_SET_ACTION (WinIoCtl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 602243e31645e1cc4706e3a3a2b954bb68fc2cbda58a0f0b6c9076ae6b0797f3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654921"
---
# <a name="device_data_management_set_action"></a>AZIONE \_ DEL SET DI GESTIONE DEI DATI DEI \_ \_ \_ DISPOSITIVI

I valori costanti seguenti sono il set di valori possibili per il tipo **DEVICE DATA MANAGEMENT SET \_ \_ \_ \_ ACTION,** definito come **tipo DWORD**.

<dl> <dt>

<span id="DeviceDsmAction_None"></span><span id="devicedsmaction_none"></span><span id="DEVICEDSMACTION_NONE"></span>**DeviceDsmAction \_ Nessuno**
</dt> <dd> <dl> <dt>

0
</dt> <dt>



Non viene eseguita alcuna azione.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Trim"></span><span id="devicedsmaction_trim"></span><span id="DEVICEDSMACTION_TRIM"></span>**DeviceDsmAction \_ Trim**
</dt> <dd> <dl> <dt>

1
</dt> <dt>



Viene eseguita un'azione di taglio.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Notification"></span><span id="devicedsmaction_notification"></span><span id="DEVICEDSMACTION_NOTIFICATION"></span>**Notifica \_ DeviceDsmAction**
</dt> <dd> <dl> <dt>

2 \| **DeviceDsmActionFlag \_ NonDestructive** (0x80000002)
</dt> <dt>



Viene eseguita un'azione di notifica. I parametri sono in una [**struttura DEVICE \_ DSM NOTIFICATION \_ \_ PARAMETERS.**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_notification_parameters) **DeviceDsmActionFlag \_ NonDestructive** (0x80000000) è un flag di bit per indicare nello stack del driver che questa operazione non è distruttiva.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadRead"></span><span id="devicedsmaction_offloadread"></span><span id="DEVICEDSMACTION_OFFLOADREAD"></span>**DeviceDsmAction \_ OffloadRead**
</dt> <dd> <dl> <dt>

3 \| **DeviceDsmActionFlag \_ NonDestructive** (0x80000003)
</dt> <dt>



Viene eseguita un'azione di lettura offload. I parametri sono in una [**struttura DEVICE \_ DSM \_ OFFLOAD READ \_ \_ PARAMETERS.**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_read_parameters) L'output si trova in [**una struttura STORAGE \_ OFFLOAD READ \_ \_ OUTPUT.**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_read_output) **DeviceDsmActionFlag \_ NonDestructive** (0x80000000) è un flag di bit per indicare nello stack del driver che questa operazione non è distruttiva.

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_OffloadWrite"></span><span id="devicedsmaction_offloadwrite"></span><span id="DEVICEDSMACTION_OFFLOADWRITE"></span>**DeviceDsmAction \_ OffloadWrite**
</dt> <dd> <dl> <dt>

4
</dt> <dt>



Viene eseguita un'azione di scrittura offload. I parametri sono in una [**struttura DEVICE \_ DSM \_ OFFLOAD WRITE \_ \_ PARAMETERS.**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_dsm_offload_write_parameters) L'output si trova in [**una struttura STORAGE \_ OFFLOAD WRITE \_ \_ OUTPUT.**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_offload_write_output)

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Allocation"></span><span id="devicedsmaction_allocation"></span><span id="DEVICEDSMACTION_ALLOCATION"></span>**Allocazione DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

5 \| **DeviceDsmActionFlag \_ NonDestructive** (0x80000005)
</dt> <dt>



Viene restituita una bitmap di allocazione per il primo intervallo di set di dati passato. L'output si trova in [**una struttura DEVICE DATA SET \_ \_ \_ LB PROVISIONING \_ \_ STATE.**](/windows/desktop/api/WinIoCtl/ns-winioctl-device_data_set_lb_provisioning_state) **DeviceDsmActionFlag \_ NonDestructive** (0x80000000) è un flag di bit per indicare nello stack del driver che questa operazione non è distruttiva.

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Repair"></span><span id="devicedsmaction_repair"></span><span id="DEVICEDSMACTION_REPAIR"></span>**Ripristino di \_ DeviceDsmAction**
</dt> <dd> <dl> <dt>

6 \| **DeviceDsmActionFlag \_ NonDestructive** (0x80000006)
</dt> <dt>



Viene eseguita un'azione di ripristino. **DeviceDsmActionFlag \_ NonDestructive** (0x80000000) è un flag di bit per indicare nello stack del driver che questa operazione non è distruttiva.

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Scrub"></span><span id="devicedsmaction_scrub"></span><span id="DEVICEDSMACTION_SCRUB"></span>**DeviceDsmAction \_ Scrub**
</dt> <dd> <dl> <dt>

7 \| **DeviceDsmActionFlag \_ NonDestructive** (0x80000007)
</dt> <dt>



Viene eseguita un'azione di scrubbing. **DeviceDsmActionFlag \_ NonDestructive** (0x80000000) è un flag di bit per indicare nello stack del driver che questa operazione non è distruttiva.

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> <dt>

<span id="DeviceDsmAction_Resiliency"></span><span id="devicedsmaction_resiliency"></span><span id="DEVICEDSMACTION_RESILIENCY"></span>**Resilienza di DeviceDsmAction \_**
</dt> <dd> <dl> <dt>

8 \| **DeviceDsmActionFlag \_ NonDestructive** (0x80000008)
</dt> <dt>



Viene eseguita un'azione di resilienza. **DeviceDsmActionFlag \_ NonDestructive** (0x80000000) è un flag di bit per indicare nello stack del driver che questa operazione non è distruttiva.

**Windows 7 e Windows Server 2008 R2:** Questo valore non è supportato prima di Windows 8 e Windows Server 2012.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 7<br/>                                                                                      |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                                         |
| Intestazione<br/>                   | <dl> <dt>WinIoCtl.h (includere Windows.h)</dt> </dl> |



 

 




