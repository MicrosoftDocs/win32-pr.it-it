---
title: Servizi di base
description: Servizi di base
ms.assetid: 7b77ed5d-0bd9-4926-b73f-afc7070fe314
keywords:
- I/O file multimediale, servizi di base
- I/O di file, servizi di base
- input e output (I/O), servizi di base
- I/O (input e output), servizi di base
- I/O di base
- mmioOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688dc6b96c612d94524758acce5d8c742fc13a36
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104398986"
---
# <a name="basic-services"></a>Servizi di base

L'utilizzo dei servizi di I/O di base è simile all'utilizzo dei servizi di I/O dei file di runtime della libreria di runtime del linguaggio C. Per poter essere letti o scritti, è necessario aprire i file. Dopo la lettura o la scrittura, il file deve essere chiuso. È anche possibile modificare il percorso di lettura o scrittura corrente all'interno di un file aperto.

Prima di iniziare qualsiasi operazione di I/O in un file, è necessario aprire il file utilizzando la funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) . Questa funzione restituisce un handle di file di tipo **HMMIO**. È possibile utilizzare questo handle di file per identificare il file aperto quando si chiamano altre funzioni di I/O di file.

> [!Note]  
> Un handle di file **HMMIO** non è un handle di file standard. Non usare gli handle di file **HMMIO** con le funzioni di I/O dei file di runtime Win32 o C.

 

Quando si usa [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) per aprire un file, si usa un flag per specificare se si sta aprendo per la lettura, la scrittura o entrambi. È inoltre possibile specificare i flag che consentono di creare o eliminare un file. Utilizzare la funzione [**mmioClose**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioclose) per chiudere un file al termine della lettura o della scrittura.

È possibile leggere e scrivere file usando rispettivamente le funzioni [**mmioRead**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioread) e [**mmioWrite**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiowrite) . La successiva operazione di lettura o scrittura si verifica in corrispondenza della posizione corrente del file o del puntatore del file in un file. La posizione del file corrente è avanzata ogni volta che un file viene letto o scritto.

È anche possibile modificare la posizione del file corrente usando la funzione [**mmioSeek**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioseek) . È necessario assicurarsi di specificare un percorso valido in un file. Se si specifica un percorso non valido, ad esempio dopo la fine del file, **mmioSeek** potrebbe non restituire un errore, ma le operazioni di I/O successive potrebbero non riuscire.

Sono disponibili flag che è possibile usare con la funzione **mmioOpen** per le operazioni successive all'i/O di file di base. Specificando una struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) , ad esempio, è possibile aprire file di memoria, specificare una routine di i/o personalizzata o fornire un buffer per i/o memorizzato nel buffer.

 

 