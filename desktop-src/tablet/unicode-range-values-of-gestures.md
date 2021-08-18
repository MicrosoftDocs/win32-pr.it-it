---
description: "Quando si implementa il proprio sistema di riconoscimento dei movimenti Microsoft, è necessario definire il nome e il valore dell'intervallo Unicode per qualsiasi movimento che il riconoscitore deve riconoscere. Se si decide di implementare i movimenti già supportati o definiti come parte del riconoscimento dei movimenti Microsoft, usare i nomi definiti e i valori di intervallo Unicode per questi movimenti. L'intera raccolta di nomi e valori di intervallo Unicode sia per i movimenti implementati che per i movimenti non implementati nel riconoscimento movimenti Microsoft è disponibile nel file di intestazione Recdefs.h (installato per impostazione predefinita in C: \\\\ Programmi Microsoft Tablet PC Platform SDK \\\\ \\\\ Include). I nomi dei movimenti e i valori dell'intervallo Unicode sono elencati anche nelle tabelle seguenti. Nota Il movimento GESTURE NULL viene usato per indicare che un riconoscitore \\_ non riconosce l'input come movimento."
ms.assetid: 931fc69a-1f7a-492c-8158-0691cd2fe57a
title: Valori di intervallo Unicode dei movimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1f96c1f59ea9e53d63999c01db73c45080f205bccf043e26463563b0f1f6af3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118449224"
---
# <a name="unicode-range-values-of-gestures"></a>Valori di intervallo Unicode dei movimenti

Quando si implementa il proprio sistema di riconoscimento dei movimenti Microsoft, è necessario definire il nome e il valore dell'intervallo Unicode per qualsiasi movimento che il riconoscitore deve riconoscere.

Se si decide di implementare i movimenti già supportati o definiti come parte del riconoscimento dei movimenti Microsoft, usare i nomi definiti e i valori di intervallo Unicode per questi movimenti. L'intera raccolta di nomi e valori di intervallo Unicode sia per i movimenti implementati che per i movimenti non implementati nel riconoscimento movimenti Microsoft è disponibile nel file di intestazione Recdefs.h (installato per impostazione predefinita in C: \\ Programmi Microsoft Tablet PC Platform SDK \\ \\ Include). I nomi dei movimenti e i valori dell'intervallo Unicode sono elencati anche nelle tabelle seguenti.

> [!Note]  
> Il movimento GESTURE \_ NULL viene usato per indicare che un riconoscitore non riconosce l'input come movimento.

 

## <a name="implemented-gestures"></a>Movimenti implementati



