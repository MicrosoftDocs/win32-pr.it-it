---
title: Formati di file di immagine
description: Formati di file di immagine
ms.assetid: 803479e8-0e00-4724-80b7-9d86709c43db
keywords:
- Interfacce di Media Player di Windows, file di immagine
- interfacce, file di immagine
- file per Skins, Art
- file di grafica per interfacce, formati di file
- Windows Media Player Skin, formati di file per l'arte
- interfacce, formati di file per l'arte
- formati di file per l'arte personalizzata
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a35af72fd502cb23e81063fe9513b4a9311f9557
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 09/16/2019
ms.locfileid: "104332436"
---
# <a name="art-file-formats"></a>Formati di file di immagine

I formati di file di immagine seguenti sono riconosciuti da Windows Media Player per le interfacce:



| Formato                                  | Estensione   | Descrizione                                                                                        |
|-----------------------------------------|-------------|----------------------------------------------------------------------------------------------------|
| Bitmap                                  | bmp        | Le immagini bitmap sono consigliate perché offrono il massimo controllo sull'immagine e sui colori esatti. |
| Graphics Interchange Format (GIF)       | gif        | Formato di immagine compresso usato per le pagine Web. Sono supportate le gif animate.                            |
| Joint Photographic Experts Group (JPEG) | .jpeg, .jpg | Formato di immagine compresso usato per le pagine Web.                                                         |
| Portable Network Graphics (PNG)         | png        | Formato di immagine compresso usato per le pagine Web.                                                         |



 

Se si usa uno dei formati di file compressi che definisce un colore come trasparente per un Web browser, non definire un colore come trasparente nel file di immagine. Usare un colore visibile per rappresentare le aree trasparenti nell'immagine e quindi definire il colore come trasparente nel file di definizione dell'interfaccia. Se, ad esempio, si crea un file GIF con alcune aree trasparenti, questi non saranno trasparenti nell'immagine finale e non sarà possibile usare il colore impostato come trasparente nel file gif per il colore della trasparenza nell'interfaccia.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[**File di immagine**](art-files.md)
</dt> </dl>

 

 




