---
description: Imposta lo stato corrente del pulsante del dispositivo specificato.
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: Metodo SetButtonState della classe Msvm_SyntheticMouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c99915fa8ede9cbb405f4483ac10ca9ff8efaf71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104227418"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a>Metodo SetButtonState della classe MSVM \_ SyntheticMouse

Imposta lo stato corrente del pulsante del dispositivo specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean isDown
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ButtonIndex* \[ in\]
</dt> <dd>

Tipo: **UInt32**

Indice in base 1 del pulsante da modificare.

</dd> <dt>

in *basso* \[ in\]
</dt> <dd>

Tipo: **booleano**

Nuovo stato di inattività del pulsante. Un valore **true** indica che il pulsante è inattivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

I valori diversi da zero indicano un errore di modifica dello stato del pulsante.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati-processo avviato** (4096)
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

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per l'operazione** (32775)
</dt> <dt>

**Tipo di dati non corretto** (32776)
</dt> <dt>

**Sistema non disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe \_ SyntheticMouse di MSVM**](msvm-syntheticmouse.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_SyntheticMouse MSVM**](msvm-syntheticmouse.md)
</dt> </dl>

 

