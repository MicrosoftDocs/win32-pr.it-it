---
description: Il metodo SetPowerState della classe CIM LogicalDevice imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve \_ essere inserito in tale stato.
ms.assetid: 0d9678e0-a956-45d3-ac41-5c1604478fd7
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_LogicalDevice (provider WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_LogicalDevice.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 23093858f034a128c08ac2c39343a51a1d73de229440b444d37e777e2b0d0ba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439441"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-cimwin32-wmi-providers"></a>Metodo SetPowerState della classe CIM_LogicalDevice (provider WMI CIMWin32)

Il **metodo SetPowerState** della classe CIM LogicalDevice imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve \_ essere inserito in tale stato.

> [!IMPORTANT]
> Le classi CIM DMTF (Distributed Management Task Force) (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Alimentazione completa** (1)


</dt> <dd>

Potenza completa.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Risparmio energia - Modalità a basso consumo** (2)


</dt> <dd>

Risparmio energia in modalità a basso consumo.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Risparmio energia - Standby** (3)


</dt> <dd>

Risparmio energia standby.

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Risparmio energia - Altro** (4)


</dt> <dd>

Risparmio energia altro.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo di alimentazione** (5)


</dt> <dd>

Ciclo di alimentazione.

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (6)


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

In una sottoclasse, il set di codici restituiti possibili deve essere specificato usando un **qualificatore ValueMap** nel metodo. Le stringhe in cui viene convertito **il contenuto di ValueMap** devono essere specificate anche nella sottoclasse come **qualificatore di** matrice Values. Questo metodo viene ereditato da [**CIM \_ LogicalDevice.**](cim-logicaldevice.md)

Questo metodo non è attualmente implementato da WMI. Per usare questo metodo, è necessario implementarlo nel proprio provider.

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

[CIM \_ LogicalDevice](setpowerstate-method-in-class-cim-logicaldevice.md)
</dt> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