| Nome del movimento                          | Valore dell'intervallo Unicode |
|---------------------------------------|---------------------|
| GESTURE \_ NULL<br/>              | 0xf000<br/>   |
| SCRATCHOUT \_ MOVIMENTO<br/>        | 0xf001<br/>   |
| TRIANGOLO MOVIMENTO \_<br/>          | 0xf002<br/>   |
| QUADRATO \_ DEI MOVIMENTI<br/>            | 0xf003<br/>   |
| GESTURE \_ STAR<br/>              | 0xf004<br/>   |
| CONTROLLO \_ MOVIMENTI<br/>             | 0xf005<br/>   |
| GESTURE \_ CURLICUE<br/>          | 0xf010<br/>   |
| GESTURE \_ DOUBLE \_ CURLICUE<br/>  | 0xf011<br/>   |
| CERCHIO \_ MOVIMENTO<br/>            | 0xf020<br/>   |
| CERCHIO \_ DOPPIO \_ MOVIMENTO<br/>    | 0xf021<br/>   |
| MOVIMENTO \_ SEMICIRCOLA \_ A SINISTRA<br/>  | 0xf028<br/>   |
| MOVIMENTO \_ SEMICIRCOLARE \_ A DESTRA<br/> | 0xf029<br/>   |
| FRECCIA \_ CHEVRON MOVIMENTO \_ VERSO L'ALTO<br/>       | 0xf030<br/>   |
| FRECCIA \_ CHEVRON MOVIMENTO \_ VERSO IL BASSO<br/>     | 0xf031<br/>   |
| FRECCIA \_ CHEVRON MOVIMENTO \_ A SINISTRA<br/>     | 0xf032<br/>   |
| FRECCIA \_ DI CONTROLLO DEL MOVIMENTO A \_ DESTRA<br/>    | 0xf033<br/>   |
| FRECCIA \_ DI MOVIMENTO VERSO \_ L'ALTO<br/>         | 0xf038<br/>   |
| FRECCIA \_ DI MOVIMENTO VERSO IL \_ BASSO<br/>       | 0xf039<br/>   |
| FRECCIA \_ A SINISTRA MOVIMENTO \_<br/>       | 0xf03a<br/>   |
| FRECCIA \_ DI MOVIMENTO A \_ DESTRA<br/>      | 0xf03b<br/>   |
| MOVIMENTO \_ VERSO L'ALTO<br/>                | 0xf058<br/>   |
| MOVIMENTO \_ VERSO IL BASSO<br/>              | 0xf059<br/>   |
| MOVIMENTO \_ A SINISTRA<br/>              | 0xf05a<br/>   |
| MOVIMENTO \_ A DESTRA<br/>             | 0xf05b<br/>   |
| MOVIMENTO \_ VERSO L'ALTO VERSO IL \_ BASSO<br/>          | 0xf060<br/>   |
| MOVIMENTO \_ VERSO L'ALTO VERSO IL \_ BASSO<br/>          | 0xf061<br/>   |
| MOVIMENTO \_ A SINISTRA A \_ DESTRA<br/>       | 0xf062<br/>   |
| MOVIMENTO \_ A DESTRA A \_ SINISTRA<br/>       | 0xf063<br/>   |
| MOVIMENTO \_ VERSO \_ L'ALTO A SINISTRA \_ LUNGO<br/>    | 0xf064<br/>   |
| MOVIMENTO \_ VERSO \_ L'ALTO A DESTRA \_ LUNGO<br/>   | 0xf065<br/>   |
| MOVIMENTO \_ VERSO IL BASSO LUNGO A \_ \_ SINISTRA<br/>  | 0xf066<br/>   |
| MOVIMENTO \_ VERSO IL BASSO LUNGO A \_ \_ DESTRA<br/> | 0xf067<br/>   |
| MOVIMENTO \_ VERSO \_ L'ALTO A SINISTRA<br/>          | 0xf068<br/>   |
| MOVIMENTO \_ VERSO \_ L'ALTO A DESTRA<br/>         | 0xf069<br/>   |
| MOVIMENTO \_ VERSO IL BASSO A \_ SINISTRA<br/>        | 0xf06a<br/>   |
| MOVIMENTO \_ VERSO IL BASSO A \_ DESTRA<br/>       | 0xf06b<br/>   |
| MOVIMENTO \_ VERSO \_ L'ALTO<br/>          | 0xf06c<br/>   |
| MOVIMENTO \_ VERSO IL \_ BASSO<br/>        | 0xf06d<br/>   |
| MOVIMENTO \_ VERSO \_ L'ALTO<br/>         | 0xf06e<br/>   |
| MOVIMENTO \_ VERSO IL \_ BASSO<br/>       | 0xf06f<br/>   |
| \_ESCLAMATIVO MOVIMENTO<br/>       | 0xf0a4<br/>   |
| TOCCO \_ CON MOVIMENTO<br/>               | 0xf0f0<br/>   |
| DOPPIO \_ \_ TOCCO CON MOVIMENTO<br/>       | 0xf0f1<br/>   |



 

## <a name="unimplemented-gestures"></a>Movimenti non implementati



