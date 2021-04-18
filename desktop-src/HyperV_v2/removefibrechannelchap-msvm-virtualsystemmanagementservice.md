---
description: Rimuove i parametri DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) da una porta Fibre Channel sintetica in una macchina virtuale.
ms.assetid: f15673e2-287d-4e87-bee4-6c0f5f9178c8
title: Metodo RemoveFibreChannelChap della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.RemoveFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 06e944c3c592b0b61ace8a72b5d42a801ab0f5df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307872"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo RemoveFibreChannelChap della classe MSVM \_ VirtualSystemManagementService

Rimuove i parametri DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) da una porta Fibre Channel sintetica in una macchina virtuale. Questo metodo avrà esito negativo se la macchina virtuale è in esecuzione.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FcPortSettings* \[ in\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata della classe [**\_ SyntheticFcPortSettingData MSVM**](msvm-syntheticfcportsettingdata.md) che definiscono le porte sintetiche Fibre Channel per la rimozione dei parametri DH-CHAP da. La proprietà **InstanceID** di ognuna di queste istanze identifica gli elementi da modificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Stato sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non valido** (32773)
</dt> <dt>

Il **sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




