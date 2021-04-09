---
description: Il metodo Invoke della classe di \_ azione CIM esegue una determinata azione. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione.
ms.assetid: 4f0be560-bd78-4c7f-b6e3-ca86837a84f9
ms.tgt_platform: multiple
title: Metodo Invoke della classe CIM_Action
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Action.Invoke
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: e02e414fb05e0dd4ea97c3e3a4d87659fed4c963
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877585"
---
# <a name="invoke-method-of-the-cim_action-class"></a>Metodo Invoke della classe di \_ azione CIM

Il metodo **Invoke** della classe [**di \_ azione CIM**](cim-action.md) esegue una determinata azione. I dettagli del modo in cui il metodo esegue l'azione sono specifici dell'implementazione.

> [!IMPORTANT]
> Le classi CIM (Common Information Model) DMTF (Distributed Management Task Force) sono le classi padre sulle quali vengono compilate le classi WMI. Attualmente WMI supporta solo gli [schemi della versione CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 Invoke();
```



## <a name="parameters"></a>Parametri

Questo metodo non presenta parametri.

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) in caso di esito positivo, 1 (uno) se il metodo non è supportato e qualsiasi altro numero per indicare un errore.

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

[\_Azione CIM](invoke-method-in-class-cim-action.md)
</dt> <dt>

[**\_Azione CIM**](cim-action.md)
</dt> <dt>

[Classi CIM](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

