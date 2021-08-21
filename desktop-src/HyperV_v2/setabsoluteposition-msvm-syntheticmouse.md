---
description: Imposta la posizione orizzontale e verticale del cursore del mouse.
ms.assetid: 7845E10A-7F61-4134-BF81-AED5483F36AD
title: Metodo SetAbsolutePosition della classe Msvm_SyntheticMouse (Dbdao.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.SetAbsolutePosition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1f7f04975d85be1cb176839c80c19710534237b3be15ca06e606dad58a099519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014309"
---
# <a name="setabsoluteposition-method-of-the-msvm_syntheticmouse-class"></a>Metodo SetAbsolutePosition della classe Msvm \_ SyntheticMouse

Imposta la posizione orizzontale e verticale del cursore del mouse.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetAbsolutePosition(
  [in] sint32 horizontalPosition,
  [in] sint32 verticalPosition
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*horizontalPosition* \[ Pollici\]
</dt> <dd>

Tipo: **sint32**

Nuova posizione orizzontale del cursore del mouse, in pixel.

</dd> <dt>

*verticalPosition* \[ Pollici\]
</dt> <dd>

Tipo: **sint32**

Nuova posizione verticale del cursore del mouse, in pixel.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Un valore restituito pari a zero indica l'esito positivo. Un valore diverso da zero indica un errore di modifica della posizione di scorrimento.

<dl> <dt>

**Completato senza errori** (0)
</dt> <dt>

**Parametri del metodo controllati - Processo avviato** (4096)
</dt> <dt>

**Operazione non** riuscita (32768)
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
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| Intestazione<br/>                   | <dl> <dt>Dbdao.h</dt> </dl>                      |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ SyntheticMouse**](msvm-syntheticmouse.md)
</dt> </dl>

 

