---
description: Oltre a recuperare i dati di larghezza dei caratteri per i singoli caratteri, le applicazioni devono anche calcolare la larghezza e l'altezza di intere stringhe.
ms.assetid: 0c1d9142-258a-447f-8950-8d684645383b
title: Larghezze e altezze delle stringhe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f57846d0588c518f445523361ae186e4b966bf93
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "103880970"
---
# <a name="string-widths-and-heights"></a>Larghezze e altezze delle stringhe

Oltre a recuperare i dati di larghezza dei caratteri per i singoli caratteri, le applicazioni devono anche calcolare la larghezza e l'altezza di intere stringhe. Due funzioni recuperano le misurazioni di larghezza e altezza di stringa: [**GetTextExtentPoint32**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentpoint32a)e [**GetTabbedTextExtent**](/windows/desktop/api/Winuser/nf-winuser-gettabbedtextextenta). Se la stringa non contiene caratteri di tabulazione, un'applicazione può utilizzare la funzione **GetTextExtentPoint32** per recuperare la larghezza e l'altezza di una stringa specificata. Se la stringa contiene caratteri di tabulazione, un'applicazione deve chiamare la funzione GetTabbedTextExtent.

Le applicazioni possono usare la funzione [**GetTextExtentExPoint**](/windows/desktop/api/Wingdi/nf-wingdi-gettextextentexpointa) per le operazioni di wrapping di parole. Questa funzione restituisce il numero di caratteri di una stringa specificata che rientrano in uno spazio specificato.

## <a name="font-ascenders-and-descenders"></a>Caratteri ascendenti e discendenti

Per alcune applicazioni viene determinata l'interlinea tra le righe di testo di dimensioni diverse utilizzando il numero massimo e il discendente del tipo di carattere. Un'applicazione può recuperare questi valori chiamando la funzione [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) e quindi controllando i membri **tmAscent** e **tmDescent** di [**TEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-textmetrica).

L'ascesa e la discesa massime sono diverse dall'ascesa tipografica e dalla discesa. Nei tipi di carattere TrueType e OpenType, l'ascesa e la discesa tipografici sono in genere la parte superiore del glifo f e la parte inferiore del glifo g. Un'applicazione può recuperare l'ascendente tipografico e il decrescente per un tipo di carattere TrueType o OpenType chiamando la funzione [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) e controllando i valori nei membri **otmMacAscent** e **otmMacDescent** della struttura [**OUTLINETEXTMETRIC**](/windows/desktop/api/Wingdi/ns-wingdi-outlinetextmetrica) .

Nella figura seguente viene illustrata la differenza tra i valori delle metriche di testo verticali restituiti nelle strutture [**NEWTEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-newtextmetrica) e [**OUTLINETEXTMETRIC**](/windows/win32/api/wingdi/ns-wingdi-outlinetextmetrica) . I nomi che iniziano con OTM sono membri della struttura **OUTLINETEXTMETRIC** .

![illustrazione che Mostra come i valori delle metriche del testo sono contrapposti ai valori delle metriche del testo della struttura](images/csftx-03.png)

## <a name="font-dimensions"></a>Dimensioni carattere

Un'applicazione può recuperare le dimensioni fisiche di un tipo di carattere TrueType o OpenType chiamando la funzione [**GetOutlineTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-getoutlinetextmetricsa) . Un'applicazione può recuperare le dimensioni fisiche di qualsiasi altro tipo di carattere chiamando la funzione [**GetTextMetrics**](/windows/desktop/api/Wingdi/nf-wingdi-gettextmetrics) . Per determinare le dimensioni di un dispositivo di output, un'applicazione può chiamare la funzione [**GetDeviceCaps**](/windows/desktop/api/Wingdi/nf-wingdi-getdevicecaps) . **GetDeviceCaps** restituisce le dimensioni fisiche e logiche.

Un pollice logico è una misura che il sistema usa per presentare tipi di carattere leggibili sullo schermo e è approssimativamente dal 30 al 40% più grande di un pollice fisico. L'utilizzo di pollici logici impedisce una corrispondenza esatta tra l'output dello schermo e la stampante. Gli sviluppatori devono tenere presente che il testo in una schermata non è semplicemente una versione ridimensionata del testo che verrà visualizzato nella pagina, in particolare se la grafica è incorporata nel testo.

 

 
