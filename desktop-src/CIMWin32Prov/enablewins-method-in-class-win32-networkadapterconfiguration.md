---
description: EnableWINS &\# 32; Il metodo statico della classe WMI Abilita le impostazioni di Windows Internet Naming Service (WINS) specifiche per TCP/IP, ma indipendente dalla scheda di rete.
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
ms.openlocfilehash: 77f5ba32606ff228908e8b7a1559a73ae5139e9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523386"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a>Metodo EnableWINS della \_ classe NetworkAdapterConfiguration Win32

Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **EnableWINS** Abilita le impostazioni WINS (Windows Internet Naming Service) specifiche per TCP/IP, ma indipendente dalla scheda di rete.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

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

*DNSEnabledForWINSResolution* \[ in\]
</dt> <dd>

Se **true**, il Domain Name System (DNS) è abilitato per la risoluzione dei nomi rispetto alla risoluzione WINS.

</dd> <dt>

*WINSEnableLMHostsLookup* \[ in\]
</dt> <dd>

Se **true**, vengono usati i file di ricerca locali. I file di ricerca conterranno i mapping degli indirizzi IP ai nomi host.

</dd> <dt>

*WINSHostLookupFile* \[ in, facoltativo\]
</dt> <dd>

File di ricerca che contengono mapping degli indirizzi IP ai nomi host. Se disponibile, i file verranno trovati nei driver% SystemRoot% \\ system32 \\ \\ .

</dd> <dt>

*WINSScopeID* \[ in, facoltativo\]
</dt> <dd>

Valore dell'identificatore dell'ambito che verrà aggiunto alla fine del nome NetBIOS del computer. I sistemi che utilizzano lo stesso identificatore di ambito possono comunicare con questo computer.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è necessario riavviare il computer; 1 (uno) per un completamento corretto quando è necessario un riavvio; un numero diverso se si verifica un errore. Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione completata, non è necessario riavviare** il computer (0)
</dt> <dt>

**Operazione completata, riavvio richiesto** (1)
</dt> <dt>

**Metodo non supportato in questa piattaforma** (64)
</dt> <dt>

**Errore sconosciuto** (65)
</dt> <dt>

**Subnet mask non valido** (66)
</dt> <dt>

**Si è verificato un errore durante l'elaborazione di un'istanza restituita** (67)
</dt> <dt>

**Parametro di input non valido** (68)
</dt> <dt>

Sono stati **specificati più di 5 gateway** (69)
</dt> <dt>

**Indirizzo IP non valido** (70)
</dt> <dt>

**Indirizzo IP gateway non valido** (71)
</dt> <dt>

**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste** (72)
</dt> <dt>

**Nome di dominio non valido** (73)
</dt> <dt>

**Nome host non valido** (74)
</dt> <dt>

**Nessun server WINS primario/secondario definito** (75)
</dt> <dt>

**File non valido** (76)
</dt> <dt>

**Percorso di sistema non valido** (77)
</dt> <dt>

**Copia del file non riuscita** (78)
</dt> <dt>

**Parametro di sicurezza non valido** (79)
</dt> <dt>

**Impossibile configurare il servizio TCP/IP** (80)
</dt> <dt>

**Impossibile configurare il servizio DHCP** (81)
</dt> <dt>

**Non è possibile rinnovare il lease DHCP** (82)
</dt> <dt>

**Impossibile rilasciare il lease DHCP** (83)
</dt> <dt>

**IP non abilitato sulla scheda** (84)
</dt> <dt>

**IPX non abilitato sulla scheda** (85)
</dt> <dt>

**Errore limite numero frame/rete** (86)
</dt> <dt>

**Tipo di frame non valido** (87)
</dt> <dt>

**Numero di rete non valido** (88)
</dt> <dt>

**Numero di rete duplicato** (89)
</dt> <dt>

**Parametro fuori limite** (90)
</dt> <dt>

**Accesso negato** (91)
</dt> <dt>

**Memoria insufficiente** (92)
</dt> <dt>

**Già esistente** (93)
</dt> <dt>

**Percorso, file o oggetto non trovato** (94)
</dt> <dt>

**Non è possibile inviare una notifica al servizio** (95)
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

L'esempio di codice per [abilitare WINS per tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript, nella raccolta TechNet, USA **ENABLEWINS** per abilitare WINS in tutte le schede di rete installate in un computer.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Classi hardware del sistema del computer](computer-system-hardware-classes.md)
</dt> <dt>

[**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Attività WMI: rete](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Attività WMI: account e domini](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Supporto di IPv6 e IPv4 in WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

