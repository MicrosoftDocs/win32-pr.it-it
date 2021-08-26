---
description: Imposta le coppie numero di rete/frame IPX (Internetworking Packet Exchange) per questa scheda di rete.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Metodo SetIPXFrameTypeNetworkPairs Win32_NetworkAdapterConfiguration classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: f914f996e26d64ae66c0be2acf1dee3988ccc2015109c6e7d3b340b406c0c23e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119973026"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a>Metodo SetIPXFrameTypeNetworkPairs della classe NetworkAdapterConfiguration Win32 \_

Imposta le coppie numero di rete/frame IPX (Internetworking Packet Exchange) per questa scheda di rete.

Windows 2000 e Windows NT 3.51 e versioni successive usano un numero di rete IPX a scopo di routing. Viene assegnato a ogni combinazione di tipo di frame/scheda di rete configurata nel sistema del computer. Questo numero viene talvolta definito "numero di rete esterno". Deve essere univoco per ogni segmento di rete. Se il tipo di frame è impostato su AUTO, il numero di rete deve essere zero.

## <a name="syntax"></a>Sintassi


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*IPXNetworkNumber* \[ Pollici\]
</dt> <dd>

Matrice di caratteri che identificano in modo univoco una scheda nel sistema del computer. Il trasporto compatibile con NetWare Link (NWLink) IPX/SPX in Windows 2000 e Windows NT 3.51 o versione successiva usa due tipi diversi di numeri di rete. Questo numero viene talvolta definito numero di rete esterna. Deve essere univoco per ogni segmento di rete. I valori in questo elenco di stringhe devono avere un valore corrispondente nel parametro IPXFrameType che identifica il tipo di frame del pacchetto usato per la rete.

</dd> <dt>

*IPXFrameType* \[ Pollici\]
</dt> <dd>

Matrice integer di identificatori di tipo frame. I valori in questa matrice corrispondono agli elementi nel *parametro IPXNetworkNumber.*

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

**Ethernet II** (0)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

**Ethernet 802.3** (1)


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

**Ethernet 802.2** (2)


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

**SNAP Ethernet** (3)


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

**AUTO** (255)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valore restituito

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

**Altro** (101-4294967295)
</dt> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows Vista<br/>                                                                |
| Server minimo supportato<br/> | Windows Server 2008<br/>                                                          |
| Spazio dei nomi<br/>                | \\CIMV2 radice<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CimWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Cimwin32.dll</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Win32 \_ NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




