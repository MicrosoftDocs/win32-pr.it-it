---
description: Questa sezione elenca un problema che può verificarsi quando si usano le finestre del dispositivo nelle applicazioni Direct3D.
ms.assetid: 7cfd2ad6-fb85-4303-9fa4-6fe7d16d9951
title: Uso di Windows Device (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56352ef0ec66def620a0ae0995d92d8b421722e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303794"
---
# <a name="working-with-device-windows-direct3d-9"></a>Uso di Windows Device (Direct3D 9)

Questa sezione elenca un problema che può verificarsi quando si usano le finestre del dispositivo nelle applicazioni Direct3D.

-   Direct3D associa solo le finestre di stato attivo invece della finestra del dispositivo con la funzione di elaborazione dei messaggi Direct3D e elabora solo i messaggi della finestra di stato attivo. Quindi, la finestra di attivazione deve essere l'elemento padre di qualsiasi finestra del dispositivo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Suggerimenti per la programmazione](programming-tips.md)
</dt> </dl>

 

 



