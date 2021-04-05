---
description: Questo argomento fornisce una procedura per eseguire la registrazione controllata da tracking dei flussi audio.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Record Track-Controlled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 366b996e590c313cec3ca2e67e12008403e4a4cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103882333"
---
# <a name="track-controlled-record"></a>Record Track-Controlled

Questo argomento fornisce una procedura per eseguire la registrazione controllata da tracking dei flussi audio.

**Per eseguire la registrazione controllata dal rilevamento dei flussi audio**

1.  Selezionare file rileva terminali nei flussi.
2.  Creare il terminale del record di file.
3.  Impostare il nome del file.
4.  Enumera i flussi nella chiamata TAPI. Per questi passaggi, vedere la procedura seguente.
5.  Chiamare il metodo [**Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) sul terminale del record di file per avviare la registrazione del flusso.

**Per enumerare i flussi nella chiamata TAPI**

1.  Creare una traccia dello stesso tipo di audio e della stessa direzione del flusso.
2.  Impostare le proprietà della traccia per il formato audio. Se non è impostato, il formato sarà uguale al formato dei flussi.
3.  Selezionare la traccia nel flusso.

Se si seleziona una traccia in più flussi, questo implica la combinazione di flussi.

 

 



