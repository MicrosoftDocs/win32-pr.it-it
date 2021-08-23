---
description: Codici di errore e di esito positivo dello streaming multimediale
ms.assetid: 3b7a11d2-55b9-4505-8eb2-46be423c662b
title: Codici di errore e di esito positivo dello streaming multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19d1a943ed4d41acd712ad19680e896df33b3afe2ed733bad86a129e2993e6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118952200"
---
# <a name="multimedia-streaming-error-and-success-codes"></a>Codici di errore e di esito positivo dello streaming multimediale

> [!Note]  
> Questa API è deprecata. Le nuove applicazioni non devono usarlo.

 

L'elenco seguente contiene i messaggi di errore e le notifiche di esito positivo per le applicazioni che usano le interfacce di streaming multimediali. Questo elenco non contiene tutti gli errori possibili. Gli errori visualizzati si applicano in modo specifico all'implementazione ® DirectShow® Microsoft delle interfacce di streaming multimediale.



| Valore                       | Codice esadecimale | Descrizione                                                                                                                                                                                |
|-----------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MS \_ S \_ IN SOSPESO              | 0x00040001       | L'aggiornamento di esempio non è ancora completo.                                                                                                                                                         |
| MS \_ S \_ NOUPDATE             | 0x00040002       | L'esempio non è stato aggiornato dopo il completamento forzato.                                                                                                                                            |
| MS \_ S \_ ENDOFSTREAM          | 0x00040003       | Fine del flusso. Esempio non aggiornato.                                                                                                                                                         |
| MS \_ E \_ SAMPLEALLOC          | 0x80040401       | Non è stato possibile rimuovere un oggetto [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) da un [**oggetto IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) perché contiene ancora almeno un campione allocato. |
| MS \_ E \_ PURPOSEID            | 0x80040402       | L'ID scopo specificato non può essere usato per la chiamata.                                                                                                                                       |
| MS \_ E \_ NOSTREAM             | 0x80040403       | Non è possibile trovare alcun flusso con gli attributi specificati.                                                                                                                                      |
| MS \_ E \_ NOSEEKING            | 0x80040404       | Ricerca non supportata per questo [**oggetto IMultiMediaStream.**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream)                                                                                                      |
| MS \_ E \_ INCOMPATIBILE         | 0x80040405       | I formati di flusso non sono compatibili.                                                                                                                                                     |
| MS \_ E \_ OCCUPATO                 | 0x80040406       | L'esempio è occupato.                                                                                                                                                                        |
| MS \_ E \_ NOTINIT              | 0x80040407       | L'oggetto non può accettare la chiamata perché la funzione di inizializzazione o equivalente non è stata chiamata.                                                                                        |
| MS \_ E \_ SOURCEALREADYDEFINED | 0x80040408       | Origine già definita.                                                                                                                                                                    |
| MS \_ E \_ INVALIDSTREAMTYPE    | 0x80040409       | Il tipo di flusso non è valido per questa operazione.                                                                                                                                           |
| MS \_ E \_ NOTRUNNING           | 0x8004040A       | [**L'oggetto IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) non è in esecuzione.                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Streaming multimediale](multimedia-streaming.md)
</dt> </dl>

 

 



