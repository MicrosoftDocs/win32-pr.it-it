---
title: Esecuzione di operazioni di I/O su file di memoria
description: Esecuzione di operazioni di I/O su file di memoria
ms.assetid: c0a5c8a0-978f-47d9-8ef0-ad391b9d1e63
keywords:
- I/O file multimediale, memoria
- I/O file, memoria
- input e output (I/O), memoria
- I/O (input e output), memoria
- I/O memoria
- mmioOpen (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82c3e98bbd3636fb88c834957ba2c3fb856406a8
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "104472750"
---
# <a name="performing-memory-file-io"></a>Esecuzione di operazioni di I/O su file di memoria

I servizi di I/O dei file multimediali consentono di trattare un blocco di memoria come file. Questa operazione può essere utile se si dispone già di un'immagine del file in memoria. I file di memoria consentono di ridurre il numero di condizioni del caso speciale nel codice perché, per finalità di I/O, è possibile considerare i file di memoria come se fossero file basati su disco. È inoltre possibile utilizzare i file di memoria con gli Appunti.

Come per I buffer di I/O, i file di memoria possono usare la memoria allocata dall'applicazione o dal gestore di I/O file. Inoltre, i file di memoria possono essere espandibili o non espandibili. Quando il gestore di I/O dei file raggiunge la fine di un file di memoria espandibile, espande il file di memoria in base a un incremento predefinito.

Per aprire un file di memoria, usare la funzione [**mmioOpen**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioopen) con il parametro *SzFilename* impostato su **null** e il \_ flag MMIO ReadWrite impostato nel parametro *dwOpenFlags* . Impostare il parametro *lpmmioinfo* in modo che punti a una struttura [**MMIOINFO**](/previous-versions//dd757322(v=vs.85)) configurata nel modo seguente:

1.  Impostare il membro **pIOProc** su **null**.
2.  Impostare il membro **fccIOProc** su FourCC \_ MEM.
3.  Impostare il membro **pchBuffer** in modo che punti al blocco di memoria. Per richiedere al gestore di I/O dei file di allocare il blocco di memoria, impostare **pchBuffer** su **null**.
4.  Impostare il membro **cchBuffer** sulle dimensioni iniziali del blocco di memoria.
5.  Impostare il membro **adwInfo** sulle dimensioni di espansione minime del blocco di memoria. Per un file di memoria non espandibile, impostare **adwInfo** su **null**.
6.  Impostare tutti gli altri membri su zero.

Non sono previste restrizioni per l'allocazione della memoria da utilizzare come file di memoria non espandibile.

 

 