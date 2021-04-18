---
title: Classe Win32_TSVirtualIPSetting
description: Rappresenta l'associazione tra una \_ classe di elementi Win32 TerminalService e una \_ classe di impostazioni TSVirtualIP Win32.
ms.assetid: 06a78b4d-973a-4912-b7e6-bc490197c4a6
ms.tgt_platform: multiple
keywords:
- Classe Win32_TSVirtualIPSetting Servizi Desktop remoto
- Classe Win32_TSVirtualIPSetting Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_TSVirtualIPSetting
- Win32_TSVirtualIPSetting.Caption
- Win32_TSVirtualIPSetting.Description
- Win32_TSVirtualIPSetting.InstallDate
- Win32_TSVirtualIPSetting.Name
- Win32_TSVirtualIPSetting.Status
- Win32_TSVirtualIPSetting.Element
- Win32_TSVirtualIPSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7368b3b2e932f45d047d4ca4db724030b2dd82ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301054"
---
# <a name="win32_tsvirtualipsetting-class"></a>Win32 \_ TSVirtualIPSetting (classe)

Rappresenta l'associazione tra una classe di elementi [**Win32 \_ TerminalService**](win32-terminalservice.md) e una classe di impostazioni [**\_ TSVirtualIP Win32**](win32-tsvirtualip.md) .

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[Dynamic, Provider("Win32_WIN32_TSVIRTUALIPSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIPSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_TerminalService REF Element;
  Win32_TSVirtualIP     REF Setting;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ TSVirtualIPSetting** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ TSVirtualIPSetting** dispone di queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione (stringa a una riga) dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**elemento**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Win32 \_ TerminalService**](win32-terminalservice.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Riferimento a un oggetto [**Win32 \_ TerminalService**](win32-terminalservice.md) che rappresenta la classe di elementi per l'associazione.

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **DateTime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")
</dt> </dl>

Data di installazione dell'oggetto. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

</dd> <dt>

**Impostazione**
</dt> <dd> <dl> <dt>

Tipo di dati: **[ **Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Riferimento a un oggetto [**Win32 \_ TSVirtualIP**](win32-tsvirtualip.md) che rappresenta la classe Setting per l'associazione.

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire diversi stati operativi e non operativi. Gli stati operativi includono: "OK", "degradato" e "errore Predator" (un elemento, ad esempio un'unità disco rigido abilitata per SMART, potrebbe funzionare correttamente, ma prevedere un errore nel prossimo futuro). Gli Stati non operativi includono: "Error", "starting", "stoping" e "Service". Il secondo "servizio" può essere applicato durante il mirroring di un disco, il ricaricamento di un elenco di autorizzazioni utente o altre attività amministrative. Non tutto questo lavoro è online, ma l'elemento gestito non è né "OK" né in uno degli altri Stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Errore")


</dt> <dd></dd> <dt>



 ("Danneggiato")


</dt> <dd></dd> <dt>



 ("Sconosciuto")


</dt> <dd></dd> <dt>



 ("Errore di predazione")


</dt> <dd></dd> <dt>



 ("Avvio")


</dt> <dd></dd> <dt>



 ("Arresto")


</dt> <dd></dd> <dt>



 ("Servizio")


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                               |
| Server minimo supportato<br/> | Windows Server 2008 R2<br/>                                                       |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_ELEMENTSETTING CIM**](cim-elementsetting.md)
</dt> <dt>

[**\_TerminalService Win32**](win32-terminalservice.md)
</dt> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

