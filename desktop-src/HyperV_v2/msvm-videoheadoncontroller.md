---
description: Associa un'head video al controller video che lo include.
ms.assetid: D072DF7C-D55B-4203-9FE5-B395D1EC1632
title: Msvm_VideoHeadOnController classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VideoHeadOnController
- Msvm_VideoHeadOnController.Antecedent
- Msvm_VideoHeadOnController.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a184f8d07be87839ef6a4d438b87953128d16d5c91b9c5e461b11e3b1312c28c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068441"
---
# <a name="msvm_videoheadoncontroller-class"></a>Classe Msvm \_ VideoHeadOnController

Associa un'head video al controller video che lo include.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VideoHeadOnController : CIM_VideoHeadOnController
{
  CIM_DisplayController REF Antecedent;
  Msvm_VideoHead        REF Dependent;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ VideoHeadOnController** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VideoHeadOnController** ha queste proprietà.

<dl> <dt>

**Antecedente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ DisplayController**](/previous-versions//cc136810(v=vs.85))**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Controller video che include l'head.

</dd> <dt>

**Dipendente**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Msvm \_ VideoHead**](msvm-videohead.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)
</dt> </dl>

Testa del dispositivo video.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ VideoHeadOnController** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ VideoHeadOnController**](cim-videoheadoncontroller.md)
</dt> <dt>

[**CIM \_ VideoHeadOnController**](/previous-versions//cc136950(v=vs.85))
</dt> <dt>

[Classi video](video-classes.md)
</dt> </dl>

 

