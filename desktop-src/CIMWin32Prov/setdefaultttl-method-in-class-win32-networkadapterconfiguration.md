---
description: Il metodo statico della classe WMI SetDefaultTTL viene usato per impostare il valore TTL (time to Live) predefinito nell'intestazione dei pacchetti IP in uscita.
ms.assetid: 74b060de-512c-407e-9f93-c3b496f8d09d
ms.tgt_platform: multiple
title: Metodo SetDefaultTTL della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTTL
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 253048b44a836f92646124fb972fe32c135e3b9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877197"
---
# <a name="setdefaultttl-method-of-the-win32_networkadapterconfiguration-class"></a>Metodo SetDefaultTTL della \_ classe NetworkAdapterConfiguration Win32

Il metodo statico della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDefaultTTL** viene usato per impostare il valore TTL (time to Live) predefinito nell'intestazione dei pacchetti IP in uscita.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetDefaultTTL(
  [in] uint8 DefaultTTL
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DefaultTTL* \[ in\]
</dt> <dd>

Valore di durata (TTL) impostato nell'intestazione dei pacchetti IP in uscita. Il valore predefinito è 32; Intervallo valido: 1-255

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

## <a name="remarks"></a>Commenti

La durata (TTL) specifica il numero di router che possono essere passati da un pacchetto IP per raggiungere la destinazione prima di essere eliminati. Ogni router decrementa di uno il numero di TTL di un pacchetto e rimuove i pacchetti con un valore TTL pari a 0 (zero).

## <a name="examples"></a>Esempio

L'esempio di [modifica della durata (TTL) predefinita per tutte le schede di rete](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript USA **SetDefaultTTL** per impostare il valore predefinito di durata (TTL) nell'intestazione dei pacchetti IP in uscita su 64

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

 

