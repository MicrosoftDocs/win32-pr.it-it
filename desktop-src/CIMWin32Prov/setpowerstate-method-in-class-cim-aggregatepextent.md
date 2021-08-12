---
description: 'Metodo SetPowerState della classe CIM_AggregatePExtent: il metodo SetPowerState imposta lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato.'
ms.assetid: 1a1a8d5e-d685-4b7e-99fb-61fa2e7bdafa
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_AggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregatePExtent.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 56d9f6c34ec1eb98d89c27eb0ebf90ad792f0237eb0b716d5ccb1d4ce2927c7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118675752"
---
# <a name="setpowerstate-method-of-the-cim_aggregatepextent-class"></a>Metodo SetPowerState della classe CIM \_ AggregatePExtent

Il **metodo SetPowerState** imposta lo stato di alimentazione desiderato per un dispositivo logico e quando il dispositivo deve essere inserito in tale stato. In una sottoclasse, il set di possibili codici restituiti deve essere specificato usando un **qualificatore ValueMap** nel metodo . Le stringhe in cui vengono **convertiti i contenuti di ValueMap** devono essere specificate anche nella sottoclasse come qualificatore di matrice **Values.** Questo metodo viene ereditato da [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

Per altre informazioni sull'uso di questo metodo con C/C++, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

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

Valore **valueMap** che specifica lo stato di alimentazione desiderato per questo dispositivo logico.

<dt>

1
</dt> <dd>

Alimentazione completa

</dd> <dt>

2
</dt> <dd>

Risparmio energia in modalità a basso consumo

</dd> <dt>

3
</dt> <dd>

Risparmio energia standby

</dd> <dt>

4
</dt> <dd>

Risparmio energia altro

</dd> <dt>

5
</dt> <dd>

Ciclo di alimentazione

</dd> <dt>

6
</dt> <dd>

Spegnimento

</dd> </dl> </dd> <dt>

*Ora* \[ Pollici\]
</dt> <dd>

Quando lo stato di alimentazione deve essere impostato, come valore di data e ora regolare o come valore di intervallo (in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo). Quando il *parametro PowerState* è uguale a 5 (ciclo di alimentazione), il parametro *Time* indica quando il dispositivo deve ripartire. L'accensione è immediata.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 (zero) se ha esito positivo, 1 (uno) se le richieste *PowerState* e *Time* specificate non sono supportate e un altro valore se si è verificato un altro errore.

## <a name="remarks"></a>Commenti

Questo metodo non è attualmente implementato da WMI. Per usare questo metodo, è necessario implementarlo nel proprio provider.

Questa documentazione è derivata dalle descrizioni della classe CIM pubblicate da DMTF. Microsoft potrebbe aver apportato modifiche per correggere gli errori minori, essere conforme agli standard della documentazione di Microsoft SDK o fornire altre informazioni.

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

[**CIM \_ AggregatePExtent**](setpowerstate-method-in-class-cim-aggregatepextent.md)
</dt> <dt>

[**CIM \_ AggregatePExtent**](cim-aggregatepextent.md)
</dt> </dl>

 

