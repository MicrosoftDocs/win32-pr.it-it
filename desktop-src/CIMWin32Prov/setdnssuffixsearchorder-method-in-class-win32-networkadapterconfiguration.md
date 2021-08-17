---
description: Il metodo statico della classe WMI SetDNSSuffixSearchOrder usa una matrice di elementi stringa per impostare l'ordine di ricerca dei suffissi.
ms.assetid: 1ad9fc99-8c57-43d4-92d2-b12f2c1451cb
ms.tgt_platform: multiple
title: Metodo SetDNSSuffixSearchOrder della Win32_NetworkAdapterConfiguration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSSuffixSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 85964d24c82367c8609e4f93b02f5614493c56efa299386038d7f73fd749dcab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119440041"
---
# <a name="setdnssuffixsearchorder-method-of-the-win32_networkadapterconfiguration-class"></a>Metodo SetDNSSuffixSearchOrder della classe NetworkAdapterConfiguration Win32 \_

Il metodo statico della classe [WMI](/windows/desktop/WmiSdk/retrieving-a-class) **SetDNSSuffixSearchOrder** usa una matrice di elementi stringa per impostare l'ordine di ricerca dei suffissi.

Questo argomento usa Managed Object Format (MOF). Per altre informazioni sull'uso di questo metodo, vedere [Chiamata di un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetDNSSuffixSearchOrder(
  [in] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DNSDomainSuffixSearchOrder* \[ Pollici\]
</dt> <dd>

Elenco di suffissi del server su cui eseguire query per i server DNS. Il percorso del Registro di sistema del suffisso DNS **è HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Tcpip \| NameServer**

Esempio: "suffix1.company.com", "suffix2.company.com"

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

Parametro al di fuori dei limiti.

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

Non tutti i lease DHCP vengono rilasciati o rinnovati.

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

Si tratta di una chiamata indipendente dall'istanza che si applica a tutti gli adapter, ma solo Windows.

## <a name="examples"></a>Esempio

L'esempio di codice VBScript Modify [the DNS Suffix Search Order for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) configura un computer per l'uso di due suffissi DNS durante l'esecuzione di ricerche DNS.

[L'esempio VBScript Impostazioni](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) abilita DHCP in un computer configura tutte le impostazioni generalmente necessarie per abilitare DHCP in un computer.

Il codice di PowerShell seguente imposta l'ordine di ricerca dei suffissi DNS.


```PowerShell
#First store the suffixes to set in a variable
$suffixes = 'microsoft.com', 'google.com', 'yahoo.com'

#Since this is a static method, get a class object and then call the method. 
$class = [wmiclass]'Win32_NetworkAdapterConfiguration'
$class.SetDNSSuffixSearchOrder($suffixes)
```



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

[Classi hardware del sistema computer](computer-system-hardware-classes.md)
</dt> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> <dt>

[Attività WMI: Rete](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[Attività WMI: Account e domini](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[Supporto di IPv6 e IPv4 in WMI](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

