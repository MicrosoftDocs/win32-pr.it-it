---
title: File con push
description: File con push
ms.assetid: bea803d2-1237-4983-9673-afdcddc32748
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, file con push
- Windows Media Player Mobile Skins, file con push
- interfacce, file con push
- Push dei file nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 071a6a4fd00eee7040d2fadb8fb80db343dc0ac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104396150"
---
# <a name="pushed-file"></a>File con push

Il file inserito contiene le immagini che verranno visualizzate quando l'utente tocca un pulsante. È anche possibile includere le immagini normale e push per lo stato di sospensione del pulsante come playpause.

L'immagine seguente è un file di cui è stato eseguito il push tipico.

![file con push](images/cesdkpus.png)

Archivia le immagini che verranno visualizzate quando si toccano i pulsanti di tipo hit. Inoltre, archiviate in questo file sono le immagini normali e push per l'immagine sospesa del pulsante come playpause. Ad eccezione delle immagini secondarie di come playpause a destra, le altre immagini dei pulsanti si allineano con l'immagine di sfondo, usando l'offset definito nella sezione bitmap del file di definizione dell'interfaccia personalizzata.

Si noti che lo sfondo dell'immagine del pulsante corrisponde esattamente all'area corrispondente nel file in background. Questo è importante perché quando l'utente tocca un pulsante di tipo hit, l'intero rettangolo definito per l'immagine push sostituisce l'area corrispondente nel file in background. Mantenere la grafica coerente con l'immagine di sfondo per assicurarsi che solo le parti del pulsante che si desidera visualizzare diverse cambieranno effettivamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di immagine**](art-files-mobile.md)
</dt> </dl>

 

 




