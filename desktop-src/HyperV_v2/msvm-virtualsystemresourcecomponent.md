---
description: Rappresenta un servizio dispositivo virtuale della piattaforma Microsoft Windows Hyper-V.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Msvm_VirtualSystemResourceComponent classe
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
ms.openlocfilehash: 0758858e9e45066cdfaddf36616c7861bbae914b12e3698665f8650c6c57d67c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340171"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a>Classe Msvm \_ VirtualSystemResourceComponent

Rappresenta un servizio dispositivo virtuale della piattaforma Microsoft Windows Hyper-V.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

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

La **classe Msvm \_ VirtualSystemResourceComponent** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VirtualSystemResourceComponent** ha queste proprietà.

<dl> <dt>

**AdditionalClassNames**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe contenente classi non di associazione aggiuntive estratte da questa **istanza di Msvm \_ VirtualSystemResourceComponent.** Queste classi non devono derivare né [**da CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) né [**da \_ CIM ResourceAllocationSettingData.**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata)

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID che rappresenta l'identificatore di classe dell'oggetto COM del servizio. Questa proprietà viene ereditata da [**Msvm \_ VirtualizationComponent.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**Contesto**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contesto in cui verrà eseguito l'oggetto appena creato. Questo valore viene passato nel *parametro dwClsContext* a [**CoCreateInstance.**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) Questa proprietà viene ereditata da [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su 1.

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se questa istanza è abilitata e può essere utilizzata per completare le richieste client. in caso contrario, **False.** Questa proprietà viene ereditata da [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)ed è sempre impostata su **True.**

</dd> <dt>

**HotAdd**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se questa istanza può essere aggiunta a caldo a una macchina virtuale. in caso contrario, **False.** Il valore predefinito è **False**.

</dd> <dt>

**HotRemove**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

**True** se questa istanza può essere rimossa a caldo da una macchina virtuale. in caso contrario, **False.** Il valore predefinito è **False**.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Stringa indipendente dalla lingua che identifica in modo univoco il servizio. Per evitare conflitti di denominazione, è consigliabile utilizzare il formato seguente: "versione \| del componente \| del fornitore". Ad esempio, questo nome rappresenta la versione 1.0 del componente porta di rete emulata Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| V1.0". Questa proprietà viene ereditata da [**Msvm \_ VirtualizationComponent.**](msvm-virtualizationcomponent.md)

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Relazione dell'oggetto WMI descritto qui con il dispositivo virtuale.



| Valore                                                                                                                                                                                                                                                           | Significato                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <dt>**"Non modificabile"**</dt> <dt>0</dt> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <dt>**"Singleton"**</dt> <dt>1</dt> </dl>                     | Singleton è un oggetto WMI di primo livello associato 1:1 a un dispositivo virtuale e può esistere solo una volta per ogni macchina virtuale. Si tratta del valore predefinito.<br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <dt>**"MultiInstance"**</dt> <dt>2</dt> </dl>     | MultiInstance è un oggetto WMI di primo livello che può esistere più volte per ogni macchina virtuale ed è associato 1:1 a un dispositivo virtuale.<br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <dt>**"Subdevice"**</dt> <dt>3</dt> </dl>                     | Subdevice è un oggetto WMI che non ha riferimenti padre, ma è controllato da un solo dispositivo virtuale che può esistere una sola volta per ogni macchina virtuale. L'oggetto WMI può tuttavia esistere più volte.<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Commenti

L'accesso alla **classe Msvm \_ VirtualSystemResourceComponent** potrebbe essere limitato dal filtro di Controllo dell'account utente. Per altre informazioni, vedere [Controllo dell'account utente e WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Fine del supporto client<br/>    | Windows 8.1<br/>                                                                                  |
| Fine del supporto server<br/>    | R2 per Windows Server 2012<br/>                                                                       |
| Spazio dei nomi<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Msvm \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

