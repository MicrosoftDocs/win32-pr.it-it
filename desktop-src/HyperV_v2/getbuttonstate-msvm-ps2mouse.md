---
description: Recupera lo stato corrente del pulsante del dispositivo specificato.
ms.assetid: 7772A3AC-1677-44A7-9E5E-D31E90988705
title: Metodo GetButtonState della classe Msvm_Ps2Mouse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Ps2Mouse.GetButtonState
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8bb0df6ad49f0d260d95c6f65e0f0f481b393dc3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106307755"
---
# <a name="getbuttonstate-method-of-the-msvm_ps2mouse-class"></a>Metodo GetButtonState della classe MSVM \_ Ps2mouse

Recupera lo stato corrente del pulsante del dispositivo specificato.

## <a name="syntax"></a>Sintassi


```mof
uint32 GetButtonState(
  [in]  uint32  buttonIndex,
  [out] boolean buttonState
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ButtonIndex* \[ in\]
</dt> <dd>

Tipo: **UInt32**

Indice in base 1 del pulsante su cui eseguire una query.

</dd> <dt>

*ButtonState* \[ out\]
</dt> <dd>

Tipo: **booleano**

Stato di inattività corrente del pulsante. Un valore **true** indica che il pulsante è inattivo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Tipo: **UInt32**

Un valore restituito pari a zero indica esito positivo. Un valore diverso da zero indica un errore di query.

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

L'accesso alla [**classe \_ Ps2Mouse di MSVM**](msvm-ps2mouse.md) potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

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

[**\_Ps2Mouse MSVM**](msvm-ps2mouse.md)
</dt> </dl>

 

