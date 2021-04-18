---
description: Rappresenta un servizio di dispositivo virtuale della piattaforma Microsoft Windows Hyper-V.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Classe Msvm_VirtualSystemResourceComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81c2d31a6497325ac77003ded266333518de890a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305986"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a>\_Classe MSVM VirtualSystemResourceComponent

Rappresenta un servizio di dispositivo virtuale della piattaforma Microsoft Windows Hyper-V.

La sintassi seguente è semplificata Managed Object Format codice (MOF) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a>Members

La **classe \_ VirtualSystemResourceComponent di MSVM** dispone di questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe \_ VirtualSystemResourceComponent di MSVM** dispone di queste proprietà.

<dl> <dt>

**AdditionalClassNames**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe contenente classi non di associazione aggiuntive emerse da questa istanza di **MSVM \_ VirtualSystemResourceComponent** . Queste classi devono derivare da né [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) né [**CIM \_ ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).

</dd> <dt>

**CLSID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID che rappresenta l'identificatore di classe dell'oggetto COM del servizio. Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Contesto**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contesto in cui viene eseguito l'oggetto appena creato. Questo valore viene passato al parametro *dwClsContext* a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance). Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su 1.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se questa istanza è abilitata e può essere utilizzata per completare le richieste del client. in caso contrario, **false**. Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su **true**.

</dd> <dt>

**HotAdd**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se questa istanza può essere aggiunta a caldo a una macchina virtuale. in caso contrario, **false**. Il valore predefinito è **False**.

</dd> <dt>

**HotRemove**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se questa istanza può essere rimossa a caldo da una macchina virtuale. in caso contrario, **false**. Il valore predefinito è **False**.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **chiave**
</dt> </dl>

Stringa indipendente dal linguaggio che identifica in modo univoco il servizio. Per evitare conflitti di denominazione, è consigliabile il formato seguente: \| " \| versione componente fornitore". Questo nome rappresenta ad esempio la versione 1,0 del componente della porta di rete emulata Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0". Questa proprietà viene ereditata da [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

La relazione dell'oggetto WMI descritta qui con il dispositivo virtuale.



| Valore                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <dt>**"Non modificabile"**</dt> <dt>0</dt> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <dt>**"Singleton"**</dt> <dt>1</dt> </dl>                     | Singleton è un oggetto WMI di primo livello associato a 1:1 con un dispositivo virtuale che può esistere solo una volta per ogni macchina virtuale. Si tratta del valore predefinito.<br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <dt>**"Multiistanza"**</dt> <dt>2</dt> </dl>     | Multi-instance è un oggetto WMI di primo livello che può esistere più volte per macchina virtuale ed è associato a 1:1 con un dispositivo virtuale.<br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <dt>**"Sottodispositivo"**</dt> <dt>3</dt> </dl>                     | Il sottodispositivo è un oggetto WMI che non contiene riferimenti padre ma è controllato da un solo dispositivo virtuale che può esistere una sola volta per ogni macchina virtuale. L'oggetto WMI può tuttavia esistere più volte.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe \_ VirtualSystemResourceComponent di MSVM** potrebbe essere limitato dal filtraggio del controllo dell'account utente. Per ulteriori informazioni, vedere [controllo dell'account utente e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows 8\]<br/>                                                              |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2012\]<br/>                                                    |
| Fine del supporto client<br/>    | Windows 8.1<br/>                                                                                  |
| Fine del supporto server<br/>    | Windows Server 2012 R2<br/>                                                                       |
| Spazio dei nomi<br/>                | \\Virtualizzazione radice \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_VirtualizationComponent MSVM**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**\_VirtualizationComponent MSVM**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

