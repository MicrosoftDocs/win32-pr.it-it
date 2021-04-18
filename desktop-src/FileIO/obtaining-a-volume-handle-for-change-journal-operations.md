---
description: 'Per ottenere un handle per un volume da utilizzare con le operazioni del journal delle modifiche USN (Update Sequence Number), chiamare la funzione CreateFile con il parametro lpFileName impostato su una stringa nel formato seguente: \\ \\ . \\ X.'
ms.assetid: a4f4dac5-76fd-4e9e-a71e-665684840d74
title: Ottenere un handle del volume per le operazioni del journal delle modifiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8036fc642de52aa2d7f9bab66dd2e380dcc070c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106319063"
---
# <a name="obtaining-a-volume-handle-for-change-journal-operations"></a>Ottenere un handle del volume per le operazioni del journal delle modifiche

Per ottenere un handle per un volume da utilizzare con le operazioni del journal delle modifiche USN (Update Sequence Number), chiamare la funzione [**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea) con il parametro *lpFileName* impostato su una stringa nel formato seguente: \\ \\ . \\ *X*:

Si noti che *X* è la lettera che identifica l'unità in cui viene visualizzato il volume NTFS.

Se il volume non dispone di una lettera di unità, utilizzare la sintassi descritta in [denominazione di un volume](naming-a-volume.md).

 

 



