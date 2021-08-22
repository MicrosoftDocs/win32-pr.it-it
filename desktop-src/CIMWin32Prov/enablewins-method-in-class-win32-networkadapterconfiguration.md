---
description: EnableWINS &\# 32; Il metodo statico della classe WMI Windows impostazioni wins (Internet Naming Service) specifiche di TCP/IP, ma indipendenti dalla scheda di rete.
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Metodo EnableWINS della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1ce820e515bb72cbd2521521726f2b6962c49ee1b453781b5d17993c45e0d22d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118676504"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a>Metodo EnableWINS della classe NetworkAdapterConfiguration Win32 \_

Il metodo statico della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableWINS** consente Windows impostazioni wins (Internet Naming Service) specifiche per TCP/IP, ma indipendenti dalla scheda di rete.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DNSEnabledForWINSResolution* \[ Pollici\]
</dt> <dd>

Se **true,** il Domain Name System (DNS) è abilitato per la risoluzione dei nomi sulla risoluzione WINS.

</dd> <dt>

*WINSEnableLMHostsLookup* \[ Pollici\]
</dt> <dd>

Se **true,** vengono usati i file di ricerca locale. I file di ricerca conterranno i mapping degli indirizzi IP ai nomi host.

</dd> <dt>

*WINSHostLookupFile* \[ in, facoltativo\]
</dt> <dd>

Ricerca di file che contengono mapping di indirizzi IP a nomi host. Se disponibili, i file si trovano in %SystemRoot% \\ driver system32 \\ \\ .

</dd> <dt>

*WINSScopeID* \[ in, facoltativo\]
</dt> <dd>

Valore dell'identificatore di ambito che verrà aggiunto alla fine del nome NetBIOS del computer. I sistemi che usano lo stesso identificatore di ambito possono comunicare con questo computer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) per un completamento corretto quando non è necessario alcun riavvio. 1 (uno) per un completamento corretto quando è necessario un riavvio; un numero diverso se si verifica un errore. Per altre informazioni sui codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [Codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Completamento riuscito, nessun riavvio necessario** (0)
</dt> <dt>

**Completamento riuscito, riavvio necessario** (1)
</dt> <dt>

**Metodo non supportato in questa piattaforma** (64)
</dt> <dt>

**Errore sconosciuto** (65)
</dt> <dt>

**Non subnet mask** (66)
</dt> <dt>

**Si è verificato un errore durante l'elaborazione di un'istanza restituita** (67)
</dt> <dt>

**Parametro di input non** valido (68)
</dt> <dt>

**Più di 5 gateway specificati** (69)
</dt> <dt>

**Indirizzo IP non valido** (70)
</dt> <dt>

**Indirizzo IP del gateway non** valido (71)
</dt> <dt>

**Si è verificato un errore durante l'accesso** al Registro di sistema per le informazioni richieste (72)
</dt> <dt>

**Nome di dominio non valido** (73)
</dt> <dt>

**Nome host non valido** (74)
</dt> <dt>

**Nessun server WINS primario/secondario definito** (75)
</dt> <dt>

**File non valido** (76)
</dt> <dt>

**Percorso di sistema non** valido (77)
</dt> <dt>

**Copia file non riuscita** (78)
</dt> <dt>

**Parametro di sicurezza non** valido (79)
</dt> <dt>

**Impossibile configurare il servizio TCP/IP** (80)
</dt> <dt>

**Impossibile configurare il servizio DHCP** (81)
</dt> <dt>

**Impossibile rinnovare il lease DHCP** (82)
</dt> <dt>

**Impossibile rilasciare il lease DHCP** (83)
</dt> <dt>

**IP non abilitato sulla scheda** (84)
</dt> <dt>

**IPX non abilitato sulla scheda** (85)
</dt> <dt>

**Errore di limiti del numero di frame/rete** (86)
</dt> <dt>

**Tipo di frame non** valido (87)
</dt> <dt>

**Numero di rete non valido** (88)
</dt> <dt>

**Numero di rete duplicato** (89)
</dt> <dt>

**Parametro fuori dai limiti** (90)
</dt> <dt>

**Accesso negato** (91)
</dt> <dt>

**Memoria insufficiente** (92)
</dt> <dt>

**Esiste già** (93)
</dt> <dt>

**Percorso, file o oggetto non trovato** (94)
</dt> <dt>

**Impossibile inviare una notifica al** servizio (95)
</dt> <dt>

**Impossibile inviare una notifica al servizio DNS** (96)
</dt> <dt>

**Interfaccia non configurabile** (97)
</dt> <dt>

**Non tutti i lease DHCP possono essere rilasciati/rinnovati** (98)
</dt> <dt>

**DHCP non abilitato sulla scheda** (100)
</dt> <dt>

**Altro** (101 4294967295)
</dt> </dl>

## <a name="examples"></a>Esempio

L'esempio di codice VBScript Enable [WINS for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) (Abilita WINS per tutte le schede di rete) in TechNet Gallery usa **EnableWINS** per abilitare WINS in tutte le schede di rete installate in un computer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi hardware del sistema informatico](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Attività WMI: Rete](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Attività WMI: account e domini](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Supporto IPv6 e IPv4 in WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

