---
description: Questa classe è la classe del tipo di evento per gli eventi di rete. La sintassi seguente è semplificata dal codice MOF.
ms.assetid: afa994ef-dd1c-4909-a6cd-7021be4fff40
title: Classe SystemConfig_Network
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
ms.openlocfilehash: 23b469c31645c6a5b04319f91b758ee19beb935c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977583"
---
# <a name="systemconfig_network-class"></a>\_Classe di rete SystemConfig

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

La classe di **\_ rete SystemConfig** presenta questi tipi di membri:

-   [Proprietà](#properties)

### <a name="properties"></a>Proprietà

La classe di **\_ rete SystemConfig** ha queste proprietà.

<dl> <dt>

**MaxHashTableSize**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (2)
</dt> </dl>

Dimensioni della tabella hash in cui vengono archiviati i blocchi di controllo TCP (TCBs). TCP archivia i blocchi di controllo in una tabella hash in modo da poterli trovare molto rapidamente.

</dd> <dt>

**MaxUserPort**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (3)
</dt> </dl>

Il numero di porta massimo TCP può essere assegnato quando un'applicazione richiede una porta utente disponibile dal sistema. In genere, le porte temporanee (quelle utilizzate brevemente) vengono allocate ai numeri di porta da 1024 a 5000.

Il valore per il numero di porta utente massimo TCP può assegnare è controllato da un'impostazione del registro di sistema. Per ulteriori informazioni, vedere [MaxUserPort](/previous-versions/windows/it-pro/windows-2000-server/cc938196(v=technet.10)).

</dd> <dt>

**TcbTablePartitions**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (1)
</dt> </dl>

Numero di partizioni nella tabella dei blocchi di controllo del trasporto. Il partizionamento della tabella dei blocchi di controllo del trasporto riduce la contesa per l'accesso alle tabelle. Questa operazione è particolarmente utile nei sistemi multiprocessore.

</dd> <dt>

**TcpTimedWaitDelay**
</dt> <dd> <dl> <dt>

Tipo di dati: **UInt32**
</dt> <dt>

Tipo di accesso: sola lettura
</dt> <dt>

Qualificatori: WmiDataId (4)
</dt> </dl>

Tempo che deve trascorrere prima che TCP possa rilasciare una connessione chiusa e riutilizzare le relative risorse. Questo intervallo tra la chiusura e la versione è noto come \_ stato Time Wait o 2MSL. Durante questo periodo di tempo, è possibile riaprire la connessione a un costo molto inferiore per il client e il server rispetto alla creazione di una nuova connessione.

La specifica RFC 793 pubblicata da IETF richiede che TCP mantenga una connessione chiusa per un intervallo almeno pari al doppio della durata massima del segmento (2MSL) della rete. Quando viene rilasciata una connessione, è possibile utilizzare la coppia di socket e il blocco di controllo TCP (TCB) per supportare un'altra connessione. Per impostazione predefinita, MSL è definito come 120 secondi e il valore di questa voce è pari a due MSLs o 4 minuti. Per ulteriori informazioni, vedere [RFC 793](https://tools.ietf.org/html/rfc973).

La riduzione del valore di questa voce tramite un'impostazione del registro di sistema consente a TCP di rilasciare connessioni chiuse più velocemente, fornendo più risorse per le nuove connessioni. Tuttavia, se il valore è troppo basso, TCP potrebbe rilasciare le risorse di connessione prima del completamento della connessione, richiedendo al server di usare risorse aggiuntive per ristabilire la connessione.

In genere, TCP non rilascia connessioni chiuse fino alla scadenza del valore di questa voce. Il protocollo TCP, tuttavia, può rilasciare le connessioni prima della scadenza di questo valore se si esauriscono i blocchi di controllo TCP (TCBs). Il numero di TCBs creato dal sistema è controllato da un'impostazione del registro di sistema. Per ulteriori informazioni, vedere [MaxFreeTCBs](/previous-versions/windows/it-pro/windows-2000-server/cc938178(v=technet.10)).

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|------------------------------------------------------|
| Client minimo supportato<br/> | \[Solo app desktop di Windows Vista\]<br/>       |
| Server minimo supportato<br/> | \[Solo app desktop Windows Server 2008\]<br/> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**SystemConfig**](systemconfig.md)
</dt> </dl>

 

 
