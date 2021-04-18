---
description: L'applicazione può usare il buffer dello stencil per le immagini 2D o 3D composite su una scena 3D.
ms.assetid: 9233d15d-fa99-41a2-a253-22f5ae5bf788
title: Composizione (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01bca61559d2773bd1e4f7dc345e9ad4c1fb6fcb
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "106305306"
---
# <a name="compositing-direct3d-9"></a>Composizione (Direct3D 9)

L'applicazione può usare il buffer dello stencil per le immagini 2D o 3D composite su una scena 3D. Una maschera nel buffer dello stencil viene utilizzata per occludere un'area della superficie di destinazione del rendering. Le informazioni 2D archiviate, ad esempio testo o bitmap, possono quindi essere scritte nell'area. In alternativa, l'applicazione è in grado di eseguire il rendering di primitive 3D nell'area mascherata dallo stencil della superficie di destinazione per il rendering. È anche possibile eseguire il rendering di un'intera scena.

I giochi spesso compostano contemporaneamente più scene 3D. Ad esempio, per la guida dei giochi viene in genere visualizzato un mirror di visualizzazione posteriore. Il mirror contiene la visualizzazione della scena 3D dietro il driver. Si tratta essenzialmente di una seconda scena 3D composita con la visualizzazione in diretta del driver.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Tecniche del buffer dello stencil](stencil-buffer-techniques.md)
</dt> </dl>

 

 



