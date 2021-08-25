---
title: Salvataggio dei dati acquisiti in un nuovo file
description: Salvataggio dei dati acquisiti in un nuovo file
ms.assetid: 2e6db328-c45e-4a98-9d21-f3c9da261f44
keywords:
- WM_CAP_FILE_SAVEAS messaggio
- Macro capFileSaveAs
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f552f6f2f94ed1a7c7f7f8cae20b20c6fa4b5aa27e8105ab3f5dc33e60b7aff8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119892911"
---
# <a name="saving-captured-data-to-a-new-file"></a>Salvataggio dei dati acquisiti in un nuovo file

Se l'utente vuole salvare i dati acquisiti, l'applicazione deve salvare il contenuto del file di acquisizione in un altro file usando il messaggio [**\_ WM CAP FILE \_ \_ SAVEAS**](wm-cap-file-saveas.md) (o la macro [**capFileSaveAs).**](/windows/desktop/api/Vfw/nf-vfw-capfilesaveas) Questo messaggio non modifica il nome o il contenuto del file di acquisizione. L'applicazione deve specificare un nome per il nuovo file perché il file di acquisizione mantiene il nome file originale.

In genere, un file di acquisizione viene preallocato per il segmento di acquisizione più grande previsto e solo una parte di esso può essere usata per acquisire i dati. Questo messaggio copia solo la parte del file di acquisizione contenente i dati di acquisizione.

 

 




