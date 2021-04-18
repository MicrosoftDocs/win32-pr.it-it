---
description: Il comportamento predefinito per il controllo InkEdit consiste nel riconoscere e convertire l'input penna in testo dopo la scadenza di un breve timeout.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Visualizzazione di input penna come input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3aca1d6a1a4700d996d65a9cfd7d62e6b27e1c71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316856"
---
# <a name="displaying-ink-as-ink"></a>Visualizzazione di input penna come input penna

Il comportamento predefinito per il controllo [InkEdit](inkedit-control-reference.md) consiste nel riconoscere e convertire l'input penna in testo dopo la scadenza di un breve timeout. Poiché il controllo è una superclasse di [RichEdit](../controls/rich-edit-controls.md), è anche possibile incorporare e visualizzare l'input penna all'interno del controllo. Ogni parola viene inserita nel controllo come oggetto [**InkDisp**](inkdisp-class.md) . L'oggetto **InkDisp** contiene l'input penna e le relative alternative di riconoscimento.

Quando viene inserita, l'input penna viene ridimensionato in modo da aumentare le dimensioni del carattere corrente e vengono applicate altre proprietà di ambiente, ad esempio corsivo o grassetto. Se l'utente sceglie di modificare il testo di un oggetto [**InkDisp**](inkdisp-class.md) , deve prima convertire l'input penna in testo.

> [!Note]  
> Tutti i dati alternativi di input penna e riconoscimento vengono persi durante la conversione.

 

Questa funzionalità è disponibile solo nei computer che eseguono Microsoft Windows XP Tablet PC Edition, Windows Vista o versioni successive.

 

 
