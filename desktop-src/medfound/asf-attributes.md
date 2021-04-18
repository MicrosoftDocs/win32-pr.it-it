---
description: Attributi ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Attributi ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ccf09542c8b96cc262cbe029111d3cb74e5b53
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305526"
---
# <a name="asf-attributes"></a>Attributi ASF

### <a name="profile-attributes"></a>Attributi del profilo

Ai profili ASF si applicano gli attributi seguenti.



| Attributo                                                                      | Descrizione                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) | Specifica la dimensione massima del pacchetto per un file ASF, in byte. |
| [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) | Specifica le dimensioni minime del pacchetto per un file ASF, in byte. |



 

### <a name="stream-configuration-attributes"></a>Attributi di configurazione del flusso

Gli attributi seguenti si applicano all'oggetto di configurazione del flusso ASF.



| Attributo                                                                              | Descrizione                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET1**](mf-asfstreamconfig-leakybucket1-attribute.md) | Imposta i parametri medi "bucket Leak" per la codifica di un file di Windows Media. |
| [**MF \_ ASFSTREAMCONFIG \_ LEAKYBUCKET2**](mf-asfstreamconfig-leakybucket2-attribute.md) | Imposta il picco dei parametri "leaky bucket" per la codifica di un file di Windows Media.    |



 

### <a name="media-buffer-attributes"></a>Attributi del buffer multimediale

Gli attributi seguenti si applicano ai buffer multimediali per i pacchetti ASF.



| Attributo                                                                          | Descrizione                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**\_limite pacchetto \_ MFASFSPLITTER**](mfasfsplitter-packet-boundary-attribute.md) | Specifica se un buffer contiene l'inizio di un pacchetto ASF (Advanced Systems Format). |



 

### <a name="presentation-descriptor-attributes"></a>Attributi del descrittore della presentazione

Per un elenco degli attributi applicabili ai descrittori di presentazione ASF, vedere la pagina relativa agli [attributi del descrittore di presentazione](presentation-descriptor-attributes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[Attributi di Media Foundation](media-foundation-attributes.md)
</dt> </dl>

 

 



