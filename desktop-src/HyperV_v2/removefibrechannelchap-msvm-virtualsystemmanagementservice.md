---
description: Rimuove i parametri DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) da una porta Fibre Channel sintetica in una macchina virtuale.
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
ms.openlocfilehash: 9b934839f6d908594ee58f0838c884fdedc48f372de061482ddf2147123a351c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147794"
---
# <a name="removefibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo RemoveFibreChannelChap della classe Msvm \_ VirtualSystemManagementService

Rimuove i parametri DH-CHAP (Diffie Hellman - Challenge Handshake Authentication Protocol) da una porta Fibre Channel sintetica in una macchina virtuale. Questo metodo avrà esito negativo se la macchina virtuale è in esecuzione.

## <a name="syntax"></a>Sintassi


```mof
uint32 RemoveFibreChannelChap(
  [in] string FcPortSettings[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FcPortSettings* \[ Pollici\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata della classe [**Msvm \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) che definiscono le porte Fibre Channel sintetiche da cui rimuovere i parametri DH-CHAP. La **proprietà InstanceID** di ognuna di queste istanze identifica gli elementi da modificare.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Non riuscito** (32768)
</dt> <dt>

**Accesso negato** (32769)
</dt> <dt>

**Non supportato** (32770)
</dt> <dt>

**Lo stato è sconosciuto** (32771)
</dt> <dt>

**Timeout** (32772)
</dt> <dt>

**Parametro non** valido (32773)
</dt> <dt>

**Il sistema è in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




