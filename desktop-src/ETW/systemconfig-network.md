---
description: Questa classe è la classe del tipo di evento per gli eventi di rete. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: SystemConfig_Network classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_Network
- SystemConfig_Network.TcbTablePartitions
- SystemConfig_Network.MaxHashTableSize
- SystemConfig_Network.MaxUserPort
- SystemConfig_Network.TcpTimedWaitDelay
api_type:
- NA
api_location: ''
ms.openlocfilehash: 6b196e8c1ad5a997642cc48491e9d1a4b5e73bc26db71d5ea5258f7cf162a00a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119069691"
---
# <a name="systemconfig_network-class"></a>Classe di rete SystemConfig \_

Questa classe è la classe del tipo di evento per gli eventi di rete.

La sintassi seguente è semplificata dal codice MOF.

## <a name="syntax"></a>Sintassi

``` syntax
[EventType(17), EventTypeName("Network")]
class SystemConfig_Network : SystemConfig
{
  uint32 TcbTablePartitions;
  uint32 MaxHashTableSize;
  uint32 MaxUserPort;
  uint32 TcpTimedWaitDelay;
};
```

## <a name="members"></a>Members

La **classe \_ SystemConfig Network** ha questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La **classe SystemConfig \_ Network** ha queste proprietà.

<dl> <dt>

**MaxHashTableSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(2)
</dt> </dl>

Dimensioni della tabella hash in cui vengono archiviati i blocchi di controllo TCP (TCB). TCP archivia i blocchi di controllo in una tabella hash in modo che possano trovarli molto rapidamente.

</dd> <dt>

**MaxUserPort**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(3)
</dt> </dl>

Il numero di porta più alto che TCP può assegnare quando un'applicazione richiede una porta utente disponibile dal sistema. In genere, le porte effimeri (quelle usate brevemente) vengono allocate ai numeri di porta da 1024 a 5000.

Il valore per il numero di porta utente più alto che TCP può assegnare è controllato da un'impostazione del Registro di sistema. Per altre informazioni, vedere [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).

</dd> <dt>

**TcbTablePartitions**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(1)
</dt> </dl>

Numero di partizioni nella tabella Transport Control Block. Il partizionamento della tabella Transport Control Block riduce al minimo i problemi di accesso alle tabelle. Ciò è particolarmente utile nei sistemi multiprocessore.

</dd> <dt>

**TcpTimedWaitDelay**
</dt> <dd> <dl> <dt>

Tipo di dati: **uint32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId(4)
</dt> </dl>

Tempo che deve trascorrere prima che TCP possa rilasciare una connessione chiusa e riutilizzarne le risorse. Questo intervallo tra la chiusura e la versione è noto come stato TIME \_ WAIT o 2MSL. Durante questo periodo, la connessione può essere riaperta a costi molto inferiori per il client e il server rispetto alla creazione di una nuova connessione.

RFC 793 pubblicato da IETF richiede che TCP mantenga una connessione chiusa per un intervallo almeno pari al doppio della durata massima dei segmenti (2MSL) della rete. Quando viene rilasciata una connessione, è possibile usare la coppia di socket e il blocco di controllo TCP (TCB) per supportare un'altra connessione. Per impostazione predefinita, msl è definito come 120 secondi e il valore di questa voce è uguale a due MSL o 4 minuti. Per altre informazioni, vedere [RFC 793](https://tools.ietf.org/html/rfc973).

La riduzione del valore di questa voce tramite un'impostazione del Registro di sistema consente a TCP di rilasciare connessioni chiuse più velocemente, fornendo più risorse per le nuove connessioni. Tuttavia, se il valore è troppo basso, TCP potrebbe rilasciare le risorse di connessione prima del completamento della connessione, richiedendo al server di usare risorse aggiuntive per ristabilire la connessione.

In genere, TCP non rilascia connessioni chiuse fino alla scadenza del valore di questa voce. Tuttavia, TCP può rilasciare le connessioni prima della scadenza di questo valore se si eseguono blocchi di controllo TCP (TCB). Il numero di TCB creati dal sistema è controllato da un'impostazione del Registro di sistema. Per altre informazioni, vedere [MaxFreeTCBs.](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10))

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | Windows Solo \[ app desktop di Vista\]<br/>       |
| Server minimo supportato<br/> | Windows Solo app desktop server 2008 \[\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 
