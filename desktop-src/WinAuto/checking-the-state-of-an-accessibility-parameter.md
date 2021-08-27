---
title: Controllo dello stato di un parametro di accessibilità
description: Il frammento di codice seguente usa la funzione GetSystemMetrics per controllare il parametro ShowSounds. Se GetSystemMetrics restituisce TRUE, l'applicazione deve presentare tutte le informazioni importanti in formato visivo.
ms.assetid: fb6a0adf-ca38-4e21-9edd-1abb2efd59e5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 374520612ce96522edc1b879a49f5f30a9c7a857f9bb46a562a4ab48effebe9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122251"
---
# <a name="checking-the-state-of-an-accessibility-parameter"></a>Controllo dello stato di un parametro di accessibilità

Il frammento di codice seguente usa [**la funzione GetSystemMetrics**](/windows/desktop/api/winuser/nf-winuser-getsystemmetrics) per controllare il parametro ShowSounds. Se **GetSystemMetrics restituisce** **TRUE,** l'applicazione deve presentare tutte le informazioni importanti in formato visivo.


```C++
BOOL fShowSounds; 
fShowSounds = GetSystemMetrics(SM_SHOWSOUNDS); 
```



 

 