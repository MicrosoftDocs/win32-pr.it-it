---
description: Verifica se il rack a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.
ms.assetid: 03276c6a-ca48-48bc-adbe-e53e02107abb
ms.tgt_platform: multiple
title: Metodo IsCompatible della classe CIM_Rack
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Rack.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3daf84cd47a89a53e808e73d4598c051b92e01197d4de18b43a5ce89ab9fb099
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064499"
---
# <a name="iscompatible-method-of-the-cim_rack-class"></a>Metodo IsCompatible della classe CIM \_ Rack

Il **metodo IsCompatible** verifica se il rack a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico. In una sottoclasse è possibile specificare il set di possibili codici restituiti usando un **qualificatore ValueMap** nel metodo . Le stringhe in cui vengono **convertiti i contenuti di ValueMap** possono essere specificate anche nella sottoclasse come qualificatore di matrice **Values.** Questo metodo viene ereditato da [**CIM \_ PhysicalPackage**](cim-physicalpackage.md).

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement ElementToCheck
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ElementToCheck* \[ Pollici\]
</dt> <dd>

Riferimento all'elemento fisico su cui viene eseguito questo metodo.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.

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

[**CIM \_ Rack**](iscompatible-method-in-class-cim-rack.md)
</dt> <dt>

[**CIM \_ Rack**](cim-rack.md)
</dt> </dl>

 

