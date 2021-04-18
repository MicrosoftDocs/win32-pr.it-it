---
title: Classe Win32_RDMSVirtualDesktopCollection
description: Crea e gestisce un insieme di desktop virtuali.
ms.assetid: fe0a484e-f9e3-4b99-8e69-da8f337ae957
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto
- Classe Win32_RDMSVirtualDesktopCollection Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection.Alias
- Win32_RDMSVirtualDesktopCollection.Type
- Win32_RDMSVirtualDesktopCollection.IsManaged
- Win32_RDMSVirtualDesktopCollection.Name
- Win32_RDMSVirtualDesktopCollection.CollectionDescription
- Win32_RDMSVirtualDesktopCollection.SecurityDescriptor
- Win32_RDMSVirtualDesktopCollection.VmFarmSettings
- Win32_RDMSVirtualDesktopCollection.UserVHDSetting
- Win32_RDMSVirtualDesktopCollection.IconContents
- Win32_RDMSVirtualDesktopCollection.ShowInPortal
- Win32_RDMSVirtualDesktopCollection.IsHA
- Win32_RDMSVirtualDesktopCollection.IsUserAdmin
- Win32_RDMSVirtualDesktopCollection.RollbackEnabled
api_location:
- RDMS.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a6da0c13b6ab223afc7afe6e92039a5388c6204
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301446"
---
# <a name="win32_rdmsvirtualdesktopcollection-class"></a>Win32 \_ RDMSVirtualDesktopCollection (classe)

