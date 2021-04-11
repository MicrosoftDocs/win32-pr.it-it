---
description: L'elenco seguente contiene i membri CMSPStream.
ms.assetid: 792a29ac-ebbb-4bb2-bebf-fbf870b18e84
title: Membri di CMSPStream
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dacee41ff95cdf16c7cd50c2e39017d9dfa7e83c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131719"
---
# <a name="cmspstream-members"></a>Membri di CMSPStream



| Tipo di membro                     | Nome                | Descrizione                                                                                                                                |
|---------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| IUnknown                        | \*\_pFTM m           | Puntatore al marshaller a thread libero.                                                                                                   |
| DWORD                           | \_dwState m          | Stato corrente del flusso.                                                                                                           |
| HANDLE                          | \_hAddress m         | Indirizzo in cui viene utilizzato il flusso.                                                                                            |
| DWORD                           | \_dwMediaType m      | Il [**tipo di supporto**](tapimediatype--constants.md) di questo flusso (audio, video e così via).                                                    |
| direzione del terminale \_             | \_direzione m        | [**Direzione**](/windows/desktop/api/Tapi3if/ne-tapi3if-terminal_direction) del flusso (in entrata o in uscita).                                                         |
| CMSPCallBase                    | \*\_pMSPCall m       | Puntatore all'oggetto chiamata.                                                                                                                |
| IGraphBuilder                   | \*\_pIGraphBuilder m | Puntatore a interfacce di oggetti Graph.                                                                                                        |
| IMediaControl                   | \*\_pIMediaControl m | Puntatore all'interfaccia del controllo multimediale.                                                                                                    |
| CMSPArray <ITTerminal \*> | \_terminali m        | Elenco di terminali nel flusso.                                                                                                       |
| CMSPCritSection                 | \_blocco m             | Blocco che protegge l'oggetto flusso. L'oggetto Stream non deve mai acquisire il blocco e quindi chiamare un metodo MSPCall che potrebbe bloccarsi. |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**CMSPStream**](/windows/desktop/api/Mspstrm/nl-mspstrm-cmspstream)
</dt> </dl>

 

 



