---
description: Fornisce i dati di impostazione per un disco rigido virtuale.
ms.assetid: 492a0b81-86b2-4d7d-a118-6ec14e3971ed
title: Msvm_VirtualHardDiskSettingData classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskSettingData
- Msvm_VirtualHardDiskSettingData.InstanceID
- Msvm_VirtualHardDiskSettingData.Caption
- Msvm_VirtualHardDiskSettingData.Description
- Msvm_VirtualHardDiskSettingData.ElementName
- Msvm_VirtualHardDiskSettingData.Type
- Msvm_VirtualHardDiskSettingData.Format
- Msvm_VirtualHardDiskSettingData.Path
- Msvm_VirtualHardDiskSettingData.ParentPath
- Msvm_VirtualHardDiskSettingData.ParentTimestamp
- Msvm_VirtualHardDiskSettingData.ParentIdentifier
- Msvm_VirtualHardDiskSettingData.MaxInternalSize
- Msvm_VirtualHardDiskSettingData.BlockSize
- Msvm_VirtualHardDiskSettingData.LogicalSectorSize
- Msvm_VirtualHardDiskSettingData.PhysicalSectorSize
- Msvm_VirtualHardDiskSettingData.VirtualDiskId
- Msvm_VirtualHardDiskSettingData.DataAlignment
- Msvm_VirtualHardDiskSettingData.PmemAddressAbstractionType
- Msvm_VirtualHardDiskSettingData.IsPmemCompatible
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: b7f87ba072aaff03ab415ccabe803546a89192ecb1e28d85b628dd0655d47421
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068421"
---
# <a name="msvm_virtualharddisksettingdata-class"></a>Classe Msvm \_ VirtualHardDiskSettingData

Fornisce i dati di impostazione per un disco rigido virtuale.

