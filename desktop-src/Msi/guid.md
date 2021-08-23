---
description: Il tipo di dati GUID è una stringa di testo che rappresenta un identificatore di classe (ID). COM deve essere in grado di convertire la stringa in un ID classe valido. Tutti i GUID devono essere creati in maiuscolo.
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: GUID (Windows installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5e92688e11d71a51c59a2edc6c3e50ed01ab246c83bf4cfb9ac67b8d6318766b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119649341"
---
# <a name="guid"></a>GUID

Il tipo di dati GUID è una stringa di testo che rappresenta un identificatore di classe (ID). COM deve essere in grado di convertire la stringa in un ID classe valido. Tutti i GUID devono essere creati in maiuscolo.

Il formato valido per un GUID è {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX} dove X è una cifra esadecimale (0,1,2,3,4,5,6,7,8,9,A,B,C,D,E,F).

Si noti che utilità come GUIDGEN possono generare GUID contenenti lettere minuscole. Prima che il GUID possa essere usato dal programma di installazione come codice prodotto, codice pacchetto o codice componente valido, è necessario che tutti questi valori siano stati modificati in lettere maiuscole.

 

 



