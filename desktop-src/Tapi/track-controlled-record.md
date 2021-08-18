---
description: In questo argomento viene illustrata una procedura per l'esecuzione di registrazioni controllate dalla traccia di flussi audio.
ms.assetid: 57df081f-df41-4187-910b-939e3d82d7a0
title: Track-Controlled record
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 499c4cb79015effa80add4fc5369ec53f134e83f3f1b7e4cda06b09869c01386
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872671"
---
# <a name="track-controlled-record"></a>Track-Controlled record

In questo argomento viene illustrata una procedura per l'esecuzione di registrazioni controllate dalla traccia di flussi audio.

**Per eseguire la registrazione controllata dalla traccia dei flussi audio**

1.  Selezionare File Track Terminals (Terminali di traccia file) nei flussi.
2.  Creare il terminale record file.
3.  Impostare il nome del file.
4.  Enumerare i flussi nella chiamata TAPI. Per questi passaggi, vedere la procedura seguente.
5.  Chiamare il [**metodo Start**](/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-start) nel terminale di registrazione file per avviare la registrazione del flusso.

**Per enumerare i flussi nella chiamata TAPI**

1.  Creare una traccia dello stesso tipo e direzione audio del flusso.
2.  Impostare le proprietà della traccia per il formato audio. Se non è impostato, il formato sarà lo stesso del formato dei flussi.
3.  Selezionare la traccia nel flusso.

Se viene selezionata una traccia in più flussi, ciò implica la combinazione di flussi.

 

 



