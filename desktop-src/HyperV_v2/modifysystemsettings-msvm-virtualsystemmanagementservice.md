---
description: Modifica le impostazioni della macchina virtuale.
ms.assetid: 3266bd0d-398b-4d3b-9248-e29c069aab11
title: Metodo ModifySystemSettings della classe Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifySystemSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4e6bf40b3dd206affcdc014e98554bfa8f88b4c2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106315488"
---
# <a name="modifysystemsettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Metodo ModifySystemSettings della classe MSVM \_ VirtualSystemManagementService

Modifica le impostazioni della macchina virtuale. Quando viene applicata alle impostazioni di sistema di una configurazione di macchina virtuale "corrente", come effetto collaterale è possibile che l'istanza della macchina virtuale venga modificata.

## <a name="syntax"></a>Sintassi


```mof
uint32 ModifySystemSettings(
  [in]  string              SystemSettings,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SystemSettings* \[ in\]
</dt> <dd>

Istanza incorporata della classe [**MSVM \_ VirtualSystemSettingData**](msvm-virtualsystemsettingdata.md) che contiene gli aspetti modificati della macchina virtuale. La proprietà **InstanceID** identifica l'impostazione della macchina virtuale da modificare.

</dd> <dt>

*Processo* \[ di out\]
</dt> <dd>

Se l'operazione viene eseguita in modo asincrono, questo metodo restituirà 4096 e questo parametro conterrà un riferimento a un oggetto derivato da [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Questo metodo restituisce uno dei valori seguenti.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Non supportato** (1)
</dt> <dt>

**Non riuscito** (2)
</dt> <dt>

**Timeout** (3)
</dt> <dt>

**Parametro non valido** (4)
</dt> <dt>

**Stato non valido** (5)
</dt> <dt>

**Parametri incompatibili** (6)
</dt> <dt>

**DMTF riservato** (..)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
</dt> <dt>

**Metodo riservato** (4097.. 32767)
</dt> <dt>

**Specifico del fornitore** (32768.. 65535)
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

[**ModifyVirtualSystem (V1)**](/previous-versions/windows/desktop/virtual/modifyvirtualsystem-msvm-virtualsystemmanagementservice)
</dt> <dt>

[**\_VirtualSystemManagementService MSVM**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

