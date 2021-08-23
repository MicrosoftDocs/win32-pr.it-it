---
description: 'Per ottenere un handle per un volume da usare con le operazioni del journal delle modifiche USN (Update Sequence Number), chiamare la funzione CreateFile con il parametro lpFileName impostato su una stringa nel formato seguente: \\ \\ . \\ X.'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Recupero di un handle di volume per le operazioni del journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3a7e8090e419df2034d1e1e1726dd74cf2b2915f6976a042a47c73544fa6b38
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683481"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a>Recupero di un handle di volume per le operazioni del journal delle modifiche

Per ottenere un handle per un volume da usare con le operazioni del journal delle modifiche USN (Update Sequence Number), chiamare la [**funzione CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il parametro *lpFileName* impostato su una stringa nel formato seguente: \\ \\ . \\ *X*:

Si noti *che X* è la lettera che identifica l'unità in cui viene visualizzato il volume NTFS.

Se il volume non dispone di una lettera di unità, usare la sintassi descritta in [Denominazione di un volume](naming-a-volume.md).

 

 



