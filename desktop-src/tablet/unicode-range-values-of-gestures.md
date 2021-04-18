---
description: "Quando si implementa il riconoscitore di movimento Microsoft, è necessario definire il nome e il valore dell'intervallo Unicode per qualsiasi movimento che il riconoscimento deve riconoscere. Se si decide di implementare i movimenti già supportati o definiti come parte del sistema di riconoscimento del movimento Microsoft, utilizzare i nomi definiti e i valori di intervallo Unicode per questi movimenti. L'intera raccolta di nomi e di valori di intervallo Unicode per i movimenti implementati e non implementati nel riconoscitore di movimento Microsoft è disponibile nel file di intestazione Recdefs. h (installato per impostazione predefinita in C: \\\\ programmi \\\\ Microsoft Tablet PC Platform SDK \\\\ ). Nelle tabelle seguenti sono elencati anche i nomi di movimento e i valori di intervallo Unicode. Si noti che il movimento \\_ null gesto viene usato per indicare che un riconoscimento non riconosce l'input come un movimento."
ms.assetid: 931fc69a-1f7a-492c-8158-0691cd2fe57a
title: Valori di intervallo Unicode dei movimenti
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b66b9b4ee511e9eeadd79e0dff2675391ceee6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106313908"
---
# <a name="unicode-range-values-of-gestures"></a>Valori di intervallo Unicode dei movimenti

Quando si implementa il riconoscitore di movimento Microsoft, è necessario definire il nome e il valore dell'intervallo Unicode per qualsiasi movimento che il riconoscimento deve riconoscere.

Se si decide di implementare i movimenti già supportati o definiti come parte del sistema di riconoscimento del movimento Microsoft, utilizzare i nomi definiti e i valori di intervallo Unicode per questi movimenti. L'intera raccolta di nomi e di valori di intervallo Unicode per i movimenti implementati e non implementati nel riconoscitore di movimento Microsoft è disponibile nel file di intestazione Recdefs. h (installato per impostazione predefinita in C: \\ programmi \\ Microsoft Tablet PC Platform SDK \\ ). Nelle tabelle seguenti sono elencati anche i nomi di movimento e i valori di intervallo Unicode.

> [!Note]  
> Il movimento \_ null gesto viene utilizzato per indicare che un riconoscimento non riconosce l'input come un movimento.

 

## <a name="implemented-gestures"></a>Movimenti implementati



| Nome movimento                          | Valore dell'intervallo Unicode |
|---------------------------------------|---------------------|
| GESTO \_ null<br/>              | 0xF000<br/>   |
| Scratch di movimento \_<br/>        | 0xf001<br/>   |
| \_triangolo movimento<br/>          | 0xf002<br/>   |
| quadrato del movimento \_<br/>            | 0xf003<br/>   |
| \_stella movimento<br/>              | 0xf004<br/>   |
| \_controllo movimenti<br/>             | 0xf005<br/>   |
| \_ricciolo movimento<br/>          | 0xf010<br/>   |
| \_ricciolo doppio \_ movimento<br/>  | 0xf011<br/>   |
| \_cerchio movimento<br/>            | 0xf020<br/>   |
| \_cerchio doppio \_ movimento<br/>    | 0xf021<br/>   |
| MOVIMENTO \_ semicerchio a \_ sinistra<br/>  | 0xf028<br/>   |
| MOVIMENTO \_ semicerchio a \_ destra<br/> | 0xf029<br/>   |
| MOVIMENTO \_ \_ freccia su<br/>       | 0xf030<br/>   |
| \_freccia di espansione \_ verso il basso<br/>     | 0xf031<br/>   |
| freccia di \_ espansione a \_ sinistra<br/>     | 0xf032<br/>   |
| freccia di \_ espansione a \_ destra<br/>    | 0xf033<br/>   |
| freccia di movimento \_ \_ verso l'alto<br/>         | 0xf038<br/>   |
| freccia di movimento \_ \_ verso il basso<br/>       | 0xf039<br/>   |
| \_freccia a \_ sinistra del movimento<br/>       | 0xf03a<br/>   |
| freccia movimento a \_ \_ destra<br/>      | 0xf03b<br/>   |
| MOVIMENTI \_ verso l'alto<br/>                | 0xf058<br/>   |
| MOVIMENTO \_ verso il basso<br/>              | 0xf059<br/>   |
| MOVIMENTO a \_ sinistra<br/>              | 0xf05a<br/>   |
| MOVIMENTO a \_ destra<br/>             | 0xf05b<br/>   |
| MOVIMENTO verso \_ il \_ basso<br/>          | 0xf060<br/>   |
| MOVIMENTO \_ verso l' \_ alto<br/>          | 0xf061<br/>   |
| MOVIMENTO \_ sinistro \_ destro<br/>       | 0xf062<br/>   |
| MOVIMENTO a \_ destra a \_ sinistra<br/>       | 0xf063<br/>   |
| MOVIMENTO \_ su \_ sinistra \_ lungo<br/>    | 0xf064<br/>   |
| MOVIMENTI \_ verso l'alto a \_ destra \_<br/>   | 0xf065<br/>   |
| MOVIMENTO \_ verso \_ sinistra \_ lungo<br/>  | 0xf066<br/>   |
| MOVIMENTO \_ verso il basso a \_ destra \_<br/> | 0xf067<br/>   |
| MOVIMENTO \_ verso l'alto a \_ sinistra<br/>          | 0xf068<br/>   |
| MOVIMENTI \_ verso l'alto a \_ destra<br/>         | 0xf069<br/>   |
| MOVIMENTO \_ verso \_ sinistra<br/>        | 0xf06a<br/>   |
| MOVIMENTO \_ verso il basso a \_ destra<br/>       | 0xf06b<br/>   |
| MOVIMENTO \_ interrotto \_<br/>          | 0xf06c<br/>   |
| MOVIMENTO \_ \_ verso il basso<br/>        | 0xf06d<br/>   |
| MOVIMENTO \_ \_ a destra<br/>         | 0xf06e<br/>   |
| MOVIMENTO a \_ destra \_<br/>       | 0xf06f<br/>   |
| \_esclamazione di movimento<br/>       | 0xf0a4<br/>   |
| \_tocco movimenti<br/>               | 0xf0f0<br/>   |
| GESTO \_ doppio \_ tocco<br/>       | 0xf0f1<br/>   |



 

