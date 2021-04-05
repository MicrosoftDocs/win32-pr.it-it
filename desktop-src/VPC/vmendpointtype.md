---
title: Enumerazione VMEndpointType (VPCCOMInterfaces. h)
description: Specifica il tipo di endpoint.
ms.assetid: b48bd860-50dc-4c8c-b65b-69c407d4612a
keywords:
- VMEndpointType enumerazione PC virtuale
topic_type:
- apiref
api_name:
- VMEndpointType
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912eb43147af03dd2b9923c4bdb778044f40d023
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103873737"
---
# <a name="vmendpointtype-enumeration"></a>Enumerazione VMEndpointType

\[Windows Virtual PC non è più disponibile per l'uso a partire da Windows 8. Usare invece il [provider WMI Hyper-V (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Specifica il tipo di endpoint.

## <a name="syntax"></a>Sintassi


```C++
typedef enum  { 
  vmEndpoint_NamedPipe  = 0,
  vmEndpoint_TCPIP      = 1
} VMEndpointType;
```



## <a name="constants"></a>Costanti

<dl> <dt>

<span id="vmEndpoint_NamedPipe"></span><span id="vmendpoint_namedpipe"></span><span id="VMENDPOINT_NAMEDPIPE"></span>**\_NamedPipe vmEndpoint**
</dt> <dd>

Lato host.

</dd> <dt>

<span id="vmEndpoint_TCPIP"></span><span id="vmendpoint_tcpip"></span><span id="VMENDPOINT_TCPIP"></span>**vmEndpoint \_ Tcpip**
</dt> <dd>

Lato Guest.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 7\]<br/>                                                    |
| Server minimo supportato<br/> | Nessuno supportato<br/>                                                                     |
| Fine del supporto client<br/>    | Windows 7<br/>                                                                          |
| Prodotto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Intestazione<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**IVMVirtualMachine::StartCommunicationChannel**](ivmvirtualmachine-startcommunicationchannel.md)
</dt> </dl>

 

