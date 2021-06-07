---
title: Per usare un flusso di script
description: Per usare un flusso di script
ms.assetid: 502b1f66-213d-41d8-992a-9bef4f6209f9
keywords:
- Windows Media Format SDK, flussi di script
- Advanced Systems Format (ASF), flussi di script
- ASF (Advanced Systems Format), flussi di script
- flussi di script, informazioni
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09782855bd3000d711f134c5889733e49e020c44
ms.sourcegitcommit: 099ecdda1e83618b844387405da0db0ebda93a65
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 06/04/2021
ms.locfileid: "111444732"
---
# <a name="to-use-a-script-stream"></a>Per usare un flusso di script

Questa sezione descrive come inviare dati script al writer per l'inclusione in un file. Per informazioni sull'inclusione di flussi di script nei profili, vedere [Configurazione di tipi di flusso arbitrari.](configuring-arbitrary-stream-types.md)

Ogni script è costituito da due stringhe, una *stringa di tipo* e una stringa *di* argomento.

I dati dello script devono essere formattati prima di essere inviati al writer. Le stringhe devono essere concatenate, separate da un **carattere NULL** e terminate con un **carattere NULL.** L'esempio seguente illustra uno script legittimo:



| &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; |   &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp; | &nbsp;  | &nbsp; |
|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|-----|
| U   | R   | L   | &nbsp; | h   | t   | t   | p   | :   | /   | /   | w   | w   | w   | .   | a   | d   | a   | t   | u   | m   | .   | c   | o   | m   | &nbsp; |



 

Ogni coppia di comandi script deve essere scritta come esempio nel writer. Per altre informazioni sulla scrittura di esempi, vedere [Per scrivere esempi](to-write-samples.md).

Quando viene riprodotto il file ASF, i comandi script verranno recapitati dal lettore (o lettore sincrono) in ordine di tempo di presentazione. È responsabilità dell'applicazione analizzare le due stringhe e rispondere al comando script.

> [!Note]  
> Quando si usa DRM per crittografare un file, nessun comando script può avere un'ora di presentazione di 0.

 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**Uso di comandi script**](using-script-commands.md)
</dt> </dl>

 

 




