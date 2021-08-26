---
title: Apertura e chiusura di file
description: Apertura e chiusura di file
ms.assetid: 72655d33-f685-4205-a982-f7cd20c59f22
keywords:
- Funzione AVIFileOpen
- Funzione AVIFileRelease
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cca5cfdce177e119d178ca09dd447b7d4e3b6a52c1881f059b72e4424f9c54c3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120038321"
---
# <a name="opening-and-closing-files"></a>Apertura e chiusura di file

Un'applicazione deve aprire un file AVI prima della lettura o della scrittura. Per aprire un file AVI, usare la [**funzione AVIFileOpen.**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) **AVIFileOpen** restituisce l'indirizzo di un'interfaccia di file AVI che contiene l'handle del file aperto e incrementa il conteggio dei riferimenti del file.

La **funzione AVIFileOpen** supporta i flag OF usati con la [funzione OpenFile.](/documentation/) Se un'applicazione scrive in un file esistente, deve includere il flag OF \_ WRITE in **AVIFileOpen**. Analogamente, se l'applicazione crea e scrive in un nuovo file, è necessario includere i flag OF \_ CREATE e OF WRITE in \_ **AVIFileOpen**.

Quando si apre un file usando **AVIFileOpen,** è possibile usare un gestore di file predefinito oppure è possibile specificare un gestore di file personalizzato per leggere e scrivere nel file e nei relativi flussi di dati. In entrambi i casi, AVIFile cerca nel Registro di sistema il gestore di file corretto da usare. È necessario assicurarsi che nel Registro di sistema siano presenti gestori di file personalizzati prima che un'applicazione possa accedervi.

È possibile incrementare il conteggio dei riferimenti di un file usando la [**funzione AVIFileAddRef.**](/windows/desktop/api/Vfw/nf-vfw-avifileaddref) Ad esempio, è possibile eseguire questa operazione quando si passa un handle dell'interfaccia file a un'altra applicazione o quando si vuole mantenere aperto un file mentre si usa una funzione che normalmente chiude il file.

È possibile chiudere un file usando la [**funzione AVIFileRelease.**](/windows/desktop/api/Vfw/nf-vfw-avifilerelease) La **funzione AVIFileRelease** decrementa il conteggio dei riferimenti di un file AVI, salva le modifiche apportate al file e, quando il conteggio dei riferimenti raggiunge lo zero, chiude il file. Le applicazioni devono bilanciare il conteggio dei riferimenti includendo una chiamata ad **AVIFileRelease** per ogni uso di [**AVIFileOpen**](/windows/desktop/api/Vfw/nf-vfw-avifileopen) **e AVIFileAddRef.**

> [!Note]  
> Un'applicazione può aprire un file con uno o più thread di programma. Tuttavia, per ottenere prestazioni ottimali, solo un thread deve accedere al file alla volta.

 

 

 