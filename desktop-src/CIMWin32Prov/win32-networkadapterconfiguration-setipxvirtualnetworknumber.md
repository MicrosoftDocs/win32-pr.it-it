---
description: Imposta il numero di rete virtuale IPX (Internetworking Packet Exchange) nel computer di destinazione.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Metodo SetIPXVirtualNetworkNumber della classe Win32_NetworkAdapterConfiguration
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: ed6e6802a17ef6ec4393d2ae0c5ec43f0e21d247
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305166"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a>Metodo SetIPXVirtualNetworkNumber della \_ classe NetworkAdapterConfiguration Win32

Imposta il numero di rete virtuale IPX (Internetworking Packet Exchange) nel computer di destinazione. Windows 2000 e Windows NT 3,51 o versione successiva utilizzano un numero di rete interno per il routing interno. Il numero di rete interno è noto anche come numero di rete virtuale. Identifica in modo univoco il sistema computer della rete. Il metodo restituisce un valore intero che può essere interpretted come segue:

## <a name="syntax"></a>Sintassi


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IPXVirtualNetNumber* \[ in\]
</dt> <dd>

Numero di rete virtuale per il sistema.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

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

**Altro** (101-4294967295)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**\_NetworkAdapterConfiguration Win32**](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




