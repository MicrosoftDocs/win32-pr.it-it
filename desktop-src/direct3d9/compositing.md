---
description: L'applicazione può usare il buffer degli stencil per creare immagini 2D o 3D composite in una scena 3D.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Composizione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9dd6d11f98a5913c32d8f71385ce9b15ab5e7047c4db8394d5b0decee87f7f7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123388"
---
# <a name="compositing-direct3d-9"></a>Composizione (Direct3D 9)

L'applicazione può usare il buffer degli stencil per creare immagini 2D o 3D composite in una scena 3D. Una maschera nel buffer degli stencil viene usata per occludere un'area della superficie di destinazione di rendering. Le informazioni 2D archiviate, ad esempio testo o bitmap, possono quindi essere scritte nell'area occluded. In alternativa, l'applicazione può eseguire il rendering di primitive 3D aggiuntive nell'area con maschera stencil della superficie di destinazione del rendering. Può anche eseguire il rendering di un'intera scena.

I giochi spesso si uniscono più scene 3D. Ad esempio, i giochi di guida in genere visualizzano un mirror retrovisore. Il mirror contiene la vista della scena 3D dietro il driver. Si tratta essenzialmente di una seconda scena 3D composita con la visualizzazione in avanti del driver.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche del buffer degli stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



