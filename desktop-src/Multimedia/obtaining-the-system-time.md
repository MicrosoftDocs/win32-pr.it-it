---
title: Recupero dell'ora di sistema
description: Recupero dell'ora di sistema
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- timer multimediali, ora di sistema
- timer, ora di sistema
- ora di sistema
- Funzione timeGetTime
- Funzione timeGetSystemTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45460078776732234510d7308bd1e8f490e3871334bdf950bcedd77943b430e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119806471"
---
# <a name="obtaining-the-system-time"></a>Recupero dell'ora di sistema

In genere, prima che un'applicazione inizi a usare i servizi timer multimediali, recupera l'ora *di sistema corrente.* L'ora di sistema è l'ora, in millisecondi, dall'avvio Windows sistema operativo Microsoft. È possibile usare la [**funzione timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) o [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) per recuperare l'ora di sistema. Queste due funzioni sono molto simili: **timeGetTime** restituisce l'ora di sistema e **timeGetSystemTime** riempie una [**struttura MMTIME**](/previous-versions//dd757347(v=vs.85)) con l'ora di sistema.

 

 