---
title: Creazione di un blocco di RIFF
description: Creazione di un blocco di RIFF
ms.assetid: d17f6215-f04f-4776-826e-eedb245f549b
keywords:
- I/O file multimediale, creazione di un blocco RIFF
- I/O di file, creazione di un blocco RIFF
- input e output (I/O), creazione di un blocco RIFF
- I/O (input e output), creazione di un blocco RIFF
- creazione di un blocco RIFF
- mmioCreateChunk (funzione)
- formato file di interscambio risorse (RIFF)
- RIFF (formato file di interscambio risorse)
- I/O RIFF
- Blocco RIFF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adca2cca96b45ecf0313f811b5df4e966be8fc0f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2020
ms.locfileid: "103872422"
---
# <a name="creating-a-riff-chunk"></a>Creazione di un blocco di RIFF

Nell'esempio seguente viene usata la funzione [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) per creare un blocco con un identificatore di blocco "riff" e un tipo di form "RDIB".


```C++
HMMIO    hmmio; 
MMCKINFO mmckinfo; 
. 
. 
. 
mmckinfo.fccType = mmioFOURCC('R', 'D', 'I', 'B'); 
mmioCreateChunk(hmmio, &mmckinfo, MMIO_CREATERIFF); 
```



Se si sta creando un blocco "RIFF" o "LIST", è necessario specificare il tipo di modulo o il tipo di elenco nel membro **fccType** della struttura [**MMCKINFO**](/windows/win32/api/mmiscapi/ns-mmiscapi-mmckinfo) . Nell'esempio precedente, "RDIB" è il tipo di form.

Se si conoscono le dimensioni del campo dati in un nuovo blocco, è possibile impostare il membro **cksize** della struttura **MMCKINFO** quando si crea il blocco. Questo valore verrà scritto nel campo dimensione dati nel nuovo blocco. Se questo valore non è corretto quando si chiama [**mmioAscend**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioascend) per contrassegnare la fine del blocco, verrà riscritto automaticamente per riflettere la dimensione corretta del campo dati.

Dopo aver creato un blocco usando la funzione [**mmioCreateChunk**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmiocreatechunk) , la posizione del file è impostata sul campo dati del blocco (8 byte dall'inizio del blocco). Se il blocco è un blocco "RIFF" o "LIST", la posizione del file è impostata sulla posizione successiva al tipo di modulo o al tipo di elenco (12 byte dall'inizio del blocco).

 

 