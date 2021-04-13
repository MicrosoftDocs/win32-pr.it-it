---
title: Recupero dell'ora di sistema
description: Recupero dell'ora di sistema
ms.assetid: 33dfcd56-11d9-45b9-b983-8354526101a7
keywords:
- timer multimediali, ora di sistema
- timer, ora di sistema
- ora di sistema
- timeGetTime (funzione)
- timeGetSystemTime (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89fdcc905569a500afe689658676137c460d19d8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472819"
---
# <a name="obtaining-the-system-time"></a>Recupero dell'ora di sistema

In genere, prima che un'applicazione inizi a usare i servizi timer multimediali, viene recuperata l' *ora di sistema* corrente. L'ora di sistema è il tempo, in millisecondi, dopo l'avvio del sistema operativo Microsoft Windows. Per recuperare l'ora di sistema, è possibile usare la funzione [**timeGetTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegettime) o [**timeGetSystemTime**](/windows/desktop/api/TimeAPI/nf-timeapi-timegetsystemtime) . Queste due funzioni sono molto simili: **timeGetTime** restituisce l'ora di sistema e **timeGetSystemTime** riempie una struttura [**MMTIME**](/previous-versions//dd757347(v=vs.85)) con l'ora di sistema.

 

 