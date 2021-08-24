---
title: Servizi di base
description: Servizi di base
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- I/O di file multimediali, servizi di base
- I/O di file, servizi di base
- input e output (I/O), servizi di base
- I/O (input e output),servizi di base
- I/O di base
- Funzione mmioOpen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3ef4ea778ad0c84137aa75d36f46dc30310180c69416a1240078f01e53d6931
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119145124"
---
# <a name="basic-services"></a>Servizi di base

L'uso dei servizi di I/O di base è simile all'uso dei servizi di I/O di file di runtime della libreria di runtime C. I file devono essere aperti prima di poter essere letti o scritti. Dopo la lettura o la scrittura, il file deve essere chiuso. È anche possibile modificare il percorso di lettura o scrittura corrente all'interno di un file aperto.

Prima di iniziare qualsiasi operazione di I/O in un file, è necessario aprire il file usando la funzione [**mmioOpen.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) Questa funzione restituisce un handle di file di **tipo HMMIO.** È possibile usare questo handle di file per identificare il file aperto quando si chiamano altre funzioni di I/O di file.

> [!Note]  
> Un handle di file **HMMIO** non è un handle di file standard. Non usare handle di file **HMMIO** con funzioni di I/O di file di run-time Win32 o C.

 

Quando si usa [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) per aprire un file, si usa un flag per specificare se viene aperto per la lettura, la scrittura o entrambi. È anche possibile specificare flag che consentono di creare o eliminare un file. Usare la [**funzione mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) per chiudere un file al termine della lettura o della scrittura.

È possibile leggere e scrivere file usando rispettivamente le funzioni [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) e [**mmioWrite.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) La successiva operazione di lettura o scrittura si verifica in corrispondenza della posizione corrente del file o del puntatore del file in un file. La posizione corrente del file viene avanzata ogni volta che un file viene letto o scritto.

È anche possibile modificare la posizione corrente del file usando la [**funzione mmioSeek.**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) È necessario assicurarsi di specificare un percorso valido in un file. Se si specifica un percorso non valido, ad esempio dopo la fine del file, **mmioSeek** potrebbe non restituire un errore, ma le operazioni di I/O successive potrebbero non riuscire.

Sono disponibili flag che è possibile usare con la **funzione mmioOpen** per le operazioni oltre all'I/O di file di base. Specificando una struttura [**MMIOINFO,**](/previous-versions//dd757322(v=vs.85)) ad esempio, è possibile aprire file di memoria, specificare una procedura di I/O personalizzata o fornire un buffer per l'I/O memorizzato nel buffer.

 

 