Crea e gestisce un insieme di desktop virtuali.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_RDManagement_Prov"), AMENDMENT]
class Win32_RDMSVirtualDesktopCollection
{
  string  Alias;
  uint32  Type;
  boolean IsManaged;
  string  Name;
  string  CollectionDescription;
  string  SecurityDescriptor;
  string  VmFarmSettings;
  string  UserVHDSetting;
  uint8   IconContents[];
  boolean ShowInPortal;
  boolean IsHA;
  boolean IsUserAdmin;
  boolean RollbackEnabled;
};
```

## <a name="members"></a>Members

La classe **Win32 \_ RDMSVirtualDesktopCollection** presenta questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La classe **Win32 \_ RDMSVirtualDesktopCollection** presenta questi metodi.



| Metodo                                                                                            | Descrizione                                                                                                                                     |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddVirtualDesktop**](addvirtualdesktop-win32-rdmsvirtualdesktopcollection.md)                 | Aggiunge un desktop virtuale a un insieme di desktop virtuali.<br/>                                                                              |
| [**CancelPatch**](cancelpatch-win32-rdmsvirtualdesktopcollection.md)                             | Annulla un processo di provisioning degli aggiornamenti software per le macchine virtuali in un insieme di desktop virtuali.<br/>                                 |
| [**GetInt32Property**](getint32property-win32-rdmsvirtualdesktopcollection.md)                   | Recupera un valore di proprietà Integer da un insieme di desktop virtuali.<br/>                                                               |
| [**GetPatchProperties**](getpatchproperties-win32-rdmsvirtualdesktopcollection.md)               | Recupera le proprietà di un processo di provisioning degli aggiornamenti software per le macchine virtuali in un insieme di desktop virtuali.<br/>             |
| [**GetStringProperty**](getstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Recupera un valore della proprietà stringa da un insieme di desktop virtuali.<br/>                                                                 |
| [**ProvisioningEnumerateJobs**](provisioningenumeratejobs-win32-rdmsvirtualdesktopcollection.md) | Enumera i processi di provisioning del desktop virtuale per questo servizio.<br/>                                                                       |
| [**ProvisioningJobCancel**](provisioningjobcancel-win32-rdmsvirtualdesktopcollection.md)         | Annulla un processo di provisioning di un desktop virtuale.<br/>                                                                                          |
| [**ProvisioningJobExecute**](provisioningjobexecute-win32-rdmsvirtualdesktopcollection.md)       | Esegue un processo di provisioning di desktop virtuale.<br/>                                                                                             |
| [**ProvisioningJobGetReport**](provisioningjobgetreport-win32-rdmsvirtualdesktopcollection.md)   | Ottiene un report sullo stato di un processo di provisioning di un desktop virtuale.<br/>                                                                |
| [**ProvisioningPrepJob**](win32-rdmsvirtualdesktopcollection-provisioningprepjob.md)             | Consente di creare un processo di provisioning di desktop virtuale.<br/>                                                                                          |
| [**RemoveVirtualDesktop**](removevirtualdesktop-win32-rdmsvirtualdesktopcollection.md)           | Rimuove un desktop virtuale da un insieme di desktop virtuali.<br/>                                                                         |
| [**SchedulePatch**](schedulepatch-win32-rdmsvirtualdesktopcollection.md)                         | Pianifica un processo di provisioning degli aggiornamenti software che installa gli aggiornamenti software nelle macchine virtuali in un insieme di desktop virtuali.<br/> |
| [**SetInt32Property**](setint32property-win32-rdmsvirtualdesktopcollection.md)                   | Aggiorna un valore della proprietà Integer di un insieme di desktop virtuali.<br/>                                                                   |
| [**SetStringProperty**](setstringproperty-win32-rdmsvirtualdesktopcollection.md)                 | Aggiorna il valore della proprietà di una stringa di un insieme di desktop virtuali.<br/>                                                                     |



 

### <a name="properties"></a>Proprietà

La classe **Win32 \_ RDMSVirtualDesktopCollection** dispone di queste proprietà.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Ottiene o imposta l'alias della raccolta.

</dd> <dt>

**CollectionDescription**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ottiene o imposta la descrizione della raccolta.

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ottiene o imposta una matrice di valori che specificano le icone per la raccolta.

</dd> <dt>

**IsHA**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene o imposta un valore che indica se la raccolta contiene macchine virtuali a disponibilità elevata. **True** se la raccolta contiene macchine virtuali a disponibilità elevata; in caso contrario, **false**.

</dd> <dt>

**IsManaged**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene o imposta un valore che indica se l'insieme è gestito. **True** se l'insieme è gestito; in caso contrario, **false**.

</dd> <dt>

**IsUserAdmin**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene o imposta un valore che indica se un utente è un amministratore di una macchina virtuale. **True** se l'utente è un amministratore di una macchina virtuale. in caso contrario, **false**.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene o imposta il nome della raccolta.

</dd> <dt>

**RollbackEnabled**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene o imposta un valore che indica se è stato eseguito il rollback di una macchina virtuale con uno snapshot della macchina virtuale. **True** se è stato eseguito il rollback della macchina virtuale con uno snapshot della macchina virtuale. in caso contrario, **false**.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ottiene o imposta un descrittore di sicurezza in formato SSDL che controlla l'accesso alla raccolta.

</dd> <dt>

**ShowInPortal**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene o imposta un valore che indica se la raccolta viene visualizzata in Servizi terminal Accesso Web (Accesso Web TS). **True** per visualizzare la raccolta in accesso Web di Servizi terminal; in caso contrario, **false**.

</dd> <dt>

**Tipo**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Ottiene o imposta un valore che indica il tipo di sessioni della macchina virtuale ospitate dalla raccolta.

Questa proprietà contiene uno dei valori seguenti:

<dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>**TempVM** (1)


</dt> <dd>

Macchine virtuali temporanee.

</dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>**ManualPersonalVM** (2)


</dt> <dd>

Macchine virtuali create manualmente.

</dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>**AutoPersonalVM** (3)


</dt> <dd>

Macchine virtuali generate automaticamente.

</dd> </dl>

</dd> <dt>

**UserVHDSetting**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ottiene o imposta l'impostazione VHD dei dati utente per la raccolta.

</dd> <dt>

**VmFarmSettings**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Ottiene o imposta le impostazioni del desktop per le macchine virtuali nella raccolta.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                   |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                              |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ RDBMS<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Provider di Desktop remoto Management Services](rdms-api-reference.md)
</dt> </dl>

 

