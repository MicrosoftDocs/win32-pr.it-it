---
description: Il metodo Invoke della classe CIM \_ RemoveFileAction esegue una determinata azione. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione. Questo metodo viene ereditato dall'azione \_ CIM.
ms.assetid: 7fc33654-a51b-41cf-a5b4-ef08fd6e40ac
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_RemoveFileAction
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RemoveFileAction.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: b3d602207cefa1adbae416f59f10bd0d7a52e50495a559e36ead184888a4d0ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120064821"
---
# <a name="invoke-method-of-the-cim_removefileaction-class"></a>Metodo Invoke della classe CIM \_ RemoveFileAction

Il **metodo Invoke** della classe [**CIM \_ RemoveFileAction**](cim-removefileaction.md) esegue una determinata azione. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione. Questo metodo viene ereditato da [**CIM \_ Action**](cim-action.md).

> [!IMPORTANT]
> Le classi CIM (Distributed Management Task Force) DMTF (Common Information Model Distributed Management Task Force) sono le classi padre su cui vengono compilate le classi WMI. WMI attualmente supporta solo gli schemi [della versione CIM 2.x](https://dmtf.org/standards/cim/schemas).

 

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

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

[CIM \_ RemoveFileAction](invoke-method-in-class-cim-removefileaction.md)
</dt> <dt>

[**CIM \_ RemoveFileAction**](cim-removefileaction.md)
</dt> </dl>

 

