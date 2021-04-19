---
title: Identificatori del tipo di spazio colore
description: Queste costanti specificano il tipo di una matrice di spazi dei colori PostScript 2. I valori seguenti sono tipi di matrice di spazi dei colori validi.
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 02/02/2021
ms.locfileid: "106320181"
---
# <a name="color-space-type-identifiers"></a>Identificatori del tipo di spazio colore

Queste costanti specificano il tipo di una matrice di spazi dei colori PostScript 2. I valori seguenti sono tipi di matrice di spazi dei colori validi.

<dl> <dt>

<span id="CSA_A"></span><span id="csa_a"></span>**\_A CSA**
</dt> <dd> <dl> <dt>



Ottiene una matrice di spazi dei colori CIEBasedA dal profilo monocromatico.


</dt> </dl> </dd> <dt>

<span id="CSA_GRAY"></span><span id="csa_gray"></span>**\_grigio CSA**
</dt> <dd> <dl> <dt>



Ottiene una matrice di spazi dei colori CIEBasedA dal profilo monocromatico.


</dt> </dl> </dd> <dt>

<span id="CSA_ABC"></span><span id="csa_abc"></span>**\_ABC CSA**
</dt> <dd> <dl> <dt>



Ottenere una matrice di spazi dei colori CIEBasedABC dal profilo RGB o L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEF"></span><span id="csa_def"></span>**DEF. CSA \_**
</dt> <dd> <dl> <dt>



Ottenere una matrice di spazi dei colori CIEBasedDEF dal profilo RGB o L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_RGB"></span><span id="csa_rgb"></span>**\_RGB CSA**
</dt> <dd> <dl> <dt>



Ottiene una matrice di spazi dei colori CIEBasedDEF seguita da una matrice di spazi dei colori CIEBasedABC dal profilo RGB. In caso di esecuzione, se la stampante non supporta spazi dei colori CIEBasedDEF, la funzione utilizza la definizione CIEBasedABC.


</dt> </dl> </dd> <dt>

<span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**\_Laboratorio CSA**
</dt> <dd> <dl> <dt>



Ottiene una matrice di spazi dei colori CIEBasedABC dal <sup>\*</sup> profilo L a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEFG"></span><span id="csa_defg"></span>**\_defg CSA**
</dt> <dd> <dl> <dt>



Ottiene una matrice di spazi dei colori CIEBasedDEFG dal profilo CMYK.


</dt> </dl> </dd> <dt>

<span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**\_CMYK CSA**
</dt> <dd> <dl> <dt>



Ottiene una matrice di spazi dei colori CIEBasedCMYK dal profilo CMYK.


</dt> </dl> </dd> </dl>

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[Concetti di base sulla gestione dei colori](basic-color-management-concepts.md)
</dt> <dt>

[Costanti ICM](wcs-constants.md)
</dt> </dl>

 

 




