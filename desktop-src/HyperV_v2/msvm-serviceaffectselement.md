---
description: Associa un'istanza di macchina virtuale al servizio di gestione che ne controlla lo stato.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Classe Msvm_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129999"
---
# <a name="msvm_serviceaffectselement-class"></a>\_Classe MSVM ServiceAffectsElement

Associa un'istanza di macchina virtuale al servizio di gestione che ne controlla lo stato.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a>Members

La **classe \_ ServiceAffectsElement di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ ServiceAffectsElement di MSVM** dispone di queste proprietà.

<dl> <dt>

**Interessato**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **CIM \_ Managed**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento alla macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**AffectingElement**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **\_ servizio CIM**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Riferimento al servizio che controlla la macchina virtuale. Questa proprietà viene ereditata da [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).

</dd> <dt>

**ElementEffects**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Specifica il tipo di controllo rappresentato dall'associazione. Questa proprietà viene ereditata da [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))ed è sempre impostata sul valore seguente.



| Valore                                                                        | Significato            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <dt>5</dt> </dl> | Gestisce<br/> |



 

</dd> <dt>

**OtherElementEffectsDescriptions**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Dettagli per il tipo di associazione nella posizione della matrice corrispondente nella matrice di proprietà **ElementAffects** . Queste informazioni sono obbligatorie se **ElementAffects** è impostato su 1 (other). Questa proprietà viene ereditata da [**CIM \_ ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))ed è sempre impostata su **null**.

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ ServiceAffectsElement di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_SERVICEAFFECTSELEMENT CIM**](cim-serviceaffectselement.md)
</dt> <dt>

[**\_SERVICEAFFECTSELEMENT CIM**](/previous-versions//cc136907(v=vs.85))
</dt> </dl>

 

