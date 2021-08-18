---
description: Il comportamento predefinito per il controllo InkEdit è riconoscere e convertire l'input penna in testo dopo la scadenza di un breve timeout.
ms.assetid: d141bcec-e9a8-48b8-86cf-9476a2cc6f9f
title: Visualizzazione dell'input penna come input penna
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de038df5c1b7e43f90ea02edc166039d606fe56761c96a47508714fd94ed6530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119709471"
---
# <a name="displaying-ink-as-ink"></a>Visualizzazione dell'input penna come input penna

Il comportamento predefinito per il [controllo InkEdit](inkedit-control-reference.md) è riconoscere e convertire l'input penna in testo dopo la scadenza di un breve timeout. Poiché il controllo è una superclasse di [RichEdit](../controls/rich-edit-controls.md), è anche possibile incorporare e visualizzare l'input penna all'interno del controllo. Ogni parola viene inserita nel controllo come [**oggetto InkDisp.**](inkdisp-class.md) **L'oggetto InkDisp** contiene l'input penna e le relative alternative di riconoscimento.

Quando viene inserito, l'input penna viene ridimensionato in base alle dimensioni correnti del carattere e vengono applicate altre proprietà di ambiente, ad esempio il corsivo o il grassetto. Se l'utente sceglie di modificare il testo di un [**oggetto InkDisp,**](inkdisp-class.md) deve prima convertire l'input penna in testo.

> [!Note]  
> Tutti i dati alternativi di input penna e riconoscimento vengono persi durante la conversione.

 

Questa funzionalità è disponibile solo nei computer che eseguono Microsoft Windows XP Tablet PC Edition, Windows Vista o versioni successive.

 

 
