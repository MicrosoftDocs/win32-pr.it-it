---
description: PNRP usa la funzione WSANSPIoctl per ricevere notifiche sulle modifiche seguenti.
ms.assetid: e5509be1-5294-4696-ab5b-fa2217ae0956
title: PNRP e WSANSPIoctl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cc07415fb483e75af8d836274d45a2c53f205e3aae15f893f909d2363c0d15
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119553311"
---
# <a name="pnrp-and-wsanspioctl"></a>PNRP e WSANSPIoctl

PNRP usa la [**funzione WSANSPIoctl**](winsock-nsp-reference-links.md) per ricevere notifiche sulle modifiche seguenti:

-   Elenco di cloud di rete
-   Disponibilità dei risultati di una richiesta di risoluzione dei nomi

La prima chiamata a [**WSALookupServiceBegin**](winsock-nsp-reference-links.md) definisce il tipo di informazioni a cui un client viene notificato. Un client può ricevere una notifica con un Windows, una routine di completamento, un handle per un oggetto WSAEVENT o una porta. Per altre informazioni sulle opzioni e sull'impostazione *del parametro lpCompletion,* vedere **WSANSPIoctl**.

Per continuare a ricevere notifiche dopo una chiamata a [**WSALookupServiceNext,**](winsock-nsp-reference-links.md)un'applicazione deve chiamare di nuovo **WSANSPIoctl.**

La [**funzione WSALookupServiceNext**](winsock-nsp-reference-links.md) si blocca anche se **viene chiamato WSANSPIoctl.** Prima di **chiamare WSALookupServiceNext,** un'applicazione deve attendere fino a quando non riceve una notifica, se il blocco è un problema.

Quando si chiama questa funzione, i parametri devono avere i valori seguenti:

<dl> <dt>

<span id="hLookup"></span><span id="hlookup"></span><span id="HLOOKUP"></span>*hLookup*
</dt> <dd>

Specifica l'handle [**restituito da WSALookupServiceBegin.**](winsock-nsp-reference-links.md)

</dd> <dt>

<span id="dwControlCode"></span><span id="dwcontrolcode"></span><span id="DWCONTROLCODE"></span>*dwControlCode*
</dt> <dd>

Deve essere **SIO \_ NSP \_ NOTIFY \_ CHANGE**.

</dd> <dt>

<span id="lpvInBuffer"></span><span id="lpvinbuffer"></span><span id="LPVINBUFFER"></span>*lpvInBuffer*
</dt> <dd>

Deve essere **NULL.**

</dd> <dt>

<span id="cbInBuffer"></span><span id="cbinbuffer"></span><span id="CBINBUFFER"></span>*cbInBuffer*
</dt> <dd>

Deve essere zero (0).

</dd> <dt>

<span id="lpvOutBuffer"></span><span id="lpvoutbuffer"></span><span id="LPVOUTBUFFER"></span>*lpvOutBuffer*
</dt> <dd>

Deve essere **NULL.**

</dd> <dt>

<span id="cbOutBuffer"></span><span id="cboutbuffer"></span><span id="CBOUTBUFFER"></span>*cbOutBuffer*
</dt> <dd>

Deve essere zero (0).

</dd> <dt>

<span id="lpcbBytesReturned"></span><span id="lpcbbytesreturned"></span><span id="LPCBBYTESRETURNED"></span>*lpcbBytesReturned*
</dt> <dd>

Deve essere **NULL.**

</dd> <dt>

<span id="lpCompletion"></span><span id="lpcompletion"></span><span id="LPCOMPLETION"></span>*lpCompletion*
</dt> <dd>

Specifica NULL **o** un puntatore a una [**struttura WSACOMPLETION.**](winsock-nsp-reference-links.md)

</dd> </dl>

Dopo aver ricevuto una notifica, chiamare [**WSALookupServiceNext**](winsock-nsp-reference-links.md) una volta per ottenere i risultati.

Per terminare una ricerca, chiamare [**WSALookupServiceEnd**](winsock-nsp-reference-links.md).

## <a name="resolution-notifications"></a>Notifiche di risoluzione

Un client può ricevere una notifica ogni volta che viene aggiunta una voce di risoluzione dei nomi. Il client chiama quindi [**WSALookupServiceNext**](winsock-nsp-reference-links.md) per ottenere i dati di risoluzione.

Se il client non usa questa tecnica, una chiamata a [**WSALookupServiceNext**](winsock-nsp-reference-links.md) può essere bloccata fino a quando non si verifica il timeout specificato.

## <a name="cloud-list-notifications"></a>Notifiche dell'elenco cloud

Un client può ricevere una notifica ogni volta che viene apportata una modifica a un set di cloud.

La [**funzione WSALookupServiceNext**](winsock-nsp-reference-links.md) restituisce **WSA \_ E NO \_ \_ MORE** come delimitatore di set. L'applicazione client deve enumerare i cloud esistenti finché non viene restituito questo messaggio e quindi usare uno schema di notifica per recuperare le modifiche successive non appena si verificano. Un'applicazione client può anche chiamare **WSALookupServiceNext,** ma la chiamata viene bloccata fino a quando non si verifica una modifica.

La [**funzione WSALookupServiceNext**](winsock-nsp-reference-links.md) restituisce un cloud in una **struttura WSAQUERYSET.** Nel membro **dwOutputFlags** viene restituito uno dei flag seguenti.



| Valore               | Descrizione                                             |
|---------------------|---------------------------------------------------------|
| IL \_ RISULTATO È STATO \_ AGGIUNTO   | Viene aggiunto il cloud restituito.                    |
| IL \_ RISULTATO È STATO \_ MODIFICATO | Il cloud restituito viene modificato.                  |
| IL \_ RISULTATO VIENE \_ ELIMINATO | Il cloud restituito viene eliminato e non è valido. |



 

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

 

 



