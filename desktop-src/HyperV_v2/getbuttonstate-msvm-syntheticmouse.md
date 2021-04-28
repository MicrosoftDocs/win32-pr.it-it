---
description: 'Metodo GetButtonState della Msvm_SyntheticMouse classe : recupera lo stato corrente del pulsante del dispositivo specificato.'
ms.assetid: 66363AF1-E360-478D-8E62-513DE66EF130
title: Metodo GetButtonState della Msvm_SyntheticMouse classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticMouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 26839292cf2fb3099e740629b28c7de0fbe3f60f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119389"
---
# <a name="getbuttonstate-method-of-the-msvm_syntheticmouse-class"></a>Metodo GetButtonState della classe SyntheticMouse Msvm \_

Recupera lo stato corrente del pulsante del dispositivo specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean isDown
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*buttonIndex* \[ Pollici\]
</dt> <dd>

Tipo: **uint32**

Indice in base 1 del pulsante su cui eseguire la query.

</dd> <dt>

*isDown* \[ Cambio\]
</dt> <dd>

Tipo: **booleano**

Stato corrente verso il basso del pulsante. Un **valore True** indica che il pulsante è in basso.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **uint32**

Un valore restituito pari a zero indica l'esito positivo. Un valore diverso da zero indica un errore di query.

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

 

