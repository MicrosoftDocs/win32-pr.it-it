---
description: Il metodo SetDynamicDNSRegistration indica la registrazione DNS dinamica degli indirizzi IP per questa scheda con binding IP.
ms.assetid: 8e6ca408-3283-40b8-b621-9befdc39b730
ms.tgt_platform: multiple
title: Metodo SetDynamicDNSRegistration della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDynamicDNSRegistration
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36818205e356f873b391159293e9204a9ced44a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103878025"
---
# <a name="setdynamicdnsregistration-method-of-the-win32_networkadapterconfiguration-class"></a>Metodo SetDynamicDNSRegistration della \_ classe NetworkAdapterConfiguration Win32

Il metodo **SetDynamicDNSRegistration** indica la registrazione DNS dinamica degli indirizzi IP per questa scheda con binding IP.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetDynamicDNSRegistration(
  [in]           boolean FullDNSRegistrationEnabled,
  [in, optional] boolean DomainDNSRegistrationEnabled
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*FullDNSRegistrationEnabled* \[ in\]
</dt> <dd>

Se **true**, gli indirizzi IP per questa connessione sono registrati in DNS con il nome DNS completo del computer. Il nome DNS completo del computer viene visualizzato nella scheda **Identificazione rete** del pannello di controllo del sistema.

</dd> <dt>

*DomainDNSRegistrationEnabled* \[ in, facoltativo\]
</dt> <dd>

Se **true**, gli indirizzi IP per questa connessione vengono registrati con il nome di dominio della connessione, oltre a essere registrati con il nome DNS completo del computer. Il nome di dominio della connessione viene impostato utilizzando il metodo [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) o assegnato da DHCP. Il nome registrato è il nome host del computer a cui è stato aggiunto il nome di dominio. Questo parametro ha un significato solo quando *FullDNSRegistrationEnabled* è abilitato. Il valore predefinito è **false**.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto il riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore. Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione completata, non è necessario riavviare il computer**
</dt> <dd>

0

Operazione completata, non è necessario riavviare il computer.

</dd> <dt>

**Operazione completata, riavvio richiesto**
</dt> <dd>

1

Operazione completata, è necessario riavviare il computer.

</dd> <dt>

**Metodo non supportato in questa piattaforma**
</dt> <dd>

64

Metodo non supportato in questa piattaforma.

</dd> <dt>

**Errore sconosciuto**
</dt> <dd>

65

Errore sconosciuto.

</dd> <dt>

**subnet mask non valido**
</dt> <dd>

66

Subnet mask non valido.

</dd> <dt>

**Si è verificato un errore durante l'elaborazione di un'istanza restituita**
</dt> <dd>

67

Si è verificato un errore durante l'elaborazione di un'istanza di restituita.

</dd> <dt>

**Parametro di input non valido**
</dt> <dd>

68

Parametro di input non valido.

</dd> <dt>

**Sono stati specificati più di 5 gateway**
</dt> <dd>

69

Sono stati specificati più di cinque gateway.

</dd> <dt>

**Indirizzo IP non valido**
</dt> <dd>

70

Indirizzo IP non valido.

</dd> <dt>

**Indirizzo IP gateway non valido**
</dt> <dd>

71

Indirizzo IP del gateway non valido.

</dd> <dt>

**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**
</dt> <dd>

72

Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste.

</dd> <dt>

**Nome di dominio non valido**
</dt> <dd>

73

Nome di dominio non valido.

</dd> <dt>

**Nome host non valido**
</dt> <dd>

74

Nome host non valido.

</dd> <dt>

**Nessun server WINS primario/secondario definito**
</dt> <dd>

75

Nessun server WINS primario o secondario definito.

</dd> <dt>

**File non valido**
</dt> <dd>

76

File non valido.

</dd> <dt>

**Percorso di sistema non valido**
</dt> <dd>

77

Percorso di sistema non valido.

</dd> <dt>

**Copia del file non riuscita**
</dt> <dd>

78

Copia del file non riuscita.

</dd> <dt>

**Parametro di sicurezza non valido**
</dt> <dd>

79

Parametro di sicurezza non valido.

</dd> <dt>

**Impossibile configurare il servizio TCP/IP**
</dt> <dd>

80

Impossibile configurare il servizio TCP/IP.

</dd> <dt>

**Non è possibile configurare il servizio DHCP**
</dt> <dd>

81

Impossibile configurare il servizio DHCP.

</dd> <dt>

**Non è possibile rinnovare il lease DHCP**
</dt> <dd>

82

Non è possibile rinnovare il lease DHCP.

</dd> <dt>

**Non è possibile rilasciare il lease DHCP**
</dt> <dd>

83

Impossibile rilasciare il lease DHCP.

</dd> <dt>

**IP non abilitato sulla scheda**
</dt> <dd>

84

IP non abilitato sulla scheda.

</dd> <dt>

**IPX non abilitato sull'adapter**
</dt> <dd>

85

IPX non abilitato sulla scheda.

</dd> <dt>

**Errore limite numero frame/rete**
</dt> <dd>

86

Errore dei limiti del numero di rete o del frame.

</dd> <dt>

**Tipo di frame non valido**
</dt> <dd>

87

Tipo di frame non valido.

</dd> <dt>

**Numero di rete non valido**
</dt> <dd>

88

Numero di rete non valido.

</dd> <dt>

**Numero di rete duplicato**
</dt> <dd>

89

Numero di rete duplicato.

</dd> <dt>

**Parametro fuori limite**
</dt> <dd>

90

Parametro fuori limite.

</dd> <dt>

**Accesso negato**
</dt> <dd>

91

Accesso negato.

</dd> <dt>

**Memoria insufficiente**
</dt> <dd>

92

Memoria insufficiente.

</dd> <dt>

**Esiste già**
</dt> <dd>

93

Esiste già.

</dd> <dt>

**Percorso, file o oggetto non trovato**
</dt> <dd>

94

Il percorso, il file o l'oggetto non è stato trovato.

</dd> <dt>

**Non è possibile inviare una notifica al servizio**
</dt> <dd>

95

Impossibile notificare il servizio.

</dd> <dt>

**Non è possibile inviare una notifica al servizio DNS**
</dt> <dd>

96

Impossibile inviare una notifica al servizio DNS.

</dd> <dt>

**Interfaccia non configurabile**
</dt> <dd>

97

Interfaccia non configurabile.

</dd> <dt>

**Non tutti i lease DHCP possono essere rilasciati/rinnovati**
</dt> <dd>

98

Non tutti i lease DHCP possono essere rilasciati o rinnovati.

</dd> <dt>

**DHCP non abilitato sull'adapter**
</dt> <dd>

100

DHCP non abilitato sulla scheda.

</dd> <dt>

**Altri**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="examples"></a>Esempio

L'esempio [Modify Dynamic DNS Registration for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) VBScript configura la registrazione DNS dinamica per una scheda di rete.

L'esempio di configurazione delle [schede di rete iSCSI come per le procedure consigliate di Microsoft](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) consente di automatizzare le impostazioni di configurazione per una macchina virtuale.

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

 

