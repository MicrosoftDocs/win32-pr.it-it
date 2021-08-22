---
description: Il sistema fornisce sei tipi di carattere predefiniti.
ms.assetid: 349ea57f-dd25-4e33-bbdf-63a320eae3a0
title: Uso di un tipo di carattere predefinito per disegnare testo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9bd140a931a13f6232235036fb7b9cf3de1a20505666e869f214219b7a60a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119468331"
---
# <a name="using-a-stock-font-to-draw-text"></a>Uso di un tipo di carattere predefinito per disegnare testo

Il sistema fornisce sei tipi di carattere predefiniti. Un tipo di carattere predefinito è un tipo di carattere logico che un'applicazione può ottenere chiamando la [funzione GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) e specificando il tipo di carattere richiesto. L'elenco seguente contiene i valori che è possibile specificare per ottenere un tipo di carattere predefinito.



| Valore                 | Significato                                                                                                                                                                                                                                                                                         |
|-----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| CARATTERE \_ FISSO ANSI \_     | Specifica un tipo di carattere monospazio in base Windows set di caratteri. In genere viene usato un tipo di carattere Courier.                                                                                                                                                                                                |
| TIPO DI CARATTERE ANSI \_ \_ VAR       | Specifica un tipo di carattere proporzionale basato sul Windows set di caratteri. Ms Sans Serif viene in genere usato.                                                                                                                                                                                              |
| TIPO DI \_ CARATTERE \_ PREDEFINITO DEL DISPOSITIVO | Specifica il tipo di carattere preferito per il dispositivo specificato. Si tratta in genere del tipo di carattere Sistema per i dispositivi di visualizzazione. tuttavia, per alcune stampanti a matrice di punti, si tratta di un tipo di carattere che risiede nel dispositivo. La stampa con questo tipo di carattere è in genere più veloce rispetto alla stampa con un tipo di carattere bitmap scaricato.    |
| TIPO DI CARATTERE \_ FISSO OEM \_      | Specifica un tipo di carattere monospazio basato su un set di caratteri OEM. Per i computer IBM e compatibili, il tipo di carattere OEM è basato sul set di caratteri IBM PC.                                                                                                                                                 |
| TIPO DI \_ CARATTERE DI SISTEMA          | Specifica il tipo di carattere System. Si tratta di un tipo di carattere proporzionale basato sul set di caratteri Windows e viene usato dal sistema operativo per visualizzare i titoli delle finestre, i nomi dei menu e il testo nelle finestre di dialogo. Il tipo di carattere System è sempre disponibile. Altri tipi di carattere sono disponibili solo se sono stati installati. |
| TIPO DI \_ CARATTERE \_ FISSO DI SISTEMA   | Specifica un tipo di carattere monospazio compatibile con il tipo di carattere System nelle prime versioni di Windows.                                                                                                                                                                                                        |



 

Per altre informazioni sui tipi di carattere, vedere [Informazioni sui tipi di carattere.](about-fonts.md)

L'esempio seguente recupera un handle per il tipo di carattere predefinito della variabile, lo seleziona in un contesto di dispositivo e quindi scrive una stringa usando tale tipo di carattere:


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



Se non sono disponibili altri tipi di carattere predefiniti, [GetStockObject](/windows/desktop/api/Wingdi/nf-wingdi-getstockobject) restituisce un handle per il tipo di carattere System (SYSTEM \_ FONT). È consigliabile usare i tipi di carattere predefiniti solo se la modalità di mapping per il contesto di dispositivo dell'applicazione è TESTO \_ MM.

 

 



