---
title: Win32_TSNetworkAdapterSetting classe
description: Definisce varie impostazioni di configurazione per la classe Terminale Win32, incluse le proprietà correlate alla scheda di rete e il numero \_ massimo di connessioni consentite.
ms.assetid: b8a757e6-801b-4349-902e-76596b06df1f
ms.tgt_platform: multiple
keywords:
- Win32_TSNetworkAdapterSetting classe Servizi Desktop remoto
- Win32_TSNetworkAdapterSetting classe Servizi Desktop remoto , descritto
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting.Caption
- Win32_TSNetworkAdapterSetting.Description
- Win32_TSNetworkAdapterSetting.InstallDate
- Win32_TSNetworkAdapterSetting.Name
- Win32_TSNetworkAdapterSetting.Status
- Win32_TSNetworkAdapterSetting.TerminalName
- Win32_TSNetworkAdapterSetting.DeviceIDList
- Win32_TSNetworkAdapterSetting.MaximumConnections
- Win32_TSNetworkAdapterSetting.NetworkAdapterID
- Win32_TSNetworkAdapterSetting.NetworkAdapterLanaID
- Win32_TSNetworkAdapterSetting.NetworkAdapterList
- Win32_TSNetworkAdapterSetting.NetworkAdapterName
- Win32_TSNetworkAdapterSetting.PolicySourceMaximumConnections
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9bddc43fc651b8107d56b63876b251f7973c6a11ecbdbbd5ee22e6dfec4338f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348546"
---
# <a name="win32_tsnetworkadaptersetting-class"></a>Classe \_ TSNetworkAdapterSetting Win32

La **classe WMI Win32 \_ TSNetworkAdapterSetting** definisce varie impostazioni di configurazione per la classe [**\_ terminale Win32,**](win32-terminal.md) incluse le proprietà correlate alla scheda di rete e il numero massimo di connessioni consentite.

La sintassi seguente è semplificata dal codice MOF e include tutte le proprietà definite ed ereditate, in ordine alfabetico. Per informazioni di riferimento sui metodi, vedere la tabella dei metodi più avanti in questo argomento.

## <a name="syntax"></a>Sintassi

``` syntax
[dynamic, provider("Win32_WIN32_TSNETWORKADAPTERSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\WinStations"), AMENDMENT]
class Win32_TSNetworkAdapterSetting : Win32_TerminalSetting
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   TerminalName;
  string   DeviceIDList[];
  uint32   MaximumConnections;
  string   NetworkAdapterID;
  uint32   NetworkAdapterLanaID;
  string   NetworkAdapterList[];
  string   NetworkAdapterName;
  uint32   PolicySourceMaximumConnections;
};
```

## <a name="members"></a>Members

La **classe Win32 \_ TSNetworkAdapterSetting** ha questi tipi di membri:

-   [Metodi](#methods)
-   [Proprietà](#properties)

### <a name="methods"></a>Metodi

La **classe Win32 \_ TSNetworkAdapterSetting** include questi metodi.



| Metodo                                                                                     | Descrizione                                                                                              |
|:-------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------|
| [**SelectAllNetworkAdapters**](win32-tsnetworkadaptersetting-selectallnetworkadapters.md) | Seleziona tutte le schede di rete.<br/>                                                                 |
| [**SelectNetworkAdapterIP**](win32-tsnetworkadaptersetting-selectnetworkadapterip.md)     | Seleziona una scheda di rete in base all'indirizzo IP della scheda.<br/>                                  |
| [**SetNetworkAdapterLanaID**](setnetworkadapterlanaid-win32-tsnetworkadaptersetting.md)   | Specifica il numero NETBIOS della scheda di rete locale (LANA) da impostare.<br/> |



 

### <a name="properties"></a>Proprietà

La **classe Win32 \_ TSNetworkAdapterSetting** ha queste proprietà.

<dl> <dt>

**Didascalia**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)
</dt> </dl>

Breve descrizione (stringa di una riga) dell'oggetto .

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**Descrizione**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**DeviceIDList**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe di ID dispositivo disponibili restituiti nell'ordine delle schede di rete fisiche restituite nella matrice di proprietà **NetworkAdapterList.** Il valore dell'ID dispositivo è la **proprietà DeviceID** in [**\_ NetworkAdapter Win32**](/windows/desktop/CIMWin32Prov/win32-networkadapter)

</dd> <dt>

**InstallDate**
</dt> <dd> <dl> <dt>

Tipo di dati: **datetime**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001.5")
</dt> </dl>

Data di installazione dell'oggetto. La mancanza di un valore non indica che l'oggetto non è installato.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**MaximumConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: Lettura/Scrittura
</dt> </dl>

Numero massimo di connessioni consentite. Il valore **MAXINT** indica un numero illimitato di connessioni.

</dd> <dt>

**Nome**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome dell'oggetto.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

</dd> <dt>

**NetworkAdapterID**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

GUID che rappresenta l'ID della scheda di rete da impostare. Un **GUID** costituito da tutti gli zeri indica tutte le schede di rete.

</dd> <dt>

**NetworkAdapterLanaID**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Numero della scheda di rete LANA (Local Area Network Adapter) NetBIOS utilizzata per identificare la scheda di rete assegnata al terminale.

</dd> <dt>

**NetworkAdapterList**
</dt> <dd> <dl> <dt>

Tipo di dati: **matrice di** stringhe
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Matrice di stringhe delle schede di rete fisiche disponibili e degli ID dispositivo corrispondenti. Gli ID dispositivo sono la **proprietà DeviceID** in [**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter).

</dd> <dt>

**NetworkAdapterName**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Descrizione della scheda di rete da impostare. Questo valore si trova in [**Win32 \_ NetworkAdapterConfiguration.**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)

</dd> <dt>

**PolicySourceMaximumConnections**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Indica se la **proprietà MaximumConnections** è configurata dal server, dai criteri di gruppo o per impostazione predefinita.

<dt>

0
</dt> <dd>

Server

</dd> <dt>

1
</dt> <dd>

Criteri di gruppo

</dd> <dt>

2
</dt> <dd>

Predefinito

</dd> </dl>

</dd> <dt>

**Status**
</dt> <dd> <dl> <dt>

Tipo di dati: **stringa**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)
</dt> </dl>

