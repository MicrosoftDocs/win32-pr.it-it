---
title: Errore di disegno D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Una chiamata di disegno da parte di una destinazione di rendering non è riuscita
keywords:
- Errore di disegno D1109 Direct2D
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 09d84f549b2361d2753ac40650ce057de9e4f84c
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549966"
---
# <a name="d1109-draw-failure"></a>D1109: Errore di disegno

Una chiamata di disegno da parte di una risorsa di destinazione di rendering non \[ *è riuscita.* \] Tag1 \[ , *tag2* \] .

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*Risorsa*
</dt> <dd>

Indirizzo della destinazione di rendering.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

Il primo valore del tag (per [**altre informazioni, vedere SetTags).**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

Il secondo valore del tag (per [**altre informazioni, vedere SetTags).**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags)

</dd> </dl> 

| &nbsp;      |  &nbsp; |
|-------------|---------|
| Livello di errore | Avviso |



 

## <a name="possible-causes"></a>Possibili cause

Esistono molti motivi per cui una chiamata di disegno potrebbe non riuscire. Per altre informazioni, vedere la documentazione di Direct2D SDK per il metodo che ha avuto esito negativo.

 

 