## <a name="unimplemented-gestures"></a>Movimenti non implementati



| Nome movimento                             | Valore dell'intervallo Unicode |
|------------------------------------------|---------------------|
| \_infinito movimento<br/>             | 0xf006<br/>   |
| \_incrociato movimento<br/>                | 0xf007<br/>   |
| \_paragrafo movimento<br/>            | 0xf008<br/>   |
| \_sezione gesture<br/>              | 0xf009<br/>   |
| \_punto elenco movimenti<br/>               | 0xf00a<br/>   |
| \_ \_ incrociato movimento<br/>        | 0xf00b<br/>   |
| \_zigzag movimento<br/>             | 0xf00c<br/>   |
| \_scambio movimenti<br/>                 | 0xf00d<br/>   |
| \_OPENUP movimento<br/>               | 0xf00e<br/>   |
| primo piano movimento \_<br/>              | 0xf00f<br/>   |
| \_rettangolo movimento<br/>            | 0xf012<br/>   |
| \_tocco cerchio \_ movimento<br/>          | 0xf022<br/>   |
| \_cerchio del cerchio del movimento \_<br/>       | 0xf023<br/>   |
| \_cerchio movimento \_ incrociato<br/>        | 0xf025<br/>   |
| \_ \_ linea \_ VERTa cerchio movimento<br/>   | 0xf026<br/>   |
| \_linea cerchio \_ movimento \_ orizzontalmente<br/>   | 0xf027<br/>   |
| \_ \_ freccia a doppio movimento \_ su<br/>    | 0xf03c<br/>   |
| \_freccia a doppio movimento verso il \_ \_ basso<br/>  | 0xf03d<br/>   |
| SEGNO \_ a \_ freccia doppia a \_ sinistra<br/>  | 0xf03e<br/>   |
| \_freccia doppia \_ a \_ destra<br/> | 0xf03f<br/>   |
| \_freccia su \_ a \_ sinistra<br/>      | 0xf040<br/>   |
| \_freccia su \_ a \_ destra<br/>     | 0xf041<br/>   |
| \_freccia verso il basso a \_ \_ sinistra<br/>    | 0xf042<br/>   |
| \_freccia verso il basso a \_ \_ destra<br/>   | 0xf043<br/>   |
| \_freccia sinistra \_ movimento \_ verso l'alto<br/>      | 0xf044<br/>   |
| \_freccia sinistra \_ movimento \_ verso il basso<br/>    | 0xf045<br/>   |
| \_ \_ freccia a destra \_ verso l'alto<br/>     | 0xf046<br/>   |
| \_freccia destra \_ \_ verso il basso<br/>   | 0xf047<br/>   |
| \_LEFTUP diagonale movimento \_<br/>     | 0xf05c<br/>   |
| \_RIGHTUP diagonale movimento \_<br/>    | 0xf05d<br/>   |
| \_LEFTDOWN diagonale movimento \_<br/>   | 0xf05e<br/>   |
| \_RIGHTDOWN diagonale movimento \_<br/>  | 0xf05f<br/>   |
| \_lettera \_ di movimento A<br/>            | 0xf080<br/>   |
| lettera di movimento \_ \_ B<br/>            | 0xf081<br/>   |
| lettera di movimento \_ \_ C<br/>            | 0xf082<br/>   |
| lettera di movimento \_ \_ D<br/>            | 0xf083<br/>   |
| lettera di movimento \_ \_ E<br/>            | 0xf084<br/>   |
| lettera di movimento \_ \_ F<br/>            | 0xf085<br/>   |
| lettera di movimento \_ \_ G<br/>            | 0xf086<br/>   |
| lettera di movimento \_ \_ H<br/>            | 0xf087<br/>   |
| lettera di movimento \_ \_ I<br/>            | 0xf088<br/>   |
| lettera di movimento \_ \_ J<br/>            | 0xf089<br/>   |
| lettera di movimento \_ \_ K<br/>            | 0xf08a<br/>   |
| lettera di movimento \_ \_ L<br/>            | 0xf08b<br/>   |
| lettera di movimento \_ \_ M<br/>            | 0xf08c<br/>   |
| lettera di movimento \_ \_ N<br/>            | 0xf08d<br/>   |
| lettera di movimento \_ \_ O<br/>            | 0xf08e<br/>   |
| lettera di movimento \_ \_ P<br/>            | 0xf08f<br/>   |
| lettera di movimento \_ \_ Q<br/>            | 0xf090<br/>   |
| lettera di movimento \_ \_ R<br/>            | 0xf091<br/>   |
| \_lettera movimento \_ S<br/>            | 0xf092<br/>   |
| lettera di movimento \_ \_ T<br/>            | 0xf093<br/>   |
| lettera di movimento \_ \_ U<br/>            | 0xf094<br/>   |
| lettera di movimento \_ \_ V<br/>            | 0xf095<br/>   |
| lettera di movimento \_ \_ W<br/>            | 0xf096<br/>   |
| lettera di movimento \_ \_ X<br/>            | 0xf097<br/>   |
| lettera di movimento \_ \_ Y<br/>            | 0xf098<br/>   |
| lettera di movimento \_ \_ Z<br/>            | 0xf099<br/>   |
| Numero di movimento \_ \_ 0<br/>             | 0xf09a<br/>   |
| Numero di movimento \_ \_ 1<br/>             | 0xf09b<br/>   |
| Numero di movimento \_ \_ 2<br/>             | 0xf09c<br/>   |
| Numero di movimento \_ \_ 3<br/>             | 0xf09d<br/>   |
| Numero di movimento \_ \_ 4<br/>             | 0xf09e<br/>   |
| Numero di movimento \_ \_ 5<br/>             | 0xf09f<br/>   |
| Numero di movimento \_ \_ 6<br/>             | 0xf0a0<br/>   |
| Numero di movimento \_ \_ 7<br/>             | 0xf0a1<br/>   |
| Numero di movimento \_ \_ 8<br/>             | 0xf0a2<br/>   |
| Numero di movimento \_ \_ 9<br/>             | 0xf0a3<br/>   |
| domanda di movimento \_<br/>             | 0xf0a5<br/>   |
| GESTO \_ acuto<br/>                | 0xf0a6<br/>   |
| \_dollaro movimento<br/>               | 0xf0a7<br/>   |
| \_asterisco movimento<br/>             | 0xf0a8<br/>   |
| GESTO \_ più<br/>                 | 0xf0a9<br/>   |
| \_doppio movimento \_<br/>           | 0xf0b8<br/>   |
| \_doppio movimento \_<br/>         | 0xf0b9<br/>   |
| GESTO \_ doppio \_ sinistro<br/>         | 0xf0ba<br/>   |
| doppio movimento a \_ \_ destra<br/>        | 0xf0bb<br/>   |
| MOVIMENTO \_ triplo \_<br/>           | 0xf0bc<br/>   |
| MOVIMENTO \_ tripla \_ giù<br/>         | 0xf0bd<br/>   |
| MOVIMENTO \_ tripla \_ sinistra<br/>         | 0xf0be<br/>   |
| MOVIMENTO \_ triplice a \_ destra<br/>        | 0xf0bf<br/>   |
| \_parentesi movimento \_ sopra<br/>        | 0xf0e4<br/>   |
| \_parentesi movimento \_ sotto<br/>       | 0xf0e5<br/>   |
| parentesi movimento a \_ \_ sinistra<br/>        | 0xf0e6<br/>   |
| parentesi movimento a \_ \_ destra<br/>       | 0xf0e7<br/>   |
| \_parentesi graffa di \_ movimento<br/>          | 0xf0e8<br/>   |
| \_parentesi graffa di movimento \_ in<br/>         | 0xf0e9<br/>   |
| parentesi graffa di movimento a \_ \_ sinistra<br/>          | 0xf0ea<br/>   |
| parentesi graffa di movimento a \_ \_ destra<br/>         | 0xf0eb<br/>   |
| \_tocco tripla \_ movimento<br/>          | 0xf0f2<br/>   |
| \_tocco a quattro movimenti \_<br/>            | 0xf0f3<br/>   |



 

 

 




