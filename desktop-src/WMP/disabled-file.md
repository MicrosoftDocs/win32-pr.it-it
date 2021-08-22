---
title: File disabilitato
description: File disabilitato
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Windows Media Player Skin per dispositivi mobili, file di grafica
- skins, file di grafica
- file per skin, art
- file di grafica per le skin, file disabilitati
- Windows Media Player Skin per dispositivi mobili,File disabilitati
- skins,File disabilitati
- File disabilitati nelle skin
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7b7d7c052ed0de1a3e231bc204b87a84f1e9e10262acfe43df310d76f76577b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997357"
---
# <a name="disabled-file"></a>File disabilitato

Il file Disabled contiene le immagini che verranno visualizzate quando non è possibile usare una funzione di pulsante specifica o lo stato di un pulsante è disattivato. Ad esempio, se è definita una  playlist vuota, verranno visualizzati i pulsanti Avanti e **Precedente** e dovranno essere visualizzati usando un'immagine disabilitata. Inoltre, per i pulsanti di attivazione/disattivazione, l'immagine Disabilitato viene usata per indicare che lo stato è disattivato.

L'immagine seguente è un tipico file disabilitato.

![file disabilitato](images/cesdkdis.png)

In questo modo vengono archiviate le immagini per i pulsanti di tipo hit disabilitati. Le immagini sono simili al file Sfondo, ma i colori sono più chiari. Usando l'offset definito nella sezione Bitmap del file di definizione dell'interfaccia, le immagini dei pulsanti sono allineate con l'immagine del file di sfondo.

Si noti che lo sfondo dell'immagine del pulsante corrisponde esattamente all'area corrispondente nel file di sfondo. Questo è importante, perché quando un pulsante di tipo hit non è disponibile, l'intero rettangolo definito per l'immagine disabilitata sostituirà l'area corrispondente nel file di sfondo. Mantenere l'immagine coerente con l'immagine di sfondo per assicurarsi che cambino effettivamente solo le parti del pulsante che si vuole visualizzare diversamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di grafica**](art-files-mobile.md)
</dt> </dl>

 

 




