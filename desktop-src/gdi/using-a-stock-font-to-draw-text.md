---
description: Il sistema fornisce sei tipi di carattere predefiniti.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Uso di un tipo di carattere azionario per creare testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56a7e580175956185bcc26a7ebbae8d46dfff078
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "103968269"
---
# <a name="using-a-stock-font-to-draw-text"></a>Uso di un tipo di carattere azionario per creare testo

Il sistema fornisce sei tipi di carattere predefiniti. Un tipo di carattere Stock è un tipo di carattere logico che un'applicazione può ottenere chiamando la funzione [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) e specificando il tipo di carattere richiesto. L'elenco seguente contiene i valori che è possibile specificare per ottenere un tipo di carattere di magazzino.



| Valore                 | Significato                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_tipo di \_ carattere fisso ANSI     | Specifica un tipo di carattere a spaziatura fissa basato sul set di caratteri di Windows. Viene in genere utilizzato un tipo di carattere Courier.                                                                                                                                                                                                |
| \_tipo di \_ carattere ANSI var       | Specifica un tipo di carattere proporzionale in base al set di caratteri di Windows. MS Sans Serif viene in genere usato.                                                                                                                                                                                              |
| \_tipo di carattere predefinito del dispositivo \_ | Specifica il tipo di carattere preferito per il dispositivo specificato. Si tratta in genere del tipo di carattere di sistema per i dispositivi di visualizzazione. per alcune stampanti a matrice di punti, tuttavia, si tratta di un tipo di carattere residente nel dispositivo. La stampa con questo tipo di carattere è in genere più veloce rispetto alla stampa con un tipo di carattere bitmap scaricato.    |
| \_tipo di \_ carattere fisso OEM      | Specifica un tipo di carattere a spaziatura fissa basato su un set di caratteri OEM. Per i computer IBM e compatibili, il tipo di carattere OEM è basato sul set di caratteri IBM PC.                                                                                                                                                 |
| tipo di carattere del sistema \_          | Specifica il tipo di carattere di sistema. Si tratta di un tipo di carattere proporzionale in base al set di caratteri di Windows e viene utilizzato dal sistema operativo per visualizzare i titoli delle finestre, i nomi dei menu e il testo nelle finestre di dialogo. Il tipo di carattere del sistema è sempre disponibile. Altri tipi di carattere sono disponibili solo se sono stati installati. |
| \_tipo di carattere fisso di sistema \_   | Specifica un tipo di carattere a spaziatura fissa compatibile con il tipo di carattere di sistema nelle prime versioni di Windows.                                                                                                                                                                                                        |



 

Per ulteriori informazioni sui tipi di carattere, vedere [informazioni sui tipi di carattere](about-fonts.md).

Nell'esempio seguente viene recuperato un handle per il tipo di carattere di azione variabile, viene selezionato in un contesto di dispositivo e viene quindi scritta una stringa utilizzando il tipo di carattere seguente:


```C++
HFONT hFont, hOldFont; 

// Retrieve a handle to the variable stock font.  
hFont = (HFONT)GetStockObject(ANSI_VAR_FONT); 

// Select the variable stock font into the specified device context. 
if (hOldFont = (HFONT)SelectObject(hdc, hFont)) 
{
    // Display the text string.  
    TextOut(hdc, 10, 50, L"Sample ANSI_VAR_FONT text", 25); 

    // Restore the original font.        
    SelectObject(hdc, hOldFont); 
}
```



Se non sono disponibili altri tipi di carattere predefiniti, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) restituisce un handle per il tipo di carattere del sistema (tipo di carattere del sistema \_ ). Usare i tipi di carattere predefiniti solo se la modalità di mapping per il contesto di dispositivo dell'applicazione è MM \_ testo.

 

 



