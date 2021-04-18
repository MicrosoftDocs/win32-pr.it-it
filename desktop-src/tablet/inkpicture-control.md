---
description: Argomento di riferimento per il controllo InkPicture per il Tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: Controllo InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded5295d48e4bb14b3c0d83713f33939a360cff4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/08/2021
ms.locfileid: "106316838"
---
# <a name="inkpicture-control"></a>Controllo InkPicture

Il controllo [InkPicture](inkpicture-control-reference.md) consente di inserire un'immagine (formato. jpg,. bmp,. png o. gif) in un'applicazione a cui gli utenti possono aggiungere input penna. È destinato agli scenari in cui l'input penna non deve essere riconosciuto come testo ma viene archiviato come input penna.

Gli utenti aggiungono input penna a un livello trasparente usando una penna. Gli utenti possono ridimensionare una finestra di [InkPicture](inkpicture-control-reference.md) senza perdere le informazioni sull'input penna, anche se l'input penna viene ritagliato durante il ridimensionamento.

Il controllo [InkPicture](inkpicture-control-reference.md) include il supporto di stampa di base. Tuttavia, è necessario implementare l'anteprima di stampa o altre funzionalità di stampa avanzate.

L'implementazione gestita (.NET Framework) di [InkPicture](/previous-versions/ms583740(v=vs.100)) eredita dalla classe [PictureBox](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1) .

Per impostazione predefinita, l'input penna viene colorato in nero se non è in modalità a contrasto elevato; in caso contrario, viene impostato sul valore dell'impostazione del colore di sistema corrente (colore \_ WINDOWTEXT). Inoltre, per impostazione predefinita, [**FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) è **false**.

All'interno del controllo [InkPicture](inkpicture-control-reference.md) , utilizzare l'oggetto [**Ink**](inkdisp-class.md) per caricare e salvare l'input penna.

> [!Note]  
> Quando si imposta [**EditingMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) su **Delete** o **Select**, vengono attivati altri eventi, ad esempio l'evento [**Stroke**](inkpicture-stroke.md) . Questi eventi sono utili se si desidera implementare modalità di eliminazione o selezione personalizzate.

 

Per informazioni di riferimento dettagliate sul controllo [InkPicture](inkpicture-control-reference.md) , vedere InkPicture.

Le sezioni seguenti illustrano in dettaglio l'uso del controllo [InkPicture](inkpicture-control-reference.md) :

-   [Uso delle immagini](working-with-pictures.md)
-   [Uso di InkPicture nelle versioni precedenti di Windows](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
