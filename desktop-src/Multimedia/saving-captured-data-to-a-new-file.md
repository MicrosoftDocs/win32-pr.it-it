---
title: Salvataggio dei dati acquisiti in un nuovo file
description: Salvataggio dei dati acquisiti in un nuovo file
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- Messaggio WM_CAP_FILE_SAVEAS
- capFileSaveAs (macro)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce1966b8cf1e189038e9ee427a868b84a1fb1b50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "103710450"
---
# <a name="saving-captured-data-to-a-new-file"></a>Salvataggio dei dati acquisiti in un nuovo file

Se l'utente desidera salvare i dati acquisiti, l'applicazione deve salvare il contenuto del file di acquisizione in un altro file usando il [**messaggio \_ \_ \_ SaveAs del file di WM Cap**](wm-cap-file-saveas.md) (o la macro [**capFileSaveAs**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) ). Questo messaggio non modifica il nome o il contenuto del file di acquisizione. L'applicazione deve specificare un nome per il nuovo file perché il file di acquisizione mantiene il nome file originale.

In genere, un file di acquisizione è preallocato per il segmento di acquisizione più grande previsto e solo una parte di esso potrebbe essere usato per acquisire i dati. Questo messaggio copia solo la parte del file di acquisizione contenente i dati di acquisizione.

 

 




