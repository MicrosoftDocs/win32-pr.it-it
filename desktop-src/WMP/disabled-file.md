---
title: File disabilitato
description: File disabilitato
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Interfacce di Windows Media Player per dispositivi mobili, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di immagine per le interfacce, file disabilitati
- Windows Media Player Mobile Skins, file disabilitati
- interfacce, file disabilitati
- File disabilitati nelle interfacce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9608c67ded6625d46126955ad42a24548a9d002c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104044964"
---
# <a name="disabled-file"></a>File disabilitato

Il file disabilitato contiene le immagini che verranno visualizzate quando non è possibile usare una funzione di pulsante particolare o lo stato di un pulsante è disattivato. Se, ad esempio, viene definita una playlist vuota, i pulsanti **Avanti** e **indietro** verranno visualizzati e devono essere visualizzati usando un'immagine disabilitata. Inoltre, per i pulsanti di attivazione, l'immagine disabilitata viene utilizzata per indicare che lo stato è disattivato.

L'immagine seguente è un file disabilitato tipico.

![file disabilitato](images/cesdkdis.png)

Archivia le immagini per i pulsanti di tipo hit che sono disabilitati. Le immagini sono simili al file in background, ma i colori sono più chiari. Utilizzando l'offset definito nella sezione bitmap del file di definizione della pelle, le immagini dei pulsanti si allineano con l'immagine del file di sfondo.

Si noti che lo sfondo dell'immagine del pulsante corrisponde esattamente all'area corrispondente nel file in background. Questo è importante, poiché quando un pulsante di tipo hit non è disponibile, l'intero rettangolo definito per l'immagine disabilitata sostituirà l'area corrispondente nel file in background. Mantenere la grafica coerente con l'immagine di sfondo per assicurarsi che solo le parti del pulsante che si desidera visualizzare diverse cambieranno effettivamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di immagine**](art-files-mobile.md)
</dt> </dl>

 

 




