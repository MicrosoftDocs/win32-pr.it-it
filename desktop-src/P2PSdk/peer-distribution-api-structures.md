---
description: Il servizio distribuzione peer Microsoft supporta le seguenti strutture.
ms.assetid: 26badfe6-3a5a-4c2e-9ef1-534c2e8573d0
title: Strutture dell'API di distribuzione peer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc9fbf86c242406aa86b7dd30497ba4c5085488
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106312250"
---
# <a name="peer-distribution-api-structures"></a>Strutture dell'API di distribuzione peer

Il servizio distribuzione peer Microsoft supporta le seguenti strutture.



| Struttura                                                              | Descrizione                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_informazioni di \_ base sul client PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_client_basic_info)    | Indica se sono presenti numerosi client che scaricano simultaneamente lo stesso contenuto.                                                                                                                                                                                             |
| [**\_tag di contenuto PEERDIST \_**](/windows/win32/api/peerdist/ns-peerdist-peerdist_content_tag)                 | Contiene un tag fornito dal client che è un valore di input per [**PeerDistClientOpenContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientopencontent). Il tag è associato al segmento di contenuto e viene usato nelle API di gestione del contenuto, ad esempio [**PeerDistClientFlushContent**](/windows/desktop/api/PeerDist/nf-peerdist-peerdistclientflushcontent). |
| [**\_Opzioni di pubblicazione PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_publication_options) | Contiene le opzioni di pubblicazione, incluse le informazioni sulla versione dell'API e i flag di opzione possibili.                                                                                                                                                                                           |
| [**\_Opzioni di recupero \_ peer**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_retrieval_options)         | Contiene la versione delle informazioni sul contenuto da recuperare.                                                                                                                                                                                                                                 |
| [**\_informazioni sullo stato di PEERDIST \_**](/windows/desktop/api/peerdist/ns-peerdist-peerdist_status_info)                 | Contiene informazioni sullo stato corrente e sulle funzionalità del servizio BranchCache nel computer locale.                                                                                                                                                                         |



 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Riferimento all'API di distribuzione peer](peer-distribution-api-reference.md)
</dt> </dl>

 

 



