---
description: I gateway &\# 32; Il metodo della classe WMI specifica un elenco di gateway per il routing dei pacchetti a una subnet diversa dalla subnet a cui è connessa la scheda di rete.
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Metodo segateways della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103877961"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a>Metodo segateways della classe Win32 \_ NetworkAdapterConfiguration

Il metodo della [classe WMI](/windows/desktop/WmiSdk/retrieving-a-class) del **gateway** specifica un elenco di gateway per il routing dei pacchetti a una subnet diversa dalla subnet a cui è connessa la scheda di rete.

In questo argomento viene utilizzata la sintassi Managed Object Format (MOF). Per ulteriori informazioni sull'utilizzo di questo metodo, vedere [chiamata a un metodo](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Sintassi


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*DefaultIPGateway* \[ in\]
</dt> <dd>

Elenco di indirizzi IP ai gateway in cui vengono instradati i pacchetti di rete.

</dd> <dt>

*GatewayCostMetric* \[ in, facoltativo\]
</dt> <dd>

Assegna un valore compreso tra 1 e 9999, utilizzato per calcolare le route più veloci e affidabili. I valori di questo parametro corrispondono ai valori nel parametro *DefaultIPGateway* . Il valore predefinito per un gateway è 1.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Restituisce un valore pari a 0 (zero) per un completamento corretto quando non è richiesto un riavvio, 1 (uno) per un completamento corretto quando è necessario un riavvio e qualsiasi altro valore se si verifica un errore. Per ulteriori informazioni sui codici di errore, vedere [**costanti di errore WMI**](/windows/desktop/WmiSdk/wmi-error-constants) o [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum). Per i valori **HRESULT** generali, vedere [codici di errore di sistema](/windows/desktop/Debug/system-error-codes).

<dl> <dt>

**Operazione completata, non è necessario riavviare il computer**
</dt> <dd>

0

</dd> <dt>

**Operazione completata, riavvio richiesto**
</dt> <dd>

1

</dd> <dt>

**Metodo non supportato in questa piattaforma**
</dt> <dd>

64

Metodo non supportato quando la scheda di interfaccia di rete è in modalità DHCP.

</dd> <dt>

**Errore sconosciuto**
</dt> <dd>

65

</dd> <dt>

**subnet mask non valido**
</dt> <dd>

66

</dd> <dt>

**Si è verificato un errore durante l'elaborazione di un'istanza restituita**
</dt> <dd>

67

</dd> <dt>

**Parametro di input non valido**
</dt> <dd>

68

</dd> <dt>

**Sono stati specificati più di 5 gateway**
</dt> <dd>

69

</dd> <dt>

**Indirizzo IP non valido**
</dt> <dd>

70

</dd> <dt>

**Indirizzo IP gateway non valido**
</dt> <dd>

71

</dd> <dt>

**Si è verificato un errore durante l'accesso al registro di sistema per le informazioni richieste**
</dt> <dd>

72

</dd> <dt>

**Nome di dominio non valido**
</dt> <dd>

73

</dd> <dt>

**Nome host non valido**
</dt> <dd>

74

</dd> <dt>

**Nessun server WINS primario/secondario definito**
</dt> <dd>

75

</dd> <dt>

**File non valido**
</dt> <dd>

76

</dd> <dt>

**Percorso di sistema non valido**
</dt> <dd>

77

</dd> <dt>

**Copia del file non riuscita**
</dt> <dd>

78

</dd> <dt>

**Parametro di sicurezza non valido**
</dt> <dd>

79

</dd> <dt>

**Impossibile configurare il servizio TCP/IP**
</dt> <dd>

80

</dd> <dt>

**Non è possibile configurare il servizio DHCP**
</dt> <dd>

81

</dd> <dt>

**Non è possibile rinnovare il lease DHCP**
</dt> <dd>

82

</dd> <dt>

**Non è possibile rilasciare il lease DHCP**
</dt> <dd>

83

</dd> <dt>

**IP non abilitato sulla scheda**
</dt> <dd>

84

</dd> <dt>

**IPX non abilitato sull'adapter**
</dt> <dd>

85

</dd> <dt>

**Errore limite numero frame/rete**
</dt> <dd>

86

</dd> <dt>

**Tipo di frame non valido**
</dt> <dd>

87

</dd> <dt>

**Numero di rete non valido**
</dt> <dd>

88

</dd> <dt>

**Numero di rete duplicato**
</dt> <dd>

89

</dd> <dt>

**Parametro fuori limite**
</dt> <dd>

90

</dd> <dt>

**Accesso negato**
</dt> <dd>

91

</dd> <dt>

**Memoria insufficiente**
</dt> <dd>

92

</dd> <dt>

**Esiste già**
</dt> <dd>

93

</dd> <dt>

**Percorso, file o oggetto non trovato**
</dt> <dd>

94

</dd> <dt>

**Non è possibile inviare una notifica al servizio**
</dt> <dd>

95

</dd> <dt>

**Non è possibile inviare una notifica al servizio DNS**
</dt> <dd>

96

</dd> <dt>

**Interfaccia non configurabile**
</dt> <dd>

97

</dd> <dt>

**Non tutti i lease DHCP possono essere rilasciati/rinnovati**
</dt> <dd>

98

</dd> <dt>

**DHCP non abilitato sull'adapter**
</dt> <dd>

100

</dd> <dt>

**Altri**
</dt> <dd>

101 4294967295

</dd> </dl>

## <a name="remarks"></a>Commenti

Questo metodo funziona solo quando la scheda di interfaccia di rete (NIC) è in modalità IP statico.

Per cancellare il gateway, impostare il gateway sullo stesso IP usato in [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).

## <a name="examples"></a>Esempio

L'esempio [modificare i gateway per una scheda di rete](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript configura due gateway per una scheda di rete.

L'esempio [assegnare un indirizzo IP statico](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript consente di impostare l'indirizzo IP e il gateway di un computer.

L' [indirizzo IP statico e quindi un join a un esempio di](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell di dominio assiste nella ricompilazione dei computer.

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

 

