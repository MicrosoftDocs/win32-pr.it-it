---
title: DISPID standard
description: Per la specifica dei controlli sono stati definiti diversi dispid standard.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af35ce4e4cad884b54bb0982037721608364a0249d3be6dd566f3aac766bb1f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129783"
---
# <a name="standard-dispids"></a>DISPID standard

Per la specifica dei controlli sono stati definiti diversi dispid standard.

## <a name="dispid_mousepointer"></a>DISPID \_ MOUSEPOINTER

Proprietà di tipo integer.

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

La proprietà Mousepointer identifica le icone standard del mouse.



| Valore         | Descrizione                                                                |
|---------------|----------------------------------------------------------------------------|
| 0<br/>  | (Impostazione predefinita) Forma determinata dall'oggetto .<br/>                       |
| 1<br/>  | Freccia<br/>                                                           |
| 2<br/>  | Cross (puntatore a forma di croce)<br/>                                      |
| 3<br/>  | I Beam<br/>                                                          |
| 4<br/>  | Icona (piccolo quadrato all'interno di un quadrato)<br/>                             |
| 5<br/>  | Dimensioni (freccia a quattro punte che punta a nord, sud, est e ovest)<br/> |
| 6<br/>  | Dimensioni NE SW (doppia freccia che punta a nord-est e sud-ovest)<br/>      |
| 7<br/>  | Dimensioni N S (doppia freccia che punta a nord e sud)<br/>                |
| 8<br/>  | Dimensioni NW, edizione Standard<br/>                                                     |
| 9<br/>  | Dimensione E W (doppia freccia che punta a est e a ovest)<br/>                  |
| 10<br/> | Freccia SU<br/>                                                        |
| 11<br/> | Hourglass (attesa)<br/>                                                |
| 12<br/> | Nessuna eliminazione<br/>                                                         |
| 13<br/> | Freccia e clessidra<br/>                                             |
| 14<br/> | Freccia e punto interrogativo<br/>                                         |
| 15<br/> | Ridimensiona tutto<br/>                                                        |
| 99<br/> | Icona personalizzata specificata dalla proprietà MouseIcon<br/>                 |



 

## <a name="dispid_mouseicon"></a>DISPID \_ MOUSEICON

Proprietà di tipo picture.

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a>IMMAGINE \_ DISPID

Proprietà di tipo picture.

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a>DISPID \_ VALIDO

Utilizzato per determinare se il controllo dispone o meno di dati validi.

Proprietà di tipo BOOL.

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a>RIQUADRO DI AMBIENTE \_ DISPID \_

Usato per consentire al controllo di ottenere hpAL del contenitore. Se il contenitore fornisce un riquadro ambiente, questa è l'unica tavolozza che può essere realizzata in primo piano. I controlli che vogliono realizzare le proprie tavolozze devono eseguire questa operazione in background. Se il contenitore non ha alcun riquadro di ambiente, il controllo attivo può realizzare la tavolozza in primo piano. La gestione del riquadro è descritta più avanti in Comportamento del riquadro per i controlli OLE, disponibile in ActiveX SDK.

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





