---
description: Verifica se lo chassis fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.
ms.assetid: 9a1aa1b7-2b95-4887-9d14-e416ff69f9df
ms.tgt_platform: multiple
title: Metodo di compatibilità della classe CIM_Chassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 8796582b153a7283429715569eeed91e4dd38fc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106304666"
---
# <a name="iscompatible-method-of-the-cim_chassis-class"></a>Metodo di compatibilità della \_ classe chassis CIM

Il **Metodo IsValid verifica se lo chassis** fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico. In una sottoclasse è possibile specificare il set di possibili codici restituiti utilizzando un qualificatore [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) nel metodo. Le stringhe a cui viene convertito il contenuto **ValueMap** possono anche essere specificate nella sottoclasse come qualificatore della matrice di **valori** . Questo metodo viene ereditato da [**\_ PhysicalPackage CIM**](cim-physicalpackage.md).

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ElementToCheck* \[ in\]
</dt> <dd>

Riferimento all'elemento fisico per il quale verificare la compatibilità.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) in caso di esito positivo, 1 (uno) se la richiesta non è supportata e qualsiasi altro numero per indicare un errore.

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

[**\_Chassis CIM**](iscompatible-method-in-class-cim-chassis.md)
</dt> <dt>

[**\_Chassis CIM**](cim-chassis.md)
</dt> </dl>

 

