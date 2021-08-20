---
description: Il metodo statico della classe WMI SetTcpMaxConnectRetransmissions viene usato per impostare il numero di tentativi che TCP ritrasmetterà una richiesta di connessione prima dell'interruzione.
ms.assetid: cb0dfba3-4ef5-4052-94f3-f688a1c55d90
ms.tgt_platform: multiple
title: Metodo SetTcpMaxConnectRetransmissions della Win32_NetworkAdapterConfiguration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxConnectRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: de612b2ece1f186fef218d8642d8ce2e28154c159df1bb5203f0fe4692f6baab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119020459"
---
# <a name="settcpmaxconnectretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a>Metodo SetTcpMaxConnectRetransmissions della classe NetworkAdapterConfiguration Win32 \_

Il metodo statico della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetTcpMaxConnectRetransmissions** viene usato per impostare il numero di tentativi che TCP ritrasmetterà una richiesta di connessione prima dell'interruzione.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetTcpMaxConnectRetransmissions(
  [in] uint32 TcpMaxConnectRetransmissions
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*TcpMaxConnectRetransmissions* \[ Pollici\]
</dt> <dd>

Numero di tentativi che TCP ritrasmetterà una richiesta di connessione prima dell'interruzione. L'intervallo valido per i valori è 0 - 0xFFFFFFFF.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce il valore 0 (zero) per un completamento corretto quando non è necessario alcun riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e un numero diverso se si verifica un errore. Per altre informazioni sui codici di errore, vedere [**Costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum.**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum) Per i valori **HRESULT** generali, vedere [Codici di errore di sistema.](/windows/desktop/Debug/system-error-codes)

<dl> <dt>

**Completamento riuscito, riavvio non necessario**
</dt> <dd>

0

Completamento riuscito, riavvio non necessario.

</dd> <dt>

**Completamento riuscito, riavvio necessario**
</dt> <dd>

1

Completamento riuscito. È necessario riavviare il computer.

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

**Non subnet mask**
</dt> <dd>

66

Non subnet mask.

</dd> <dt>

**Si è verificato un errore durante l'elaborazione di un'istanza restituita**
</dt> <dd>

67

Si è verificato un errore durante l'elaborazione di un'istanza restituita.

</dd> <dt>

**Parametro di input non valido**
</dt> <dd>

68

Parametro di input non valido.

</dd> <dt>

**Più di 5 gateway specificati**
</dt> <dd>

69

Sono stati specificati più di cinque gateway.

</dd> <dt>

**Indirizzo IP non valido**
</dt> <dd>

70

Indirizzo IP non valido.

</dd> <dt>

**Indirizzo IP del gateway non valido**
</dt> <dd>

71

Indirizzo IP del gateway non valido.

</dd> <dt>

**Si è verificato un errore durante l'accesso al Registro di sistema per le informazioni richieste**
</dt> <dd>

72

Si è verificato un errore durante l'accesso al Registro di sistema per le informazioni richieste.

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

**Impossibile configurare il servizio DHCP**
</dt> <dd>

81

Impossibile configurare il servizio DHCP.

</dd> <dt>

**Impossibile rinnovare il lease DHCP**
</dt> <dd>

82

Impossibile rinnovare il lease DHCP.

</dd> <dt>

**Non è possibile rilasciare il lease DHCP**
</dt> <dd>

83

Impossibile rilasciare il lease DHCP.

</dd> <dt>

**IP non abilitato sulla scheda**
</dt> <dd>

84

IP non abilitato nella scheda.

</dd> <dt>

**IPX non abilitato sulla scheda**
</dt> <dd>

85

IPX non abilitato sulla scheda.

</dd> <dt>

**Errore di limiti dei numeri di rete/frame**
</dt> <dd>

86

Errore di limiti del numero di rete o del frame.

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

**Parametro fuori dai limiti**
</dt> <dd>

90

Parametro fuori dai limiti.

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

Percorso, file o oggetto non trovato.

</dd> <dt>

**Impossibile inviare una notifica al servizio**
</dt> <dd>

95

Impossibile inviare una notifica al servizio.

</dd> <dt>

**Impossibile inviare una notifica al servizio DNS**
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

**DHCP non abilitato sulla scheda**
</dt> <dd>

100

DHCP non abilitato sulla scheda.

</dd> <dt>

**Altri**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Commenti

Il timeout di ritrasmissione iniziale è di tre secondi e raddoppia per ogni tentativo successivo.

## <a name="examples"></a>Esempio

L'esempio VBScript Modify [the Maximum Allowed TCP Connection Retransmissions](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) (Modifica il numero massimo di ritrasmissioni di connessioni TCP consentite) configura il numero di volte in cui TCP ritrasmetterà un tentativo di connessione prima di abbandonare il lavoro.

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista, Windows Vista<br/>                                                 |
| Server minimo supportato<br/> | Windows Server 2008, Windows Server 2008<br/>                                     |
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

 

