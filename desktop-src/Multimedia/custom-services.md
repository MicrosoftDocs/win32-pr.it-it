---
title: Servizi personalizzati
description: Servizi personalizzati
ms.assetid: 98b68205-3a34-4406-84de-bf2c8a5ed5b0
keywords:
- I/O di file multimediali, servizi personalizzati
- I/O di file, servizi personalizzati
- input e output (I/O), servizi personalizzati
- I/O (input e output),servizi personalizzati
- I/O personalizzato
- Funzione mmioInstallIOProc
- Funzione mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8c2418d3a87669527feda37547674bee83175dd6e4533312e8b89c346048c04
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144574"
---
# <a name="custom-services"></a>Servizi personalizzati

I servizi di I/O di file multimediali usano procedure di I/O per gestire l'input fisico e l'output associati alla lettura e alla scrittura in diversi tipi di sistemi di archiviazione, ad esempio sistemi di archiviazione file e sistemi di archiviazione di database. Esistono procedure di I/O predefinite per i file system standard e per i file di memoria, ma è possibile fornire una procedura di I/O personalizzata per accedere a un sistema di archiviazione univoco usando la funzione [**mmioInstallIOProc.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc)

Per aprire un file usando una procedura di I/O personalizzata, usare la [**funzione mmioOpen.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) Includere un segno più (+) o la costante CFSEPCHAR nel nome file per separare il nome del file fisico dal nome dell'elemento del file da aprire. Nell'esempio seguente viene aperto un elemento file denominato "element" da un file denominato FILENAME. Arco:


```C++
mmioOpen("filename.arc+element", NULL, MMIO_READ); 
```



Quando il gestore di I/O di file rileva un segno più in un nome file, esamina l'estensione del nome file per determinare quale procedura di I/O associare al file. Nell'esempio precedente, il gestore di I/O di file tentava di usare la procedura di I/O associata a . Estensione del nome file ARC; questa procedura di I/O sarebbe stata installata usando [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc). Se non è installata alcuna procedura di I/O, [**mmioOpen restituisce**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) un errore.

Le procedure di I/O devono rispondere ai messaggi seguenti:

-   [**MMIOM \_ CLOSE**](mmiom-close.md)
-   [**MMIOM \_ OPEN**](mmiom-open.md)
-   [**MMIOM \_ READ**](mmiom-read.md)
-   [**MMIOM \_ WRITE**](mmiom-write.md)
-   [**RICERCA \_ MMIOM**](mmiom-seek.md)
-   [**RIDENOMINAZIONE DI MMIOM \_**](mmiom-rename.md)
-   [**MMIOM \_ WRITEFLUSH**](mmiom-writeflush.md)

È anche possibile creare messaggi personalizzati e inviarli alla procedura di I/O usando la funzione [**mmioSendMessage.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiosendmessage) Se si definiscono messaggi personalizzati, assicurarsi che siano definiti in corrispondenza o al di sopra del valore definito dalla costante MMIOM \_ USER.

Oltre all'elaborazione dei messaggi, una procedura di I/O deve mantenere il membro **lDiskOffset** della struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) (a cui punta il parametro *lpmmioinfo* della funzione **mmioOpen).** Il **membro lDiskOffset** deve sempre contenere l'offset del file rispetto al percorso a cui accederà il successivo messaggio MMIOM READ o \_ MMIOM \_ WRITE. L'offset è specificato in byte ed è relativo all'inizio del file. La procedura di I/O può usare il **membro adwInfo** per gestire le informazioni sullo stato necessarie. La procedura di I/O non deve modificare altri membri nella **struttura MMIOINFO.**

 

 