| Nome del movimento                             | Valore dell'intervallo Unicode |
|------------------------------------------|---------------------|
| GESTURE \_ INFINITY<br/>             | 0xf006<br/>   |
| INCROCIO \_ MOVIMENTI<br/>                | 0xf007<br/>   |
| PARAGRAFO \_ MOVIMENTO<br/>            | 0xf008<br/>   |
| SEZIONE \_ GESTURE<br/>              | 0xf009<br/>   |
| PUNTO ELENCO \_ MOVIMENTI<br/>               | 0xf00a<br/>   |
| PUNTO \_ ELENCO DEI MOVIMENTI \_ INCROCIATO<br/>        | 0xf00b<br/>   |
| \_SQUIGGLE DEI MOVIMENTI<br/>             | 0xf00c<br/>   |
| SCAMBIO DI \_ MOVIMENTI<br/>                 | 0xf00d<br/>   |
| APERTURA \_ DEI MOVIMENTI<br/>               | 0xf00e<br/>   |
| CLOSEUP \_ MOVIMENTI<br/>              | 0xf00f<br/>   |
| RETTANGOLO DEI \_ MOVIMENTI<br/>            | 0xf012<br/>   |
| TOCCO \_ CERCHIO \_ MOVIMENTO<br/>          | 0xf022<br/>   |
| CERCHIO \_ MOVIMENTO \_<br/>       | 0xf023<br/>   |
| CERCHIO \_ DI \_ MOVIMENTO INCROCIATO<br/>        | 0xf025<br/>   |
| MOVIMENTO \_ CERCHIO \_ LINEA \_ VERT<br/>   | 0xf026<br/>   |
| GESTURE \_ CIRCLE \_ LINE \_ HORZ<br/>   | 0xf027<br/>   |
| FRECCIA \_ DOPPIA MOVIMENTO VERSO \_ \_ L'ALTO<br/>    | 0xf03c<br/>   |
| FRECCIA \_ DOPPIA MOVIMENTO VERSO IL \_ \_ BASSO<br/>  | 0xf03d<br/>   |
| FRECCIA \_ DOPPIA MOVIMENTO A \_ \_ SINISTRA<br/>  | 0xf03e<br/>   |
| FRECCIA \_ DOPPIA A \_ DESTRA MOVIMENTO \_<br/> | 0xf03f<br/>   |
| FRECCIA \_ IN SU VERSO \_ \_ L'ALTO VERSO SINISTRA<br/>      | 0xf040<br/>   |
| FRECCIA \_ VERSO \_ L'ALTO VERSO \_ L'ALTO VERSO DESTRA<br/>     | 0xf041<br/>   |
| FRECCIA \_ GIÙ MOVIMENTO A \_ \_ SINISTRA<br/>    | 0xf042<br/>   |
| MOVIMENTO \_ FRECCIA GIÙ A \_ \_ DESTRA<br/>   | 0xf043<br/>   |
| MOVIMENTO \_ FRECCIA \_ SINISTRA \_ SU<br/>      | 0xf044<br/>   |
| MOVIMENTO \_ FRECCIA SINISTRA VERSO IL \_ \_ BASSO<br/>    | 0xf045<br/>   |
| FRECCIA \_ DESTRA MOVIMENTO VERSO \_ \_ L'ALTO<br/>     | 0xf046<br/>   |
| FRECCIA \_ DESTRA MOVIMENTO VERSO IL \_ \_ BASSO<br/>   | 0xf047<br/>   |
| MOVIMENTO \_ \_ DIAGONALE A SINISTRA<br/>     | 0xf05c<br/>   |
| MOVIMENTO \_ \_ DIAGONALE A DESTRA<br/>    | 0xf05d<br/>   |
| MOVIMENTO \_ \_ DIAGONALE A SINISTRA<br/>   | 0xf05e<br/>   |
| DIAGONALE \_ \_ MOVIMENTO VERSO DESTRA<br/>  | 0xf05f<br/>   |
| LETTERA \_ A DEL \_ MOVIMENTO<br/>            | 0xf080<br/>   |
| LETTERA \_ B DEL \_ MOVIMENTO<br/>            | 0xf081<br/>   |
| LETTERA \_ \_ MOVIMENTO C<br/>            | 0xf082<br/>   |
| LETTERA \_ \_ MOVIMENTO D<br/>            | 0xf083<br/>   |
| LETTERA \_ E DEL \_ MOVIMENTO<br/>            | 0xf084<br/>   |
| LETTERA \_ MOVIMENTO \_ F<br/>            | 0xf085<br/>   |
| LETTERA \_ MOVIMENTO \_ G<br/>            | 0xf086<br/>   |
| LETTERA \_ DI MOVIMENTO \_ H<br/>            | 0xf087<br/>   |
| LETTERA \_ I DEL \_ MOVIMENTO<br/>            | 0xf088<br/>   |
| LETTERA \_ DI MOVIMENTO \_ J<br/>            | 0xf089<br/>   |
| LETTERA \_ MOVIMENTO \_ K<br/>            | 0xf08a<br/>   |
| LETTERA \_ DI MOVIMENTO \_ L<br/>            | 0xf08b<br/>   |
| LETTERA \_ MOVIMENTO \_ M<br/>            | 0xf08c<br/>   |
| LETTERA \_ MOVIMENTO \_ N<br/>            | 0xf08d<br/>   |
| LETTERA \_ O MOVIMENTO \_<br/>            | 0xf08e<br/>   |
| LETTERA \_ MOVIMENTO \_ P<br/>            | 0xf08f<br/>   |
| LETTERA \_ MOVIMENTO \_ Q<br/>            | 0xf090<br/>   |
| LETTERA \_ DI MOVIMENTO \_ R<br/>            | 0xf091<br/>   |
| LETTERA \_ S DEL \_ MOVIMENTO<br/>            | 0xf092<br/>   |
| LETTERA \_ T DEL \_ MOVIMENTO<br/>            | 0xf093<br/>   |
| LETTERA \_ DI MOVIMENTO \_ U<br/>            | 0xf094<br/>   |
| LETTERA \_ DI MOVIMENTO \_ V<br/>            | 0xf095<br/>   |
| LETTERA \_ DI MOVIMENTO \_ W<br/>            | 0xf096<br/>   |
| LETTERA \_ DI MOVIMENTO \_ X<br/>            | 0xf097<br/>   |
| LETTERA \_ DI MOVIMENTO \_ Y<br/>            | 0xf098<br/>   |
| LETTERA \_ DI MOVIMENTO \_ Z<br/>            | 0xf099<br/>   |
| CIFRA \_ MOVIMENTO \_ 0<br/>             | 0xf09a<br/>   |
| CIFRA \_ MOVIMENTO \_ 1<br/>             | 0xf09b<br/>   |
| CIFRA \_ \_ MOVIMENTO 2<br/>             | 0xf09c<br/>   |
| CIFRA \_ \_ MOVIMENTO 3<br/>             | 0xf09d<br/>   |
| CIFRA \_ MOVIMENTO \_ 4<br/>             | 0xf09e<br/>   |
| CIFRA \_ MOVIMENTO \_ 5<br/>             | 0xf09f<br/>   |
| CIFRA \_ \_ MOVIMENTO 6<br/>             | 0xf0a0<br/>   |
| CIFRA \_ MOVIMENTO \_ 7<br/>             | 0xf0a1<br/>   |
| CIFRA \_ \_ MOVIMENTO 8<br/>             | 0xf0a2<br/>   |
| CIFRA \_ \_ MOVIMENTO 9<br/>             | 0xf0a3<br/>   |
| DOMANDA SUL \_ MOVIMENTO<br/>             | 0xf0a5<br/>   |
| MOVIMENTO \_ ACUTO<br/>                | 0xf0a6<br/>   |
| DOLLARO \_ MOVIMENTO<br/>               | 0xf0a7<br/>   |
| ASTERISCO MOVIMENTO \_<br/>             | 0xf0a8<br/>   |
| GESTURE \_ PLUS<br/>                 | 0xf0a9<br/>   |
| GESTURE \_ DOUBLE \_ UP<br/>           | 0xf0b8<br/>   |
| MOVIMENTO \_ \_ RADDOPPIA VERSO IL BASSO<br/>         | 0xf0b9<br/>   |
| MOVIMENTO \_ DOPPIO \_ A SINISTRA<br/>         | 0xf0ba<br/>   |
| MOVIMENTO \_ DOPPIO \_ DESTRO<br/>        | 0xf0bb<br/>   |
| MOVIMENTO \_ TRIPLO \_ VERSO L'ALTO<br/>           | 0xf0bc<br/>   |
| MOVIMENTO \_ TRIPLO \_ VERSO IL BASSO<br/>         | 0xf0bd<br/>   |
| MOVIMENTO \_ TRIPLO \_ SINISTRO<br/>         | 0xf0be<br/>   |
| MOVIMENTO \_ TRIPLO \_ DESTRO<br/>        | 0xf0bf<br/>   |
| GESTURE \_ BRACKET \_ OVER<br/>        | 0xf0e4<br/>   |
| PARENTESI \_ DEL MOVIMENTO \_ SOTTO<br/>       | 0xf0e5<br/>   |
| PARENTESI QUADRA \_ DEL \_ MOVIMENTO A SINISTRA<br/>        | 0xf0e6<br/>   |
| PARENTESI QUADRA \_ DEL \_ MOVIMENTO A DESTRA<br/>       | 0xf0e7<br/>   |
| GESTURE \_ BRACE \_ OVER<br/>          | 0xf0e8<br/>   |
| PARENTESI \_ GRAFFA DI MOVIMENTO \_ IN<br/>         | 0xf0e9<br/>   |
| PARENTESI \_ GRAFFA DI \_ MOVIMENTO VERSO SINISTRA<br/>          | 0xf0ea<br/>   |
| PARENTESI \_ GRAFFA DI \_ MOVIMENTO A DESTRA<br/>         | 0xf0eb<br/>   |
| TOCCO \_ TRIPLO \_ MOVIMENTO<br/>          | 0xf0f2<br/>   |
| TOCCO \_ DEL QUAD CON \_ MOVIMENTO<br/>            | 0xf0f3<br/>   |



 

 

 




