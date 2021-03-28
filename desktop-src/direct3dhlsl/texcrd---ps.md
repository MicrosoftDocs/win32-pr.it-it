---
title: texcrd-PS
description: Copia i dati delle coordinate di trama dal registro iteratore delle coordinate di trama di origine come dati di colore nel registro di destinazione.
ms.assetid: b3330d70-6e18-4494-a01c-51f0a282e305
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e1b7bda7ab06c4af43eaa40393d2c5d64b09d9f4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104993400"
---
# <a name="texcrd---ps"></a>texcrd-PS

Copia i dati delle coordinate di trama dal registro iteratore delle coordinate di trama di origine come dati di colore nel registro di destinazione.

## <a name="syntax"></a>Sintassi



| texcrd DST, src |
|-----------------|



 

dove

-   DST è il registro di destinazione.
-   src è un registro di origine.

## <a name="remarks"></a>Commenti



| Versioni pixel shader | 1\_1 | 1\_2 | 1 \_ 3 | 1\_4 | 2 \_ 0 | 2 \_ x | 2 \_ SW | 3 \_ 0 | 3 \_ SW |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| texcrd                |      |      |      | x    |      |      |       |      |       |



 

Questa istruzione interpreta i dati delle coordinate come dati di colore (RGBA).

Questa istruzione non consente di campionare alcuna trama. Sono rilevanti solo le coordinate di trama impostate in questa fase della trama.

Quando si usa texcrd, tenere presente i dettagli seguenti sulla modalità di copia dei dati dal registro di origine al registro di destinazione. Il registro delle coordinate di trama di origine (t \# ) include i dati nell'intervallo \[ -D3DCAPS9. MaxTextureRepeat, D3DCAPS9. MaxTextureRepeat \] , mentre il registro di destinazione (r \# ) può conservare i dati solo nell'intervallo (probabilmente inferiore) \[ -D3DCAPS9. PixelShader1xMaxValue, D3DCAPS9. PixelShader1xMaxValue \] . Si noti che per pixel shader versione \_ 4 D3DCAPS9. PixelShader1xMaxValue deve essere un minimo di otto. È probabile che l'istruzione texcrd, nel processo di blocco dei dati di origine non compreso nell'intervallo del registro di destinazione, si comporti in modo diverso su hardware diverso. Il primo hardware pixel shader versione 1 \_ 4 sul mercato eseguirà un morsetto speciale per i valori non compresi nell'intervallo. Questo morsetto è stato progettato per produrre un numero che può essere inserito nel registro di destinazione, ma anche per mantenere il comportamento di indirizzamento della trama per i dati fuori intervallo (vedere [**D3DTEXTUREADDRESS**](/windows/desktop/direct3d9/d3dtextureaddress)) se i dati devono essere usati successivamente per il campionamento di trama. Tuttavia, un nuovo hardware di produttori diversi potrebbe non presentare questo comportamento e potrebbe solo tagliare i dati per adattarsi all'intervallo di registro di destinazione. Pertanto, il modo più sicuro di agire quando si usa pixel shader versione 1 \_ 4 texcrd è fornire i dati delle coordinate di trama solo nel pixel shader che è già compreso nell'intervallo \[ -8, 8, in \] modo da non basarsi sul modo in cui i morsetti hardware vengono usati.

A differenza \_ di TEXCOORD, texcrd non blocca i valori compresi tra 0 e 1.

Regole per l'uso di texcrd:

1.  Lo stesso modificatore. xyz o. XYW deve essere applicato a ogni lettura di un singolo registro t (n) in un'istruzione texcrd o texld.
2.  Il quarto risultato del canale di texcrd viene annullato o non definito in tutti i casi.
3.  Il terzo canale non è definito o non è definito per il \_ case XYW DW.

## <a name="examples"></a>Esempio

Di seguito è riportato il set completo di sintassi consentita per texcrd, che tiene conto di tutte le combinazioni di modificatori di origine valide e di una maschera di scrittura di destinazione. Si noti che la notazione. RGBA e. xyzw può essere usata in modo interscambiabile.

Copia i primi tre canali del registro iteratore delle coordinate di trama, t (n), in r (m). Il quarto canale di r (m) non è inizializzato.


```
texcrd  r(m).rgb, t(n).xyz  

// Produces the same result as the previous instruction
texcrd  r(m).rgb, t(n)
```



Inserisce il primo, il secondo e il quarto componente di t (n) nei primi tre canali di r (m). Il quarto canale di r (m) non è inizializzato.


```
texcrd  r(m).rgb, t(n).xyw
```



Di seguito è riportato un esempio di suddivisione proiettiva usando il \_ modificatore DW.

Questo esempio copia x/w e y/w da t (n) nei primi due canali di r (m). Il terzo e il quarto canale di r (m) non sono inizializzati. Tutti i dati scritti in precedenza nel terzo canale di r (m) andranno perduti. I dati nel quarto canale di r (m) andranno perduti a causa del marcatore di fase. Per la versione 1 \_ 4, il \_ flag D3DTTFF proiettato viene ignorato.


```
texcrd  r(m).rg,  t(n)_dw.xyw
```



## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Istruzioni pixel shader](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 