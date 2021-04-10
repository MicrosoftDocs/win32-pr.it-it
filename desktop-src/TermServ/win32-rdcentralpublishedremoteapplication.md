---
title: Classe Win32_RDCentralPublishedRemoteApplication
description: Descrive un'applicazione pubblicata in un altro computer per l'utilizzo remoto tramite Servizi terminal.
ms.assetid: 8605bd1e-e825-4fd9-b14f-9d3bdac489f1
ms.tgt_platform: multiple
keywords:
- Classe Win32_RDCentralPublishedRemoteApplication Servizi Desktop remoto
- Classe Win32_RDCentralPublishedRemoteApplication Servizi Desktop remoto, descritta
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteApplication
- Win32_RDCentralPublishedRemoteApplication.Caption
- Win32_RDCentralPublishedRemoteApplication.Description
- Win32_RDCentralPublishedRemoteApplication.InstallDate
- Win32_RDCentralPublishedRemoteApplication.Name
- Win32_RDCentralPublishedRemoteApplication.Status
- Win32_RDCentralPublishedRemoteApplication.PublishingFarm
- Win32_RDCentralPublishedRemoteApplication.Alias
- Win32_RDCentralPublishedRemoteApplication.SecurityDescriptor
- Win32_RDCentralPublishedRemoteApplication.Path
- Win32_RDCentralPublishedRemoteApplication.VPath
- Win32_RDCentralPublishedRemoteApplication.IconContents
- Win32_RDCentralPublishedRemoteApplication.CommandLineSetting
- Win32_RDCentralPublishedRemoteApplication.RequiredCommandLine
- Win32_RDCentralPublishedRemoteApplication.ShowInPortal
- Win32_RDCentralPublishedRemoteApplication.AppID
- Win32_RDCentralPublishedRemoteApplication.RDPFileContents
- Win32_RDCentralPublishedRemoteApplication.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd837f62d8d0787d992e8eed7316ed1ef3f199ae
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "103964084"
---
# <a name="win32_rdcentralpublishedremoteapplication-class"></a>Win32 \_ RDCentralPublishedRemoteApplication (classe)

Descrive un'applicazione pubblicata in un altro computer per l'utilizzo remoto tramite Servizi terminal.

La sintassi seguente è semplificata dal codice MOF (Managed Object Format) e include tutte le proprietà ereditate.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteApplication : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  string   SecurityDescriptor;
  string   Path;
  string   VPath;
  uint8    IconContents[];
  uint32   CommandLineSetting;
  string   RequiredCommandLine;
  boolean  ShowInPortal;
  string   AppID;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a>Members

La classe **Win32 \_ RDCentralPublishedRemoteApplication** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe **Win32 \_ RDCentralPublishedRemoteApplication** dispone di queste proprietà.

<dl> <dt>

**Alias**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Alias dell'applicazione.

</dd> <dt>

**AppID**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

AppID viene usato per l'aggiunta nei client.

</dd> <dt>

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

**CommandLineSetting**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Indica se sono necessari argomenti della riga di comando per questa applicazione.

<dt>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>

<span id="DoNotAllow"></span><span id="donotallow"></span><span id="DONOTALLOW"></span>**DoNotAllow** (0)


</dt> <dd>

Non consentire

</dd> <dt>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>

<span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Consenti** (1)


</dt> <dd></dd> <dt>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>

<span id="Require"></span><span id="require"></span><span id="REQUIRE"></span>**Richiedi** (2)


</dt> <dd></dd> </dl>

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

**Cartelle**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice di **stringhe**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Elenco delle cartelle in cui deve essere visualizzata la risorsa.

</dd> <dt>

**IconContents**
</dt> <dd> <dl> <dt>

Tipo di dati: matrice **Uint8**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Contenuto dell'icona corrispondente all'applicazione.

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

**Percorso**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Percorso dell'applicazione

</dd> <dt>

**PublishingFarm**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **chiave**](/windows/desktop/WmiSdk/key-qualifier)
</dt> </dl>

Alias della farm che ha pubblicato l'applicazione

</dd> <dt>

**RDPFileContents**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Contenuto del file RDP corrispondente all'applicazione.

</dd> <dt>

**RequiredCommandLine**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Argomenti della riga di comando necessari per questa applicazione.

</dd> <dt>

**SecurityDescriptor**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> <dt>

Qualificatori: [ **facoltativo**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)
</dt> </dl>

Descrittore di sicurezza che controlla l'accesso all'applicazione in formato SDDL. La stringa vuota implica l'autorizzazione All Access.

</dd> <dt>

**ShowInPortal**
</dt> <dd> <dl> <dt>

Tipo di dati: **Boolean**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

**true** se l'applicazione deve essere visualizzata nel accesso Web di Servizi terminal; in caso contrario, **false**.

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

</dd> <dt>

**VPath**
</dt> <dd> <dl> <dt>

Tipo di dati: **String**
</dt> <dt>

Tipo di accesso: lettura/scrittura
</dt> </dl>

Percorso virtuale dell'applicazione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Nessuno supportato<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2012<br/>                                                           |
| Spazio dei nomi<br/>                | Radice \\ CIMV2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>Tscpub. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TscPubWmi.dll</dt> </dl> |



 

