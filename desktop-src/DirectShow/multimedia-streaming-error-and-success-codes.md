---
description: Codici di errore e di riuscita dello streaming multimediale
ms.assetid: 3b7a11d2-55b9-4505-8eb2-46be423c662b
title: Codici di errore e di riuscita dello streaming multimediale
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c54a185b46134f4603c7adea0f1b4467da3a2cf
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "104351696"
---
# <a name="multimedia-streaming-error-and-success-codes"></a>Codici di errore e di riuscita dello streaming multimediale

> [!Note]  
> Questa API è deprecata. Le nuove applicazioni non devono utilizzarlo.

 

Nell'elenco seguente sono riportati i messaggi di errore e le notifiche di esito positivo per le applicazioni che utilizzano le interfacce di streaming multimediali. Questo elenco non contiene tutti i possibili errori. gli errori indicati si applicano in modo specifico all'implementazione di Microsoft® DirectShow® delle interfacce di streaming multimediali.



| Valore                       | Codice esadecimale | Descrizione                                                                                                                                                                                |
|-----------------------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| MS \_ S \_ in sospeso              | 0x00040001       | Aggiornamento di esempio non ancora completato.                                                                                                                                                         |
| MS \_ S \_ NOUPDATE             | 0x00040002       | Il campione non è stato aggiornato dopo il completamento forzato.                                                                                                                                            |
| \_ENDOFSTREAM MS S \_          | 0x00040003       | Fine del flusso. Esempio non aggiornato.                                                                                                                                                         |
| MS \_ E \_ SAMPLEALLOC          | 0x80040401       | Non è stato possibile rimuovere un oggetto [**IMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imediastream) da un oggetto [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) perché contiene ancora almeno un campione allocato. |
| MS \_ E \_ PURPOSEID            | 0x80040402       | L'ID scopo specificato non può essere utilizzato per la chiamata.                                                                                                                                       |
| MS \_ E \_ nostream             | 0x80040403       | Non è possibile trovare alcun flusso con gli attributi specificati.                                                                                                                                      |
| MS \_ E \_ noseeking            | 0x80040404       | La ricerca non è supportata per questo oggetto [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) .                                                                                                      |
| MS \_ E \_ incompatibile         | 0x80040405       | I formati dei flussi non sono compatibili.                                                                                                                                                     |
| MS \_ E \_ occupato                 | 0x80040406       | L'esempio è occupato.                                                                                                                                                                        |
| MS \_ E \_ NOTINIT              | 0x80040407       | L'oggetto non può accettare la chiamata perché la relativa funzione di inizializzazione o equivalente non è stata chiamata.                                                                                        |
| MS \_ E \_ SOURCEALREADYDEFINED | 0x80040408       | Origine già definita.                                                                                                                                                                    |
| MS \_ E \_ INVALIDSTREAMTYPE    | 0x80040409       | Il tipo di flusso non è valido per questa operazione.                                                                                                                                           |
| MS \_ E \_ non in esecuzione           | 0x8004040A       | Lo stato dell'oggetto [**IMultiMediaStream**](/previous-versions/windows/desktop/api/mmstream/nn-mmstream-imultimediastream) non è in esecuzione.                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Streaming multimediale](multimedia-streaming.md)
</dt> </dl>

 

 



