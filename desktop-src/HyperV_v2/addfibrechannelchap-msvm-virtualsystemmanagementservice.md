---
description: Aggiunge i parametri DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) a una porta di Fibre Channel sintetica in una macchina virtuale.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Metodo AddFibreChannelChap della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 07151a902efa8f8077debc44bd732286c0a96a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103967558"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo AddFibreChannelChap della classe MSVM \_ VirtualSystemManagementService

Aggiunge i parametri DH-CHAP (Diffie Hellman-Challenge Handshake Authentication Protocol) a una porta di Fibre Channel sintetica in una macchina virtuale. Questo metodo avrà esito negativo se la macchina virtuale è in esecuzione.

## <a name="syntax"></a>Sintassi


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FcPortSettings* \[ in\]
</dt> <dd>

Matrice di stringhe che contengono un'istanza incorporata della classe [**MSVM \_ SyntheticFcPortSettingData**](msvm-syntheticfcportsettingdata.md) che descrive le impostazioni per le porte Fibre Channel sintetiche per le macchine virtuali. La proprietà **InstanceID** di ognuna di queste istanze identifica gli elementi da modificare.

</dd> <dt>

*SecretEncoding* \[ in\]
</dt> <dd>

Specifica il tipo di codifica per il segreto condiviso.

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

**ASCII stampabile** (1)


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

**Binario** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*SharedSecret* \[ in\]
</dt> <dd>

Specifica il segreto condiviso.

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

 

 




