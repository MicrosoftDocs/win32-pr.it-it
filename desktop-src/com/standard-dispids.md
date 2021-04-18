---
title: DISPID standard
description: Per la specifica dei controlli è stato definito un numero di DISPID standard.
ms.assetid: f938b64f-5d45-40e7-ad02-665ce9c86a70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 657a7cd12ac92504bb5d63dcd486b6a45da47310
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "106297999"
---
# <a name="standard-dispids"></a>DISPID standard

Per la specifica dei controlli è stato definito un numero di DISPID standard.

## <a name="dispid_mousepointer"></a>DISPID \_ MOUSEPOINTER

Proprietà di tipo Integer.

``` syntax
#define DISPID_MOUSEPOINTER            -521
```

La proprietà MousePointer identifica le icone del mouse standard.



| Valore         | Descrizione                                                                |
|---------------|----------------------------------------------------------------------------|
| 0<br/>  | Predefinita Forma determinata dall'oggetto.<br/>                       |
| 1<br/>  | Freccia<br/>                                                           |
| 2<br/>  | Cross (puntatore tra i capelli)<br/>                                      |
| 3<br/>  | Beam I<br/>                                                          |
| 4<br/>  | Icona (quadrato piccolo all'interno di un quadrato)<br/>                             |
| 5<br/>  | Size (freccia a quattro punte che punta a nord, Sud, est e ovest)<br/> |
| 6<br/>  | Size NE SW (doppia freccia che indica nordest e sud-ovest)<br/>      |
| 7<br/>  | Size N S (doppia freccia che punta verso nord e Sud)<br/>                |
| 8<br/>  | Dimensioni NW, SE<br/>                                                     |
| 9<br/>  | Size E W (doppia freccia che punta verso est e ovest)<br/>                  |
| 10<br/> | Freccia SU<br/>                                                        |
| 11<br/> | Clessidra (attesa)<br/>                                                |
| 12<br/> | Nessuna eliminazione<br/>                                                         |
| 13<br/> | Freccia e clessidra<br/>                                             |
| 14<br/> | Freccia e punto interrogativo<br/>                                         |
| 15<br/> | Ridimensiona tutto<br/>                                                        |
| 99<br/> | Icona personalizzata specificata dalla proprietà MouseIcon<br/>                 |



 

## <a name="dispid_mouseicon"></a>DISPID \_ MOUSEICON

Proprietà di tipo immagine.

``` syntax
#define DISPID_MOUSEICON               -522
```

## <a name="dispid_picture"></a>\_immagine DISPID

Proprietà di tipo immagine.

``` syntax
#define DISPID_PICTURE                 -523
```

## <a name="dispid_valid"></a>DISPID \_ valido

Utilizzato per determinare se il controllo dispone o meno di dati validi.

Proprietà di tipo BOOL.

``` syntax
#define DISPID_VALID                   -524
```

## <a name="dispid_-ambient_palette"></a>\_ \_ tavolozza ambiente DISPID

Usato per consentire al controllo di ottenere il HPAL del contenitore. Se il contenitore fornisce una tavolozza di ambiente, si tratta dell'unica tavolozza che può essere realizzata in primo piano. I controlli che vogliono realizzare le proprie tavolozze devono eseguire questa operazione in background. Se non è presente alcuna tavolozza di ambiente fornita dal contenitore, il controllo attivo può realizzare la relativa tavolozza in primo piano. La gestione della tavolozza viene ulteriormente discussa nel comportamento della tavolozza per i controlli OLE presenti in ActiveX SDK.

``` syntax
#define DISPID_AMBIENT_PALETTE         -726
```

 

 





