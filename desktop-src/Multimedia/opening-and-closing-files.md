---
title: Apertura e chiusura di file
description: Apertura e chiusura di file
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- AVIFileOpen (funzione)
- AVIFileRelease (funzione)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68e1c51c4747e03bf4f18a8e6c560e45798e1c8c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/05/2021
ms.locfileid: "106321083"
---
# <a name="opening-and-closing-files"></a>Apertura e chiusura di file

Un'applicazione deve aprire un file AVI prima della lettura o della scrittura. Per aprire un file AVI, usare la funzione [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) . **AVIFileOpen** restituisce l'indirizzo di un'interfaccia file AVI contenente l'handle del file aperto e incrementa il conteggio dei riferimenti del file.

La funzione **AVIFileOpen** supporta l'oggetto dei flag utilizzati con la funzione [OpenFile](/documentation/) . Se un'applicazione scrive in un file esistente, deve includere il flag di \_ scrittura in **AVIFileOpen**. Analogamente, se l'applicazione crea e scrive in un nuovo file, è necessario includere i \_ flag di creazione e di \_ scrittura in **AVIFileOpen**.

Quando si apre un file con **AVIFileOpen**, è possibile usare un gestore di file predefinito oppure specificare un gestore di file personalizzato per la lettura e la scrittura nel file e nei relativi flussi di dati. In entrambi i casi, AVIFile Cerca nel registro di sistema il gestore di file corretto da usare. È necessario assicurarsi che i gestori di file personalizzati si trovino nel registro di sistema prima che un'applicazione possa accedervi.

È possibile incrementare il conteggio dei riferimenti di un file tramite la funzione [**AVIFileAddRef**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) . Ad esempio, è possibile eseguire questa operazione quando si passa un handle dell'interfaccia file a un'altra applicazione o quando si vuole lasciare un file aperto quando si usa una funzione che normalmente chiude il file.

È possibile chiudere un file usando la funzione [**AVIFileRelease**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) . La funzione **AVIFileRelease** decrementa il conteggio dei riferimenti di un file AVI, Salva le modifiche apportate al file e quando il conteggio dei riferimenti raggiunge zero, chiude il file. Le applicazioni devono bilanciare il conteggio dei riferimenti includendo una chiamata a **AVIFileRelease** per ogni uso di [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) e **AVIFileAddRef**.

> [!Note]  
> Un'applicazione può aprire un file con uno o più thread di programma. Tuttavia, per ottenere le migliori prestazioni possibili, solo un thread deve accedere al file in un momento qualsiasi.

 

 

 