---
description: Il metodo SetPowerState definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.
ms.assetid: 3808b75d-229e-44c0-a1bc-aa260590cd36
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_AggregatePSExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePSExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9c3c973306d1861c8a0ec725aca9d00e2e8d569
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103966181"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepsextent-class"></a>Metodo SetPowerState della classe CIM \_ AggregatePSExtent

Il metodo **SetPowerState** definisce lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato. In una sottoclasse, è necessario specificare il set di codici restituiti possibili, usando un qualificatore **ValueMap** nel metodo. Le stringhe a cui viene convertito il contenuto **ValueMap** devono essere specificate anche nella sottoclasse come qualificatore della matrice di **valori** . Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Sintassi


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*PowerState* \[ in\]
</dt> <dd>

Valore **ValueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.

<dt>

1
</dt> <dd>

Potenza completa

</dd> <dt>

2
</dt> <dd>

Risparmio energia-modalità a basso consumo

</dd> <dt>

3
</dt> <dd>

Risparmio energia-standby

</dd> <dt>

4
</dt> <dd>

Risparmio energia-altro

</dd> <dt>

5
</dt> <dd>

Ciclo di alimentazione

</dd> <dt>

6
</dt> <dd>

Spegnimento

</dd> </dl> </dd> <dt>

*Ora* \[ di in\]
</dt> <dd>

Quando è necessario impostare lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo (dove l'intervallo inizia quando viene ricevuta la chiamata al metodo). Quando il parametro *PowerState* è uguale a 5, (ciclo di alimentazione), il parametro *Time* indica quando il dispositivo deve accendere di nuovo il dispositivo. Lo spegnimento è immediato.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 (zero) se ha esito positivo, 1 (uno) se la richiesta *PowerState* e *Time* specificata non è supportata e un altro valore se si sono verificati altri errori.

## <a name="remarks"></a>Commenti

Questo metodo non è attualmente implementato da WMI. Per usare questo metodo, è necessario implementarlo nel proprio provider.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe avere apportato modifiche per correggere gli errori secondari, rispettare gli standard di documentazione di Microsoft SDK o fornire altre informazioni.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[\_AGGREGATEPSEXTENT CIM](setpowerstate-method-in-class-cim-aggregatepsextent.md)
</dt> <dt>

[**\_AGGREGATEPSEXTENT CIM**](cim-aggregatepsextent.md)
</dt> </dl>

 

 




