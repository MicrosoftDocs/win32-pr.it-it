---
description: Argomento di riferimento per il controllo InkPicture per Tablet PC.
ms.assetid: 1ced9779-dae5-4f9a-8a68-b2c0d041d5b4
title: Controllo InkPicture
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef9cb4b5e1919e111e84cc6b654b56b14eff93cfb5aedacc15400fb3ef1af07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118451100"
---
# <a name="inkpicture-control"></a>Controllo InkPicture

Il [controllo InkPicture](inkpicture-control-reference.md) consente di inserire un'immagine (formato .jpg, .bmp, .png o .gif) in un'applicazione a cui gli utenti possono aggiungere input penna. È destinato a scenari in cui l'input penna non deve essere riconosciuto come testo, ma viene archiviato come input penna.

Gli utenti aggiungono input penna a un livello trasparente usando una penna. Gli utenti possono ridimensionare una [finestra InkPicture](inkpicture-control-reference.md) senza perdere informazioni sull'input penna, anche se l'input penna viene ritagliato durante il ridimensionamento.

Il [controllo InkPicture](inkpicture-control-reference.md) include il supporto di stampa di base. Tuttavia, è necessario implementare l'anteprima di stampa o altre funzionalità di stampa avanzate.

L'implementazione gestita (.NET Framework) di [InkPicture](/previous-versions/ms583740(v=vs.100)) eredita dalla [classe PictureBox.](/dotnet/api/system.windows.forms.picturebox?view=netcore-3.1)

Per impostazione predefinita, l'input penna è di colore nero se non è in modalità a contrasto elevato; In caso contrario, viene impostato sul valore corrente dell'impostazione del colore di sistema (COLOR \_ WINDOWTEXT). Inoltre, per impostazione [**predefinita FitToCurve**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkdrawingattributes-get_fittocurve) è **FALSE.**

All'interno [del controllo InkPicture](inkpicture-control-reference.md) usare l'oggetto [**Ink**](inkdisp-class.md) per caricare e salvare l'input penna.

> [!Note]  
> Quando si imposta [**EditingMode su**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_editingmode) **Delete o** **Select,** vengono attivati altri eventi, ad esempio [**l'evento Stroke.**](inkpicture-stroke.md) Questi eventi sono utili se si vogliono implementare modalità di eliminazione o selezione personalizzate.

 

Per informazioni di riferimento dettagliate sul [controllo InkPicture,](inkpicture-control-reference.md) vedere InkPicture.

Le sezioni seguenti illustrano in dettaglio l'uso [del controllo InkPicture:](inkpicture-control-reference.md)

-   [Uso delle immagini](working-with-pictures.md)
-   [Uso di InkPicture nelle versioni precedenti di Windows](using-inkpicture-on-earlier-versions-of-windows.md)

 

 
