---
title: Struttura RAS_PORT_STATISTICS (rassapi. h)
description: La \_ struttura delle statistiche della porta RAS \_ riporta le statistiche che un server RAS raccoglie per una porta connessa.
ms.assetid: c42c7059-ff92-4f49-a86e-2f47a083aa8e
keywords:
- RAS struttura RAS_PORT_STATISTICS
- RAS puntatore alla struttura PRAS_PORT_STATISTICS
topic_type:
- apiref
api_name:
- RAS_PORT_STATISTICS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85e60fb001da3f8401e47c366eecc86aced22b77
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 12/12/2020
ms.locfileid: "106301754"
---
# <a name="ras_port_statistics-structure"></a>Struttura delle statistiche della \_ porta RAS \_

\[La struttura delle **\_ \_ statistiche della porta RAS** non è supportata a partire da Windows Vista.\]

La struttura delle **\_ \_ statistiche della porta RAS** riporta le statistiche che un server RAS raccoglie per una porta connessa. Il server RAS Reimposta i vari contatori statistici ogni volta che la porta è connessa. Chiamare la funzione [**RasAdminPortClearStatistics**](rasadminportclearstatistics.md) per forzare la reimpostazione dei contatori delle statistiche da parte del server RAS.

Per una porta che fa parte di una connessione a più collegamenti, questa struttura fornisce due set di statistiche. Il primo set contiene le statistiche cumulative per tutte le porte della connessione. Queste statistiche sono le stesse per tutte le porte della connessione. Il secondo set contiene le statistiche solo per questa porta. Se la porta non fa parte di una connessione a più collegamenti, entrambi i set di statistiche avranno le stesse informazioni. Per determinare se una porta fa parte di una connessione a più collegamenti, controllare il \_ bit a collegamento multiplo della porta nel membro **flag** della struttura [**della \_ porta di Ras \_ 0**](ras-port-0-str.md) della porta.

## <a name="syntax"></a>Sintassi


```C++
typedef struct _RAS_PORT_STATISTICS {
  DWORD dwBytesXmited;
  DWORD dwBytesRcved;
  DWORD dwFramesXmited;
  DWORD dwFramesRcved;
  DWORD dwCrcErr;
  DWORD dwTimeoutErr;
  DWORD dwAlignmentErr;
  DWORD dwHardwareOverrunErr;
  DWORD dwFramingErr;
  DWORD dwBufferOverrunErr;
  DWORD dwBytesXmitedUncompressed;
  DWORD dwBytesRcvedUncompressed;
  DWORD dwBytesXmitedCompressed;
  DWORD dwBytesRcvedCompressed;
  DWORD dwPortBytesXmited;
  DWORD dwPortBytesRcved;
  DWORD dwPortFramesXmited;
  DWORD dwPortFramesRcved;
  DWORD dwPortCrcErr;
  DWORD dwPortTimeoutErr;
  DWORD dwPortAlignmentErr;
  DWORD dwPortHardwareOverrunErr;
  DWORD dwPortFramingErr;
  DWORD dwPortBufferOverrunErr;
  DWORD dwPortBytesXmitedUncompressed;
  DWORD dwPortBytesRcvedUncompressed;
  DWORD dwPortBytesXmitedCompressed;
  DWORD dwPortBytesRcvedCompressed;
} RAS_PORT_STATISTICS, *PRAS_PORT_STATISTICS;
```



## <a name="members"></a>Members

<dl> <dt>

**dwBytesXmited**
</dt> <dd>

Specifica il numero totale di byte trasmessi dalla connessione.

</dd> <dt>

**dwBytesRcved**
</dt> <dd>

Specifica il numero totale di byte ricevuti dalla connessione.

</dd> <dt>

**dwFramesXmited**
</dt> <dd>

Specifica il numero totale di frame trasmessi dalla connessione.

</dd> <dt>

**dwFramesRcved**
</dt> <dd>

Specifica il numero totale di frame ricevuti dalla connessione.

</dd> <dt>

**dwCrcErr**
</dt> <dd>

Specifica il numero totale di errori CRC sulla connessione. Gli errori CRC sono causati dall'esito negativo di un controllo di ridondanza ciclico. Un errore CRC indica che uno o più caratteri nel pacchetto di dati ricevuti sono stati rilevati all'arrivo.

</dd> <dt>

**dwTimeoutErr**
</dt> <dd>

Specifica il numero totale di errori di timeout della connessione. Gli errori di timeout si verificano quando un carattere previsto non viene ricevuto nel tempo. Quando si verifica questo problema, il software presuppone che i dati siano andati perduti e che ne richieda il reinviato.

</dd> <dt>

**dwAlignmentErr**
</dt> <dd>

Specifica il numero totale di errori di allineamento nella connessione. Gli errori di allineamento si verificano quando un carattere ricevuto non è quello previsto. Questa situazione si verifica in genere quando un carattere viene perso o si verifica un errore di timeout.

</dd> <dt>

**dwHardwareOverrunErr**
</dt> <dd>

Specifica il numero totale di errori di sovraccarico hardware sulla connessione. Questi errori indicano il numero di volte in cui il computer di invio ha trasmesso i caratteri più velocemente di quanto l'hardware del computer ricevente possa elaborarli. Se il problema persiste, ridurre la velocità di connessione BPS nel client.

</dd> <dt>

**dwFramingErr**
</dt> <dd>

Specifica il numero totale di errori di frame sulla connessione. Un errore di framing si verifica quando viene ricevuto un carattere asincrono con un bit di avvio o di arresto non valido.

</dd> <dt>

