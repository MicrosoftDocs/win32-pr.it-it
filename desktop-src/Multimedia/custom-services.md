---
title: Servizi personalizzati
description: Servizi personalizzati
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- I/O di file multimediali, servizi personalizzati
- I/O di file, servizi personalizzati
- input e output (I/O), servizi personalizzati
- I/O (input e output), servizi personalizzati
- I/O personalizzato
- mmioInstallIOProc (funzione)
- mmioOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e41e3c5974fee9903c0864b1cfefccc8354b26a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104046697"
---
# <a name="custom-services"></a>Servizi personalizzati

I servizi di I/O dei file multimediali usano le procedure di I/O per gestire l'input fisico e l'output associato alla lettura e alla scrittura in diversi tipi di sistemi di archiviazione, ad esempio sistemi di archiviazione di file e sistemi di archiviazione di database. Per i file System standard e per i file di memoria sono disponibili procedure di I/O predefinite, ma è possibile fornire una procedura di I/O personalizzata per accedere a un sistema di archiviazione univoco tramite la funzione [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) .

Per aprire un file usando una routine di I/O personalizzata, usare la funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . Includere un segno più (+) o la costante CFSEPCHAR nel nome file per separare il nome del file fisico dal nome dell'elemento del file che si vuole aprire. Nell'esempio seguente viene aperto un elemento file denominato "element" da un file denominato FILENAME. ARCO


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



Quando il gestore di I/O dei file rileva un segno più in un nome di file, esamina l'estensione del nome file per determinare quale procedura di I/O associare al file. Nell'esempio precedente, il gestore di I/O dei file tenterà di utilizzare la procedura di I/O associata a. Estensione del nome file ARC; Questa procedura di I/O sarebbe stata installata usando [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc). Se non è installata alcuna routine di I/O, [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) restituisce un errore.

Le procedure di i/O devono rispondere ai messaggi seguenti:

-   [**chiusura di MMIOM \_**](mmiom-close.md)
-   [**MMIOM \_ aperto**](mmiom-open.md)
-   [**MMIOM di \_ lettura**](mmiom-read.md)
-   [**\_scrittura MMIOM**](mmiom-write.md)
-   [**MMIOM \_ Seek**](mmiom-seek.md)
-   [**ridenominazione MMIOM \_**](mmiom-rename.md)
-   [**\_WRITEFLUSH MMIOM**](mmiom-writeflush.md)

È anche possibile creare messaggi personalizzati e inviarli alla routine di I/O tramite la funzione [**mmioSendMessage**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) . Se si definiscono messaggi personalizzati, assicurarsi che siano definiti in corrispondenza o superiore al valore definito dalla \_ costante utente MMIOM.

Oltre all'elaborazione dei messaggi, una routine di I/O deve mantenere il membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) (a cui fa riferimento il parametro *lpmmioinfo* della funzione **mmioOpen** ). Il membro **lDiskOffset** deve sempre contenere l'offset del file nel percorso a cui avrà accesso il successivo messaggio di scrittura MMIOM di \_ lettura o MMIOM \_ . L'offset viene specificato in byte ed è relativo all'inizio del file. La procedura di I/O può utilizzare il membro **adwInfo** per mantenere le informazioni sullo stato richieste. La procedura di I/O non deve modificare altri membri nella struttura **MMIOINFO** .

 

 