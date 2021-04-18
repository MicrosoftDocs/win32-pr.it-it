---
description: Windows 7 introduce le librerie, che offrono agli utenti un'unica visualizzazione coerente dei file, anche quando tali file sono archiviati in percorsi diversi.
title: Librerie di Windows
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 19DA68B2-FCB6-443d-A3CD-0BF2F429B149
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: ddb21b4678005d3def5812258a75f2e4fec4b9f2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980935"
---
# <a name="windows-libraries"></a>Librerie di Windows

Windows 7 introduce le librerie, che offrono agli utenti un'unica visualizzazione coerente dei file, anche quando tali file sono archiviati in percorsi diversi. Le librerie possono essere configurate e organizzate da un utente e una raccolta può contenere cartelle trovate nel computer dell'utente e anche cartelle condivise in rete. Le librerie presentano una visualizzazione più semplice del sistema di archiviazione sottostante perché, per l'utente, i file e le cartelle in una raccolta vengono visualizzati in una singola visualizzazione, indipendentemente dalla posizione in cui sono archiviati fisicamente.

Gli sviluppatori che scrivono nuovi programmi in Windows 7 sono invitati a usare le librerie come mezzo tramite cui gli utenti interagiscono con i file usati dal programma. L'utilizzo delle librerie nel programma fornirà agli utenti un'esperienza più semplice e intuitiva in Windows 7.

Gli sviluppatori devono anche esaminare i programmi esistenti e aggiornarli, se necessario, per lavorare con le librerie. Poiché le librerie non fanno parte del file system, le API basate su file system non avranno accesso alle librerie che l'utente potrebbe avere configurato.

I programmi che attualmente consentono agli utenti di archiviare il contenuto in cartelle diverse o in computer diversi trarranno maggiore vantaggio quando aggiungono il supporto per le librerie. Le librerie semplificano la gestione del contenuto in diverse posizioni di archiviazione per lo sviluppatore e l'utente.

In questa guida vengono descritte le librerie, il modo in cui è possibile eseguire i programmi per lavorare con le librerie e alcuni dei modi in cui un programma può utilizzare le librerie per migliorare l'esperienza dell'utente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni sulle librerie](library-leverage-to-manage-folders.md)
</dt> <dt>

[Uso delle librerie nel programma](library-be-library-aware.md)
</dt> <dt>

[**IShellLibrary**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllibrary)
</dt> <dt>

[Collegamenti Shell](./links.md)
</dt> <dt>

[Cartelle note](known-folders.md)
</dt> <dt>

[Schema Descrizione libreria](library-schema-entry.md)
</dt> </dl>

 

 
