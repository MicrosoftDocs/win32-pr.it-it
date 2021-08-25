---
description: Imposta lo stato di alimentazione del dispositivo. L'uso di questo metodo è stato deprecato. Usare invece il metodo SetPowerState nella classe PowerManagementService associata.
ms.assetid: 2f53a8bd-18a8-45aa-92ad-68a33b6a42ab
title: Metodo SetPowerState della classe CIM_LogicalDevice (gestione di Hyper-V)
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
- vmms.exe
ms.openlocfilehash: 149145a3433b55cb8c71dc4affdea9a00b4cbd6696d77b91cfe6258b2f6e010e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119900271"
---
# <a name="setpowerstate-method-of-the-cim_logicaldevice-class-hyper-v-management"></a>Metodo SetPowerState della classe CIM_LogicalDevice (gestione di Hyper-V)

Imposta lo stato di alimentazione del dispositivo. L'uso di questo metodo è stato deprecato. Usare invece il **metodo SetPowerState** nella classe **PowerManagementService** associata.

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

Stato di alimentazione da impostare.

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

**Alimentazione completa** (1)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

**Risparmio energia - Modalità a basso consumo** (2)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

**Risparmio energia - Standby** (3)


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

**Risparmio energia - Altro** (4)


</dt> <dd></dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

**Ciclo di alimentazione** (5)


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

**Power Off** (6)


</dt> <dd></dd> </dl> </dd> <dt>

*Ora* \[ Pollici\]
</dt> <dd>

Ora indica quando deve essere impostato lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo (dove l'intervallo inizia quando viene ricevuta la chiamata al metodo).

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore 0 se l'operazione ha esito positivo. In caso contrario, restituisce un errore.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 8.1<br/>                                                                                  |
| Server minimo supportato<br/> | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




