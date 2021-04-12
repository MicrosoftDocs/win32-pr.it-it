---
description: Il metodo SetPowerState della classe CIM \_ NetworkAdapter imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato.
ms.assetid: b384bd64-c4a3-4a35-b18a-a4f23cd3d131
ms.tgt_platform: multiple
title: Metodo SetPowerState della classe CIM_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkAdapter.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a92777ebff1716c89a8f4c893a6ce99e78858e09
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483333"
---
# <a name="setpowerstate-method-of-the-cim_networkadapter-class"></a>Metodo SetPowerState della classe CIM \_ NetworkAdapter

Il metodo **SetPowerState** della classe CIM \_ NetworkAdapter imposta lo stato di alimentazione desiderato per un dispositivo logico e quando un dispositivo deve essere inserito in tale stato. In una sottoclasse, è necessario specificare il set di possibili codici restituiti utilizzando un qualificatore **ValueMap** nel metodo. Le stringhe a cui viene convertito il contenuto **ValueMap** devono essere specificate anche nella sottoclasse come qualificatore della matrice di **valori** . Questo metodo viene ereditato da [**\_ LogicalDevice CIM**](cim-logicaldevice.md).

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

Potenza piena.

</dd> <dt>

2
</dt> <dd>

Risparmio energia-modalità a basso consumo.

</dd> <dt>

3
</dt> <dd>

Risparmio energia standby.

</dd> <dt>

4
</dt> <dd>

Risparmio di energia.

</dd> <dt>

5
</dt> <dd>

Ciclo di alimentazione.

</dd> <dt>

6
</dt> <dd>

Spegnimento.

</dd> </dl> </dd> <dt>

*Ora* \[ di in\]
</dt> <dd>

Specifica quando deve essere impostato lo stato di alimentazione, come valore di data e ora normale o come valore di intervallo, in cui l'intervallo inizia quando viene ricevuta la chiamata al metodo. Quando il parametro *PowerState* è uguale a 5 ("ciclo di alimentazione"), il parametro *Time* indica quando riaccendere il dispositivo. Lo spegnimento è immediato.

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

[\_NETWORKADAPTER CIM](setpowerstate-method-in-class-cim-networkadapter.md)
</dt> <dt>

[**\_NETWORKADAPTER CIM**](cim-networkadapter.md)
</dt> </dl>

 

 




