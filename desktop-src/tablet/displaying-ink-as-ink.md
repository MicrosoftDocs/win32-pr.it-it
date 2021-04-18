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
# <a name="displaying-ink-as-ink"></a><span data-ttu-id="906f5-103">Visualizzazione di input penna come input penna</span><span class="sxs-lookup"><span data-stu-id="906f5-103">Displaying Ink as Ink</span></span>

<span data-ttu-id="906f5-104">Il comportamento predefinito per il controllo [InkEdit](inkedit-control-reference.md) consiste nel riconoscere e convertire l'input penna in testo dopo la scadenza di un breve timeout.</span><span class="sxs-lookup"><span data-stu-id="906f5-104">The default behavior for the [InkEdit](inkedit-control-reference.md) control is to recognize and convert ink into text after a brief timeout has expired.</span></span> <span data-ttu-id="906f5-105">Poiché il controllo è una superclasse di [RichEdit](../controls/rich-edit-controls.md), è anche possibile incorporare e visualizzare l'input penna all'interno del controllo.</span><span class="sxs-lookup"><span data-stu-id="906f5-105">Because the control is a superclass of [RichEdit](../controls/rich-edit-controls.md), it is also possible to embed and display ink within the control.</span></span> <span data-ttu-id="906f5-106">Ogni parola viene inserita nel controllo come oggetto [**InkDisp**](inkdisp-class.md) .</span><span class="sxs-lookup"><span data-stu-id="906f5-106">Each word is inserted into the control as an [**InkDisp**](inkdisp-class.md) object.</span></span> <span data-ttu-id="906f5-107">L'oggetto **InkDisp** contiene l'input penna e le relative alternative di riconoscimento.</span><span class="sxs-lookup"><span data-stu-id="906f5-107">The **InkDisp** object contains the ink and its recognition alternates.</span></span>

<span data-ttu-id="906f5-108">Quando viene inserita, l'input penna viene ridimensionato in modo da aumentare le dimensioni del carattere corrente e vengono applicate altre proprietà di ambiente, ad esempio corsivo o grassetto.</span><span class="sxs-lookup"><span data-stu-id="906f5-108">When inserted, the ink is scaled to the current font size and other ambient properties, such as italics or bold, are applied.</span></span> <span data-ttu-id="906f5-109">Se l'utente sceglie di modificare il testo di un oggetto [**InkDisp**](inkdisp-class.md) , deve prima convertire l'input penna in testo.</span><span class="sxs-lookup"><span data-stu-id="906f5-109">If the user chooses to edit the text of an [**InkDisp**](inkdisp-class.md) object, he or she must first convert the ink to text.</span></span>

> [!Note]  
> <span data-ttu-id="906f5-110">Tutti i dati alternativi di input penna e riconoscimento vengono persi durante la conversione.</span><span class="sxs-lookup"><span data-stu-id="906f5-110">All ink and recognition alternate data is lost during the conversion.</span></span>

 

<span data-ttu-id="906f5-111">Questa funzionalità è disponibile solo nei computer che eseguono Microsoft Windows XP Tablet PC Edition, Windows Vista o versioni successive.</span><span class="sxs-lookup"><span data-stu-id="906f5-111">This feature is available only on computers that run Microsoft Windows XP Tablet PC Edition, Windows Vista, or later.</span></span>

 

 
