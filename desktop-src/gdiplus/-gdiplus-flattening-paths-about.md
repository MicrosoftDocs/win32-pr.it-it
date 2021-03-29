---
description: Un oggetto GraphicsPath archivia una sequenza di linee e B&\# 233; Zier spline.
ms.assetid: 8ce77146-dc28-4c0b-bcf0-dad4bf3d86e8
title: Percorsi Flat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7caee9b8d760d9702b6a3ea7711090f001a57912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104987712"
---
# <a name="flattening-paths"></a>Percorsi Flat

Un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) archivia una sequenza di linee e spline di Bézier. È possibile aggiungere diversi tipi di curve (ellissi, archi, spline cardinali) a un tracciato, ma ogni curva viene convertita in una spline di Bézier prima di essere archiviata nel percorso. L'appiattimento di un tracciato è costituito dalla conversione di ogni spline di Bézier nel percorso a una sequenza di linee rette.

Per rendere flat un tracciato, chiamare il metodo [**GraphicsPath:: Flat**](/windows/desktop/api/Gdipluspath/nf-gdipluspath-graphicspath-flatten) di un oggetto [**GraphicsPath**](/windows/desktop/api/gdipluspath/nl-gdipluspath-graphicspath) . Il metodo **GraphicsPath:: Flat** riceve un argomento flat che specifica la distanza massima tra il percorso bidimensionale e il percorso originale. Nella figura seguente viene illustrato un percorso prima e dopo l'appiattimento.

![illustrazione che mostra una sequenza di spline di Bezier connesse in blu e le righe corrispondenti in rosso](images/aboutgdip02-art32a.png)

 

 



