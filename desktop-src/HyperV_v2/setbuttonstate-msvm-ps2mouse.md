---
description: 'Metodo SetButtonState della classe Msvm_Ps2Mouse : imposta lo stato corrente del pulsante del dispositivo specificato.'
ms.assetid: 312A2B8B-D518-4797-9B50-F12493598CD6
title: Metodo SetButtonState della classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.SetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b8ccc67590861a07b8a1d0181c43530a19d27e3f9426f3c6c363be44c0996f78
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119822891"
---
# <a name="setbuttonstate-method-of-the-msvm_ps2mouse-class"></a>Metodo SetButtonState della classe Msvm \_ Ps2Mouse

Imposta lo stato corrente del pulsante del dispositivo specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetButtonState(
  [in] uint32  buttonIndex,
  [in] boolean buttonState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*buttonIndex* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Indice in base 1 del pulsante da modificare.

</dd> <dt>

*buttonState* \[ Pollici\]
</dt> <dd>

Tipo: **booleano**

Nuovo stato verso il basso del pulsante. Il **valore True** indica che il pulsante è in basso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Un valore restituito pari a zero indica l'esito positivo. Un valore diverso da zero indica un errore di modifica dello stato del pulsante.

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

L'accesso alla [**classe Msvm \_ Ps2Mouse**](msvm-ps2mouse.md) potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ Ps2Mouse**](msvm-ps2mouse.md)
</dt> </dl>

 

