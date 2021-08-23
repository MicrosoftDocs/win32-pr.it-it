---
title: texcrd - ps
description: Copia i dati delle coordinate della trama dal registro dell'iteratore delle coordinate della trama di origine come dati di colore nel registro di destinazione.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 795dacbec01abdfa49527e36fefc9194a6168a99c1d9ab425b30f987e5445096
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118506427"
---
# <a name="texcrd---ps"></a>texcrd - ps

Copia i dati delle coordinate della trama dal registro dell'iteratore delle coordinate della trama di origine come dati di colore nel registro di destinazione.

## <a name="syntax"></a>Sintassi



| texcrd dst, src |
|-----------------|



 

dove

-   dst è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ sw | 3 \_ 0 | 3 \_ sw |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcrd                |      |      |      | x    |      |      |       |      |       |



 

Questa istruzione interpreta i dati delle coordinate come dati di colore (RGBA).

Nessuna trama viene campionata da questa istruzione. Sono rilevanti solo le coordinate di trama impostate in questa fase della trama.

Quando si usa texcrd, tenere presente i dettagli seguenti sulla modalità di copia dei dati dal registro di origine al registro di destinazione. Il registro delle coordinate della trama di origine (t \# ) contiene i dati nell'intervallo \[ -D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat , mentre il registro di destinazione (r ) può contenere i dati solo nell'intervallo (probabilmente più \] \# piccolo) \[ -D3DCAPS9. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] . Si noti che per pixel shader versione \_ 1 4, D3DCAPS9. PixelShader1xMaxValue deve essere almeno otto. È probabile che l'istruzione texcrd, nel processo di blocco dei dati di origine non compreso nell'intervallo del registro di destinazione, si comporti in modo diverso su hardware diverso. Il primo pixel shader hardware della versione 1 4 sul mercato eseguirà una speciale chiusura per \_ i valori non compreso nell'intervallo. Questo elemento è progettato per produrre un numero che può rientrare nel registro di destinazione, ma anche per mantenere il comportamento di indirizzamento della trama per i dati non in intervallo (vedere [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) se i dati dovevano essere usati successivamente per il campionamento delle trame. Tuttavia, il nuovo hardware di produttori diversi potrebbe non presentare questo comportamento e potrebbe semplicemente contenere dati adatti all'intervallo di registri di destinazione. Pertanto, il corso di azione più sicuro quando si usa pixel shader versione 1 4 texcrd consiste nell'fornire i dati delle coordinate della trama solo nel pixel shader che è già compreso nell'intervallo \_ \[ -8,8 in modo da non basarsi sul modo in cui i requisiti \] hardware.

A differenza di texcoord, \_ texcrd non stringe valori compresi tra 0 e 1.

Regole per l'uso di texcrd:

1.  Lo stesso modificatore .xyz o .xyw deve essere applicato a ogni lettura di un singolo registro t(n) all'interno di un'istruzione texcrd o texld.
2.  Il quarto risultato del canale di texcrd non è impostato/non definito in tutti i casi.
3.  Il terzo canale non è impostato/non definito per il caso xyw \_ dw.

## <a name="examples"></a>Esempio

Di seguito è riportato il set completo di sintassi consentite per texcrd, tenendo conto di tutte le combinazioni valide di modificatore/selettore di origine e maschera di scrittura di destinazione. Si noti che la notazione .rgba e .xyzw può essere usata in modo intercambiabile.

Copia i primi tre canali del registro dell'iteratore delle coordinate di trama, t(n), in r(m). Il quarto canale di r(m) non è inizializzato.


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



Inserisce il primo, il secondo e il quarto componente di t(n) nei primi tre canali di r(m). Il quarto canale di r(m) non è inizializzato.


```
texcrd  r(m).rgb, t(n).xyw
```



Di seguito è riportato un esempio di divisione proiettata che usa il \_ modificatore dw.

Questo esempio copia x/w e y/w da t(n) nei primi due canali di r(m). Il terzo e il quarto canale di r(m) non sono inizializzati. Tutti i dati scritti in precedenza nel terzo canale di r(m) andranno persi. I dati nel quarto canale di r(m) vengono persi a causa del marcatore di fase. Per la versione \_ 1 4, il flag D3DTTFF \_ PROJECTED viene ignorato.


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni per pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 