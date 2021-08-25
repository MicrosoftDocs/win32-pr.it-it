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
ms.openlocfilehash: b1d30d0b33cbeb053e37f9e52c3948009a19692dbe1c53eedab9dfd6623726a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814791"
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

 

 