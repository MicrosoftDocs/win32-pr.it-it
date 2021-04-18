---
description: Il tipo di dati GUID è una stringa di testo che rappresenta un identificatore di classe (ID). COM deve essere in grado di convertire la stringa in un ID di classe valido. Tutti i GUID devono essere creati in maiuscolo.
ms.assetid: 9e5e2a49-ecf5-43e8-ba6d-42ceaf0beba8
title: GUID (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 297c9995d537f6cf4b9d2ccf35488e27dc35903f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106314263"
---
# <a name="guid"></a>GUID

Il tipo di dati GUID è una stringa di testo che rappresenta un identificatore di classe (ID). COM deve essere in grado di convertire la stringa in un ID di classe valido. Tutti i GUID devono essere creati in maiuscolo.

Il formato valido per un GUID è {XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX}, dove X è una cifra esadecimale (0, 1, 2, 3, 4, 5, 6, 7, 8, 9, A, B, C, D, E, F).

Si noti che utilità come GUIDGEN possono generare GUID contenenti lettere minuscole. Questi devono essere tutti modificati in lettere maiuscole prima che il GUID possa essere usato dal programma di installazione come codice del prodotto valido, codice del pacchetto o codice componente.

 

 