La sintassi seguente è Managed Object Format codice MOF e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskSettingData : CIM_SettingData
{
  string   InstanceID;
  string   Caption = "Virtual Hard Disk Setting Data";
  string   Description = "Setting Data for a Virtual Hard Disk";
  string   ElementName;
  uint16   Type;
  uint16   Format;
  string   Path;
  string   ParentPath;
  DATETIME ParentTimestamp;
  string   ParentIdentifier;
  uint64   MaxInternalSize;
  uint32   BlockSize;
  uint32   LogicalSectorSize;
  uint32   PhysicalSectorSize;
  string   VirtualDiskId;
  uint64   DataAlignment;
  uint16   PmemAddressAbstractionType;
  boolean  IsPmemCompatible;
};
```

## <a name="members"></a>Members

La **classe Msvm \_ VirtualHardDiskSettingData** include questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe Msvm \_ VirtualHardDiskSettingData** ha queste proprietà.

<dl> <dt>

**Blocksize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Dimensioni del blocco utilizzate dal disco rigido virtuale, in byte.

</dd> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Breve descrizione dell'oggetto. Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Virtual Hard Disk Setting Data".

</dd> <dt>

**DataAlignment**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica l'allineamento desiderato, in byte, per il payload dei dati del disco virtuale

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)ed è sempre impostata su "Setting Data for a Virtual Hard Disk" (Impostazione dei dati per un disco rigido virtuale).

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome visualizzato per l'oggetto . Questa proprietà viene ereditata da [**CIM \_ ManagedElement.**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)

</dd> <dt>

**Formato**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Formato del disco rigido virtuale. Si tratta di uno dei valori seguenti.

<dt>

<span id="VHD"></span><span id="vhd"></span>

<span id="VHD"></span><span id="vhd"></span>**Disco rigido virtuale** (2)


</dt> <dd></dd> <dt>

<span id="VHDX"></span><span id="vhdx"></span>

<span id="VHDX"></span><span id="vhdx"></span>**VHDX** (3)


</dt> <dd></dd> <dt>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>

<span id="VHDSet"></span><span id="vhdset"></span><span id="VHDSET"></span>**VHDSet** (4)


</dt> <dd>

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> </dl>

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: **Chiave**
</dt> </dl>

Identifica in modo univoco un'istanza di questa classe. Questa proprietà viene ereditata da [**CIM \_ SettingData.**](/previous-versions//cc136911(v=vs.85))

</dd> <dt>

**IsPmemCompatible**
</dt> <dd> <dl> <dt>

Tipo di dati: **booleano**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Specifica se il disco virtuale può essere usato come archivio di backup per un dispositivo con memoria persistente.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

</dd> <dt>

**LogicalSectorSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Dimensioni del settore logico utilizzate dal disco rigido virtuale, in byte.

</dd> <dt>

**MaxInternalSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint64**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Dimensioni massime del disco rigido virtuale come visualizzabili dalla macchina virtuale, in byte. Questa dimensione verrà arrotondata per es. al successivo multiplo più grande delle dimensioni del settore.

</dd> <dt>

**ParentIdentifier**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID utilizzato per identificare in modo univoco l'elemento padre del disco rigido virtuale. Se il disco rigido virtuale non ha un elemento padre, questo campo è vuoto.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

**ParentPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Elemento padre del disco rigido virtuale. Se il disco rigido virtuale non ha un elemento padre, questa proprietà è vuota.

</dd> <dt>

**ParentTimestamp**
</dt> <dd> <dl> <dt>

Tipo di dati: **DATETIME**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Timestamp dell'elemento padre del disco rigido virtuale. Se il disco rigido virtuale non ha un elemento padre, questo campo è vuoto.

> [!Note]  
> Aggiunta in Windows 10 e Windows Server 2016.

 

</dd> <dt>

**Percorso**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Percorso completo del disco rigido virtuale.

</dd> <dt>

**PhysicalSectorSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Dimensioni del settore fisico utilizzate dal disco rigido virtuale, in byte.

</dd> <dt>

**PmemAddressAbstractionType**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Metodo di astrazione dell'indirizzo di memoria persistente da usare con questo disco virtuale.

> [!Note]  
> Aggiunta in Windows 10, versione 1709.

 

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

**Nessuno** (0)


</dt> <dd></dd> <dt>

<span id="BTT"></span><span id="btt"></span>

**BTT** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Sconosciuto** (65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint16**
</dt> <dt>

Tipo di accesso: Lettura/scrittura
</dt> </dl>

Tipo di disco rigido virtuale. Questo sarà uno dei valori seguenti.

<dt>

<span id="Fixed"></span><span id="fixed"></span><span id="FIXED"></span>

**Risolto** (2)


</dt> <dd></dd> <dt>

<span id="Dynamic"></span><span id="dynamic"></span><span id="DYNAMIC"></span>

**Dinamico** (3)


</dt> <dd></dd> <dt>

<span id="Differencing"></span><span id="differencing"></span><span id="DIFFERENCING"></span>

**Differenze** (4)


</dt> <dd></dd> </dl>

</dd> <dt>

**VirtualDiskId**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

GUID usato per identificare in modo univoco il disco virtuale.

Quando il metodo [**Msvm \_ ImageManagementService.GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md) restituisce un'istanza di **Msvm \_ VirtualHardDiskSettingData,** il client può usare questa proprietà per ottenere l'ID disco univoco del disco rigido virtuale.

In caso di rilevamento dei conflitti o in caso contrario, un client può impostare il valore **VirtualDiskId** su un nuovo GUID e passare questa istanza **di Msvm \_ VirtualHardDiskSettingData** al metodo [**Msvm \_ ImageManagementService.SetVirtualHardDiskSettingData**](setvirtualharddisksettingdata-msvm-imagemanagementservice.md) per modificare l'ID disco del disco rigido virtuale. Se il disco rigido virtuale non è un disco rigido virtuale VHDX o se il disco rigido virtuale è collegato, l'operazione non riesce. L'operazione ha esito negativo anche se il formato del valore passato non è valido, cio' non è un GUID o ha tutti gli 0. L'operazione ha esito negativo se il valore passato è uguale all'ID disco corrente.

Gli errori generati dalla [**funzione SetVirtualDiskInformation**](/windows/win32/api/virtdisk/nf-virtdisk-setvirtualdiskinformation) vengono visualizzati tramite questa proprietà. Un client può anche usare lo stesso meccanismo per fornire il **valore VirtualDiskId** durante la creazione del disco rigido virtuale tramite il metodo [**Msvm \_ ImageManagementService.CreateVirtualHardDisk**](createvirtualharddisk-msvm-imagemanagementservice.md) nello stesso spazio dei nomi. Può essere usato per creare dischi rigidi virtuali VHD1 o VHD2.

**Windows 8.1:** Questo valore non è supportato fino a quando Windows 8.1 e Windows Server 2012 R2.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | \[Windows 8 solo app desktop\]<br/>                                                              |
| Server minimo supportato<br/> | \[Windows Server 2012 solo app desktop\]<br/>                                                    |
| Spazio dei nomi<br/>                | Virtualizzazione \\ radice \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**CIM \_ SettingData**](cim-settingdata.md)
</dt> <dt>

[**GetVirtualHardDiskSettingData**](getvirtualharddisksettingdata-msvm-imagemanagementservice.md)
</dt> </dl>

 

