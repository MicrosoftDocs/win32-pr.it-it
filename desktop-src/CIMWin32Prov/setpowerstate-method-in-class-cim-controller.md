---
description: 'Metodo SetPowerState della classe CIM_Controller: il metodo SetPowerState imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.'
ms.assetid: 442c6c2c-8e9a-476c-bb57-8b1a6439e97f
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_Controller
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Controller.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 0b8956afb9547f949f68007e7e2da7d2dce4f9f46a2e45cb66ea838ad206ad45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439621"
---
# <a name="setpowerstate-method-of-the-cim_controller-class"></a>Metodo SetPowerState della classe controller CIM \_

Il **metodo SetPowerState** imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato. In una sottoclasse, il set di codici restituiti possibili deve essere specificato usando un **qualificatore ValueMap** nel metodo. Le stringhe in cui viene convertito **il contenuto di ValueMap** devono essere specificate anche nella sottoclasse come **qualificatore di** matrice Values. Questo metodo viene ereditato da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PowerState* \[ Pollici\]
</dt> <dd>

Valore **ValueMap** che specifica lo stato di alimentazione desiderato per il dispositivo logico.

<dt>

1
</dt> <dd>

Potenza completa.

</dd> <dt>

2
</dt> <dd>

Risparmio energia in modalità a basso consumo.

</dd> <dt>

3
</dt> <dd>

Risparmio energia standby.

</dd> <dt>

4
</dt> <dd>

Risparmio energia altro.

</dd> <dt>

5
</dt> <dd>

Ciclo di alimentazione.

</dd> <dt>

6
</dt> <dd>

Disattivare l'alimentazione.

</dd> </dl> </dd> <dt>

*Ora* \[ Pollici\]
</dt> <dd>

Specifica quando deve essere impostato lo stato di alimentazione, come valore di data e ora regolare o come valore di intervallo (dove l'intervallo inizia quando viene ricevuta la chiamata al metodo). Quando il *parametro PowerState* è uguale a 5 ("Ciclo di alimentazione"), il parametro *Time* indica quando il dispositivo deve essere ri accensione. L'accensione è immediata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 (zero) in caso di esito positivo, 1 (uno) se la richiesta *PowerState* e *Time* specificata non è supportata e un altro valore se si è verificato un altro errore.

## <a name="remarks"></a>Commenti

Questo metodo non è attualmente implementato da WMI. Per usare questo metodo, è necessario implementarlo nel proprio provider. Per altre informazioni, vedere [Creazione di provider WMI.](/windows/desktop/WmiSdk/creating-wmi-providers)

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere errori secondari, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[CIM \_ Controller](setpowerstate-method-in-class-cim-controller.md)
</dt> <dt>

[**CIM \_ Controller**](cim-controller.md)
</dt> </dl>

 