**dwBufferOverrunErr**
</dt> <dd>

Specifica il numero totale di errori di sovraccarico del buffer nella connessione. Si verifica un errore di sovraccarico del buffer quando il computer mittente trasmette caratteri più velocemente di quanto il computer ricevente possa adattarlo. Se il problema persiste, ridurre la velocità di connessione BPS nel client.

</dd> <dt>

**dwBytesXmitedUncompressed**
</dt> <dd>

Specifica il numero totale di byte trasmessi non compressi dalla connessione.

</dd> <dt>

**dwBytesRcvedUncompressed**
</dt> <dd>

Specifica il numero totale di byte ricevuti decompressi dalla connessione.

</dd> <dt>

**dwBytesXmitedCompressed**
</dt> <dd>

Specifica il numero totale di byte trasmessi dalla connessione.

</dd> <dt>

**dwBytesRcvedCompressed**
</dt> <dd>

Specifica il numero totale di byte ricevuti compressi dalla connessione.

</dd> <dt>

**dwPortBytesXmited**
</dt> <dd>

Specifica il numero totale di byte trasmessi dalla porta.

</dd> <dt>

**dwPortBytesRcved**
</dt> <dd>

Specifica il numero totale di byte ricevuti dalla porta.

</dd> <dt>

**dwPortFramesXmited**
</dt> <dd>

Specifica il numero totale di frame trasmessi dalla porta.

</dd> <dt>

**dwPortFramesRcved**
</dt> <dd>

Specifica il numero totale di frame ricevuti dalla porta.

</dd> <dt>

**dwPortCrcErr**
</dt> <dd>

Specifica il numero totale di errori CRC sulla porta. Gli errori CRC sono causati dall'esito negativo di un controllo di ridondanza ciclico. Un errore CRC indica che uno o più caratteri nel pacchetto di dati ricevuti sono stati rilevati all'arrivo.

</dd> <dt>

**dwPortTimeoutErr**
</dt> <dd>

Specifica il numero totale di errori di timeout sulla porta. Gli errori di timeout si verificano quando un carattere previsto non viene ricevuto nel tempo. Quando si verifica questo problema, il software presuppone che i dati siano andati perduti e che ne richieda il reinviato.

</dd> <dt>

**dwPortAlignmentErr**
</dt> <dd>

Specifica il numero totale di errori di allineamento sulla porta. Gli errori di allineamento si verificano quando un carattere ricevuto non è quello previsto. Questa situazione si verifica in genere quando un carattere viene perso o si verifica un errore di timeout.

</dd> <dt>

**dwPortHardwareOverrunErr**
</dt> <dd>

Specifica il numero totale di errori di sovraccarico hardware sulla porta. Questi errori indicano il numero di volte in cui il computer di invio ha trasmesso i caratteri più velocemente di quanto l'hardware del computer ricevente possa elaborarli. Se il problema persiste, ridurre la velocità di connessione BPS nel client.

</dd> <dt>

**dwPortFramingErr**
</dt> <dd>

Specifica il numero totale di errori di framing sulla porta. Un errore di framing si verifica quando viene ricevuto un carattere asincrono con un bit di avvio o di arresto non valido.

</dd> <dt>

**dwPortBufferOverrunErr**
</dt> <dd>

Specifica il numero totale di errori di sovraccarico del buffer sulla porta. Si verifica un errore di sovraccarico del buffer quando il computer mittente trasmette caratteri più velocemente di quanto il computer ricevente possa adattarlo. Se il problema persiste, ridurre la velocità di connessione BPS nel client.

</dd> <dt>

**dwPortBytesXmitedUncompressed**
</dt> <dd>

Specifica il numero totale di byte trasmessi non compressi dalla porta. Se la porta fa parte di una connessione a più collegamenti, questo membro non è valido. Usare invece le statistiche di compressione per la connessione.

</dd> <dt>

**dwPortBytesRcvedUncompressed**
</dt> <dd>

Specifica il numero totale di byte ricevuti decompressi dalla porta. Se la porta fa parte di una connessione a più collegamenti, questo membro non è valido. Usare invece le statistiche di compressione per la connessione.

</dd> <dt>

**dwPortBytesXmitedCompressed**
</dt> <dd>

Specifica il numero totale di byte trasmessi dalla porta. Se la porta fa parte di una connessione a più collegamenti, questo membro non è valido. Usare invece le statistiche di compressione per la connessione.

</dd> <dt>

**dwPortBytesRcvedCompressed**
</dt> <dd>

Specifica il numero totale di byte ricevuti dalla porta compressi. Se la porta fa parte di una connessione a più collegamenti, questo membro non è valido. Usare invece le statistiche di compressione per la connessione.

</dd> </dl>

## <a name="requirements"></a>Requisiti



| Requisito | Valore |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimo supportato<br/> | Windows 2000 Professional \[solo app desktop\]<br/>                           |
| Server minimo supportato<br/> | Windows 2000 Server \[solo app desktop\]<br/>                                 |
| Fine del supporto client<br/>    | Windows XP<br/>                                                                |
| Fine del supporto server<br/>    | Windows Server 2003<br/>                                                       |
| Intestazione<br/>                   | <dl> <dt>Rassapi. h</dt> </dl> |



## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Panoramica del servizio di accesso remoto (RAS)](about-remote-access-service.md)
</dt> <dt>

[Strutture di amministrazione del server RAS](ras-server-administration-structures.md)
</dt> <dt>

[**\_Porta RAS \_ 0**](ras-port-0-str.md)
</dt> <dt>

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortClearStatistics**](rasadminportclearstatistics.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





