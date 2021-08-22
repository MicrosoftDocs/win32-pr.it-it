---
description: Rappresenta un servizio della piattaforma Microsoft Windows Hyper-V.
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Msvm_VirtualizationComponent classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ab2d2d5652f2969ad20ee70077d23375371e3507991a16b6d5e6dda2245678ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068431"
---
# <a name="msvm_virtualizationcomponent-class"></a>Classe Msvm \_ VirtualizationComponent

Rappresenta un servizio della piattaforma Microsoft Windows Hyper-V.

La sintassi seguente è semplificata Managed Object Format (MOF).

## <a name="syntax"></a>Sintassi

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ VirtualizationComponent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VirtualizationComponent** ha queste proprietà.

<dl> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID **che** rappresenta l'identificatore di classe dell'oggetto COM del servizio.

</dd> <dt>

**Contesto**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **sperimentale**
</dt> </dl>

Contesto in cui verrà eseguito l'oggetto appena creato. Questo valore viene passato nel *parametro dwClsContext* a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Questa proprietà è sempre impostata su 1.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se questa istanza è abilitata e può essere usata per completare le richieste client. in caso contrario, **False**. Questa proprietà è sempre impostata su **True.**

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Stringa indipendente dalla lingua che identifica in modo univoco il servizio. Per evitare conflitti di denominazione, è consigliabile il formato seguente: "versione \| del componente \| del fornitore". Ad esempio, questo nome rappresenta la versione 1.0 del componente porta di rete emulata Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| V1.0".

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ VirtualizationComponent** potrebbe essere limitato dal filtro del controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Fine del supporto client<br/>    | Windows 8.1<br/>                                                                                  |
| Fine del supporto server<br/>    | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

