---
description: Nel frammento di codice seguente viene illustrato come richiedere e impostare un indirizzo multicast per una conferenza.
ms.assetid: faff57a9-88b3-45ce-bf9e-3f7087dfd1fd
title: Acquisizione di un indirizzo multicast
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffb451bb403002a4b2dc347abf51e587d8ea02a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128730"
---
# <a name="acquiring-a-multicast-address"></a>Acquisizione di un indirizzo multicast

\[ I controlli e le interfacce per la comunicazione di telefonia IP Rendezvous non sono disponibili per l'uso in Windows Vista, Windows Server 2008 e nelle versioni successive del sistema operativo. L'API del client RTC fornisce funzionalità simili.\]

Nel frammento di codice seguente viene illustrato come richiedere e impostare un indirizzo multicast per una conferenza.

Per motivi di semplicità, in questo frammento viene mostrata l'assegnazione di un indirizzo multicast a un elemento multimediale. In realtà, la selezione di un ambito, la richiesta di indirizzo multicast e l'assegnazione verranno eseguite per ogni elemento multimediale che interessano la conferenza.

Questo frammento presuppone che la [connessione a un server ILS](connecting-to-an-ils-server.md) sia già stata eseguita. Le operazioni illustrate qui verranno eseguite nella sezione "modificare le impostazioni, se necessario" di [creazione di un annuncio](creating-a-conference-announcement.md)per la conferenza.


```C++
// If ( hr != S_OK ) process the error here.
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Interfacce COM multicast](multicast-com-interfaces.md)
</dt> <dt>

[**IMcastAddressAllocation**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastaddressallocation)
</dt> <dt>

[**IMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastscope)
</dt> <dt>

[**IMcastLeaseInfo**](/windows/desktop/api/Mdhcp/nn-mdhcp-imcastleaseinfo)
</dt> <dt>

[**IEnumMcastScope**](/windows/desktop/api/Mdhcp/nn-mdhcp-ienummcastscope)
</dt> <dt>

[**ITConferenceBlob**](itconferenceblob.md)
</dt> <dt>

[**ITSdp**](itsdp.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> <dt>

[**IEnumBstr**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumbstr)
</dt> <dt>

[**ITMedia**](itmedia.md)
</dt> <dt>

[**ITConnection**](itconnection.md)
</dt> </dl>

 

 