Stato corrente dell'oggetto. È possibile definire vari stati operativi e non operativi. Gli stati operativi includono: "OK", "Degraded" e "Pred Fail" (un elemento, ad esempio un disco rigido abilitato per SMART, potrebbe funzionare correttamente ma prevedere un errore nel prossimo futuro). Gli stati non di operazione includono: "Error", "Starting", "Stopping" e "Service". Quest'ultimo, "Servizio", può essere applicato durante il ridimensionamento del mirror di un disco, il ricaricamento di un elenco di autorizzazioni utente o altro lavoro amministrativo. Non tutte queste operazioni sono in linea, ma l'elemento gestito non è né "OK" né in uno degli altri stati.

Questa proprietà viene ereditata da [**CIM \_ ManagedSystemElement.**](cim-managedsystemelement.md)

<dt>



 ("OK")


</dt> <dd></dd> <dt>



 ("Error")


</dt> <dd></dd> <dt>



 ("Danneggiato")


</dt> <dd></dd> <dt>



 ("Sconosciuto")


</dt> <dd></dd> <dt>



 ("Pred Fail")


</dt> <dd></dd> <dt>



 ("Starting")


</dt> <dd></dd> <dt>



 ("Arresto")


</dt> <dd></dd> <dt>



 ("Servizio")


</dt> <dd></dd> </dl>

</dd> <dt>

**TerminalName**
</dt> <dd> <dl> <dt>

Tipo di dati: **string**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> </dl>

Nome del terminale.

Questa proprietà viene ereditata da [**\_ TerminalSetting Win32.**](win32-terminalsetting.md)

</dd> </dl>

## <a name="remarks"></a>Commenti

Tenere presente che le winstation associate alla sessione della console non possono accedere ai metodi e alle proprietà di questa classe. Se si tenta di eseguire questa operazione specificando "Console" come valore della proprietà TerminalName, i metodi di questo oggetto restituiscono **WBEM \_ E \_ NOT \_ SUPPORTED.** Questo codice di errore viene restituito anche se una stazione finestra tenta di chiamare i metodi di questo oggetto per aggiungere o modificare le proprietà di sicurezza degli account LocalSystem, LocalService o NetworkService.

Per connettersi allo spazio dei nomi "Root \\ CIMV2 \\ TerminalServices", il livello di autenticazione deve includere la privacy dei pacchetti. Per le chiamate C/C++, questo è un livello di autenticazione di **RPC \_ C \_ AUTHN \_ LEVEL \_ PKT \_ PRIVACY**. Per Visual Basic e le chiamate di scripting, si tratta di un livello di autenticazione **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con valore 6. Nell'esempio Visual Basic Scripting Edition (VBScript) seguente viene illustrato come connettersi a un computer remoto con privacy dei pacchetti.


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



Managed Object Format (MOF) contengono le definizioni per Windows di Strumentazione gestione Windows (WMI). I file MOF non vengono installati come parte di Microsoft Windows Software Development Kit (SDK). Vengono installati nel server quando si aggiunge il ruolo associato usando il Server Manager. Per altre informazioni sui file MOF, vedere [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | Radice \\ CIMv2 \\ TerminalServices<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ NetworkAdapter**](/windows/desktop/CIMWin32Prov/win32-networkadapter)
</dt> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](/windows/desktop/CIMWin32Prov/win32-networkadapterconfiguration)
</dt> <dt>

[**Win32 \_ TerminalSetting**](win32-terminalsetting.md)
</dt> <dt>

[**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md)
</dt> </dl>

 

