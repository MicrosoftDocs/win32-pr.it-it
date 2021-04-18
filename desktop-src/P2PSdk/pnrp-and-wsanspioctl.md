---
description: PNRP utilizza la funzione WSANSPIoctl per ricevere notifiche sulle modifiche apportate a quanto segue.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP e WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c36dc53fb3d00eeaa2b74be643a7ea62af436e93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312231"
---
# <a name="pnrp-and-wsanspioctl"></a>PNRP e WSANSPIoctl

PNRP utilizza la funzione [**WSANSPIoctl**](winsock-nsp-reference-links.md) per ricevere notifiche sulle modifiche apportate ai seguenti elementi:

-   Elenco di cloud di rete
-   Disponibilità dei risultati di una richiesta di risoluzione dei nomi

La prima chiamata a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) definisce il tipo di informazioni a cui un client riceve una notifica. Un client può ricevere una notifica con un messaggio di Windows, una routine di completamento, un handle per un oggetto WSAEVENT o una porta. Per ulteriori informazioni sulle opzioni e sull'impostazione del parametro *lpCompletion* , vedere **WSANSPIoctl**.

Per continuare a ricevere notifiche dopo una chiamata a [**WSALookupServiceNext**](winsock-nsp-reference-links.md), un'applicazione deve chiamare di nuovo **WSANSPIoctl** .

La funzione [**WSALookupServiceNext**](winsock-nsp-reference-links.md) si blocca anche se viene chiamato **WSANSPIoctl** . Prima di chiamare **WSALookupServiceNext**, un'applicazione deve attendere fino a quando non riceve una notifica, se il blocco è un problema.

Quando si chiama questa funzione, i parametri devono avere i valori seguenti:

<dl> <dt>

<span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*
</dt> <dd>

Specifica l'handle restituito da [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) .

</dd> <dt>

<span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*
</dt> <dd>

Deve essere **una \_ \_ \_ modifica di notifica NSP di sio**.

</dd> <dt>

<span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*
</dt> <dd>

Deve essere **null**.

</dd> <dt>

<span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*
</dt> <dd>

Deve essere zero (0).

</dd> <dt>

<span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*
</dt> <dd>

Deve essere **null**.

</dd> <dt>

<span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*
</dt> <dd>

Deve essere zero (0).

</dd> <dt>

<span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*
</dt> <dd>

Deve essere **null**.

</dd> <dt>

<span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*
</dt> <dd>

Specifica **null** o un puntatore a una struttura [**WSACOMPLETION**](winsock-nsp-reference-links.md) .

</dd> </dl>

Dopo la ricezione di una notifica, chiamare [**WSALookupServiceNext**](winsock-nsp-reference-links.md) una volta per ottenere i risultati.

Per terminare una ricerca, chiamare [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).

## <a name="resolution-notifications"></a>Notifiche di risoluzione

Un client può ricevere una notifica ogni volta che viene aggiunta una voce di risoluzione dei nomi. Il client chiama quindi [**WSALookupServiceNext**](winsock-nsp-reference-links.md) per ottenere i dati di risoluzione.

Se il client non utilizza questa tecnica, è possibile bloccare una chiamata a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) fino a quando non si verifica il timeout specificato.

## <a name="cloud-list-notifications"></a>Notifiche degli elenchi cloud

Un client può ricevere una notifica ogni volta che viene apportata una modifica a un set di cloud.

La funzione [**WSALookupServiceNext**](winsock-nsp-reference-links.md) restituisce **WSA \_ E \_ non \_ più** come delimitatore di set. L'applicazione client deve enumerare i cloud esistenti fino a quando non viene restituito questo messaggio e quindi utilizzare uno schema di notifica per recuperare le modifiche successive non appena si verificano. Un'applicazione client può anche chiamare **WSALookupServiceNext**, ma la chiamata viene bloccata fino a quando non si verifica una modifica.

La funzione [**WSALookupServiceNext**](winsock-nsp-reference-links.md) restituisce un cloud in una struttura **WSAQUERYSET** . Nel membro **dwOutputFlags** viene restituito uno dei flag seguenti.



| Valore               | Descrizione                                             |
|---------------------|---------------------------------------------------------|
| RISULTATO \_ \_ aggiunto   | Viene aggiunto il cloud restituito.                    |
| RISULTATO \_ \_ modificato | Il cloud restituito viene modificato.                  |
| RISULTATO \_ \_ eliminato | Il cloud restituito viene eliminato e non è valido. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[PNRP e WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
</dt> <dt>

[PNRP e WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)
</dt> <dt>

[PNRP e WSAQUERYSET](pnrp-and-wsaqueryset.md)
</dt> <dt>

[Codici di errore PNRP NSP](pnrp-nsp-error-codes.md)
</dt> <dt>

[**WSANSPIoctl**](winsock-nsp-reference-links.md)
</dt> <dt>

**WSALookupServiceBegin**
</dt> <dt>

**WSALookupServiceEnd**
</dt> <dt>

**WSAQUERYSET**
</dt> </dl>

 

 



