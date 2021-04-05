---
title: Errore di D1109
ms.assetid: 76154839-719e-4c73-a80e-f9216f3468e3
description: Una chiamata di disegnare da una destinazione di rendering non è riuscita
keywords:
- Direct2D errore di D1109 di estrazione
topic_type:
- apiref
api_name:
- D1109 Draw Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4b08dfb99d49dcb447443685e1fbfa01a2cbad1c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "103730079"
---
# <a name="d1109-draw-failure"></a>D1109: errore di estrazione

Una chiamata di disegnare da una risorsa di destinazione di rendering non riuscita \[  \] . Tag \[ *tag1*, *Tag2* \] .

## <a name="placeholders"></a>Segnaposto

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*risorse*
</dt> <dd>

Indirizzo della destinazione di rendering.

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

Il primo valore del tag (per ulteriori informazioni, vedere la pagina relativa ai [**tag**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*Tag2*
</dt> <dd>

Il secondo valore del tag (per ulteriori informazioni, vedere la pagina relativa ai [**tag**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) ).

</dd> </dl> 

|             |         |
|-------------|---------|
| Livello di errore | Avviso |



 

## <a name="possible-causes"></a>Possibili cause

Esistono molti motivi per cui una chiamata di un progetto potrebbe non riuscire. Per ulteriori informazioni, vedere la documentazione di Direct2D SDK per il metodo che ha avuto esito negativo.

 

 