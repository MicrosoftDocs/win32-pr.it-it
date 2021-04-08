---
description: Il metodo ResetCounter Reimposta i contatori di errore e di avviso.
ms.assetid: 5bc6c939-cd97-40ca-a16c-5227e7f27c76
ms.tgt_platform: multiple
title: Metodo ResetCounter della classe CIM_DeviceErrorCounts
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceErrorCounts.ResetCounter
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 386547362f5a7aa52bddfbf9df3af01949aecbdd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877350"
---
# <a name="resetcounter-method-of-the-cim_deviceerrorcounts-class"></a>Metodo ResetCounter della classe CIM \_ DeviceErrorCounts

Il metodo **ResetCounter** Reimposta i contatori di errore e di avviso. Viene usato un metodo in modo che la strumentazione del dispositivo logico, che cataloga gli errori e gli avvisi, possa anche reimpostare i contatori e l'elaborazione interna. In una sottoclasse, il set di possibili codici restituiti può essere specificato utilizzando un qualificatore **ValueMap** nel metodo. Le stringhe a cui viene convertito il contenuto **ValueMap** possono anche essere specificate nella sottoclasse come qualificatore della matrice di **valori** .

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 ResetCounter(
  [in] uint16 SelectedCounter
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*SelectedCounter* \[ in\]
</dt> <dd>

Contatore degli errori da ripristinare.

<dt>

<span id="All"></span><span id="all"></span><span id="ALL"></span>

**Tutto** (0)


</dt> <dd></dd> <dt>

<span id="Indeterminate_Error_Counter"></span><span id="indeterminate_error_counter"></span><span id="INDETERMINATE_ERROR_COUNTER"></span>

**Contatore errori indeterminato** (1)


</dt> <dd></dd> <dt>

<span id="Critical_Error_Counter"></span><span id="critical_error_counter"></span><span id="CRITICAL_ERROR_COUNTER"></span>

**Contatore errore critico** (2)


</dt> <dd></dd> <dt>

<span id="Major_Error_Counter"></span><span id="major_error_counter"></span><span id="MAJOR_ERROR_COUNTER"></span>

**Contatore errore principale** (3)


</dt> <dd></dd> <dt>

<span id="Minor_Error_Counter"></span><span id="minor_error_counter"></span><span id="MINOR_ERROR_COUNTER"></span>

**Contatore errori secondari** (4)


</dt> <dd></dd> <dt>

<span id="Warning_Counter"></span><span id="warning_counter"></span><span id="WARNING_COUNTER"></span>

**Contatore avvisi** (5)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce 0 (zero) se ha esito positivo, 1 (uno) se non è supportato e qualsiasi altro valore se si è verificato un errore.

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

[\_DEVICEERRORCOUNTS CIM](resetcounter-method-in-class-cim-deviceerrorcounts.md)
</dt> <dt>

[**\_DEVICEERRORCOUNTS CIM**](cim-deviceerrorcounts.md)
</dt> </dl>

 

