---
description: 'Metodo SetButtonState della classe Msvm_SyntheticMouse : imposta lo stato corrente del pulsante del dispositivo specificato.'
ms.assetid: 942DB31C-09A2-43B6-A666-267AF6A84E0E
title: Metodo SetButtonState della Msvm_SyntheticMouse classe
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
ms.openlocfilehash: 161520ac1b7e9dba1a084a8fb3c623155aa135fe
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109209"
---
# <a name="setbuttonstate-method-of-the-msvm_syntheticmouse-class"></a>Metodo SetButtonState della classe SyntheticMouse Msvm \_

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

*buttonIndex* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Indice in base 1 del pulsante da modificare.

</dd> <dt>

*isDown* \[ Pollici\]
</dt> <dd>

Tipo: **booleano**

Nuovo stato verso il basso del pulsante. Un **valore True** indica che il pulsante è in basso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

I valori diversi da zero indicano un errore di modifica dello stato del pulsante.

<dl> <dt>

**Completata senza errori** (0)
</dt> <dt>

**Parametri del metodo verificati - Processo avviato** (4096)
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

**Sistema in uso** (32774)
</dt> <dt>

**Stato non valido per questa operazione** (32775)
</dt> <dt>

**Tipo di dati non** corretto (32776)
</dt> <dt>

**Il sistema non è disponibile** (32777)
</dt> <dt>

**Memoria insufficiente** (32778)
</dt> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla [**classe Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md) potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8 solo \[ app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | Solo app desktop di Windows Server 2012 \[\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md)
</dt> </dl>

 

