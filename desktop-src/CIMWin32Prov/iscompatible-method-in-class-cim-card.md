---
description: Il metodo IsCompatible verifica se l'elemento fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico.
ms.assetid: 809a1871-dfa2-499b-9adf-118dec71586b
ms.tgt_platform: multiple
title: Metodo IsCompatible della CIM_Card classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Card.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 84fb7bb4c6ae3f5f562bc0a51d4a2a8ee4852fcb19a820b35e073d389366b133
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064701"
---
# <a name="iscompatible-method-of-the-cim_card-class"></a>Metodo IsCompatible della classe CARD \_ CIM

Il **metodo IsCompatible** verifica se l'elemento fisico a cui si fa riferimento può essere contenuto o inserito nel pacchetto fisico. In una sottoclasse è possibile specificare il set di codici restituiti possibili usando un **qualificatore ValueMap** nel metodo . Le stringhe in cui viene convertito **il contenuto di ValueMap** possono essere specificate anche nella sottoclasse come **qualificatore di** matrice Values. Questo metodo viene ereditato da [**CIM \_ PhysicalPackage.**](cim-physicalpackage.md)

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Distributed Management Task Force) Common Information Model sono le classi padre su cui vengono compilate le classi WMI. WMI supporta attualmente solo gli [schemi della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*ElementToCheck* \[ Pollici\]
</dt> <dd>

Riferimento all'elemento fisico su cui viene eseguito il metodo **IsCompatible.**

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) in caso di esito positivo e qualsiasi altro numero per indicare un errore.

## <a name="remarks"></a>Commenti

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

[Scheda \_ CIM](iscompatible-method-in-class-cim-card.md)
</dt> <dt>

[**Scheda \_ CIM**](cim-card.md)
</dt> </dl>

 

