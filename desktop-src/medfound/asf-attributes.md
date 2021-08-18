---
description: Attributi ASF
ms.assetid: c1570669-6e9c-4614-af4d-2a148f12e36f
title: Attributi ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: babbb8697126ae6882c11526ed9e6cb31e2233b81685c820d200fbd21bab08c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975030"
---
# <a name="asf-attributes"></a>Attributi ASF

### <a name="profile-attributes"></a>Attributi del profilo

Gli attributi seguenti si applicano ai profili ASF.



| Attributo                                                                      | Descrizione                                                  |
|--------------------------------------------------------------------------------|--------------------------------------------------------------|
| [**MF \_ ASFPROFILE \_ MAXPACKETSIZE**](mf-asfprofile-maxpacketsize-attribute.md) | Specifica le dimensioni massime del pacchetto per un file ASF, in byte. |
| [**MF \_ ASFPROFILE \_ MINPACKETSIZE**](mf-asfprofile-minpacketsize-attribute.md) | Specifica le dimensioni minime del pacchetto per un file ASF, in byte. |



 

### <a name="stream-configuration-attributes"></a>Attributi di configurazione del flusso

Gli attributi seguenti si applicano all'oggetto di configurazione del flusso ASF.



| Attributo                                                                              | Descrizione                                                                   |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**PERDITA \_ DI MF ASFSTREAMCONFIGYBUCKET1 \_**](mf-asfstreamconfig-leakybucket1-attribute.md) | Imposta i parametri medi "leaky bucket" per la codifica di Windows file multimediale. |
| [**PERDITA \_ DI MF ASFSTREAMCONFIGYBUCKET2 \_**](mf-asfstreamconfig-leakybucket2-attribute.md) | Imposta i parametri di picco "bucket di perdita" per la codifica di Windows file multimediale.    |



 

### <a name="media-buffer-attributes"></a>Attributi del buffer multimediale

Gli attributi seguenti si applicano ai buffer multimediali per i pacchetti ASF.



| Attributo                                                                          | Descrizione                                                                               |
|------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| [**LIMITE DEL PACCHETTO MFASFSPLITTER \_ \_**](mfasfsplitter-packet-boundary-attribute.md) | Specifica se un buffer contiene l'inizio di un pacchetto ASF (Advanced Systems Format). |



 

### <a name="presentation-descriptor-attributes"></a>Attributi del descrittore di presentazione

Per un elenco degli attributi applicabili ai descrittori di presentazione di ASF, vedere [Attributi del descrittore di presentazione](presentation-descriptor-attributes.md).

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**IMFASFProfile**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfprofile)
</dt> <dt>

[**IMFASFStreamConfig**](/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamconfig)
</dt> <dt>

[Media Foundation attributi](media-foundation-attributes.md)
</dt> </dl>

 

 



