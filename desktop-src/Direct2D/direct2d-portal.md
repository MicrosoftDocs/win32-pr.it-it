---
title: Direct2D
description: .
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2eae62ba2d6ff44920d6b6d4890a8c48bc3c0f8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/20/2020
ms.locfileid: "104047029"
---
# <a name="direct2d"></a>Direct2D

## <a name="purpose"></a>Scopo

Direct2D è un'API per la grafica 2D in modalità immediata e con accelerazione hardware che offre prestazioni elevate e rendering di alta qualità per la geometria 2D, le bitmap e il testo. L'API Direct2D è progettata per interagire correttamente con GDI, GDI+ e Direct3D.

## <a name="developer-audience"></a>Sviluppatori

Direct2D è progettato principalmente per l'uso da parte delle classi di sviluppatori seguenti:

-   Sviluppatori di applicazioni native di grandi dimensioni e di livello aziendale.
-   Sviluppatori che creano Toolkit e librerie di controllo per l'uso da parte degli sviluppatori downstream.
-   Sviluppatori che richiedono il rendering lato server della grafica 2D.
-   Gli sviluppatori che utilizzano la grafica Direct3D e necessitano di rendering semplice e a prestazioni elevate 2D e di testo per menu, elementi dell'interfaccia utente (UI) e visualizzazioni Heads-up (HUDs).

## <a name="run-time-requirements"></a>Requisiti di runtime

-   Windows 7 o Windows Vista con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Vista e versioni successive.
-   Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) e aggiornamento della piattaforma per Windows Server 2008 e versioni successive.

> [!Note]
>
> L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 sono un set di librerie di runtime che consente agli sviluppatori di utilizzare applicazioni per Windows 7, Windows Vista, Windows Server 2008 R2 e Windows Server 2008. Questi aggiornamenti saranno disponibili per tutti i clienti di Windows Vista e Windows Server 2008 tramite Windows Update. Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 possono avere Windows Update rilevare se l'aggiornamento richiesto è installato; in caso contrario, Windows Update lo scaricherà e installerà in background. Per ulteriori informazioni su entrambi gli aggiornamenti, vedere [aggiornamento della piattaforma per Windows Vista](https://support.microsoft.com/kb/971644).

 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                          | Descrizione                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novità di Direct2D](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | Di seguito sono riportate alcune delle nuove aggiunte a Direct2D. <br/>                                                                                                                   |
| [Informazioni su Direct2D](direct2d-overview.md)<br/>                                             | Introduce Direct2D, un'API che fornisce agli sviluppatori Win32 la possibilità di eseguire attività di rendering grafiche 2D con prestazioni e qualità visive superiori. <br/> |
| [Guida introduttiva di Direct2D per Windows 8](direct2d-quickstart-with-device-context.md)<br/>    | Vengono riepilogati i passaggi necessari per creare con Direct2D e viene fornito codice di esempio.<br/>                                                                                     |
| [Introduzione con Direct2D](getting-started-with-direct2d-nav.md)<br/>              | Viene descritto come iniziare a creare applicazioni Direct2D e viene fornito codice di esempio.<br/>                                                                             |
| [Guida per programmatori](programming-guide.md)<br/>                                          | Questa sezione contiene argomenti sulla programmazione concettuale che descrivono come usare l'API Direct2D. <br/>                                                                    |
| [Riferimento Direct2D](reference.md)<br/>                                                      | Descrive in modo dettagliato l'API Direct2D.<br/>                                                                                                                              |
| [Strumenti e utilità](tools-and-utilities.md)<br/>                                      | Strumenti e utilità forniti per Direct2D.<br/>                                                                                                                         |
| [Esempi](d2d-samples.md)<br/>                                                          | Applicazioni di esempio che illustrano l'API Direct2D.<br/>                                                                                                             |
| [Glossario Direct2D](direct2d-glossary.md)<br/>                                          | Vengono descritti i termini comunemente utilizzati dalla documentazione di Direct2D. <br/>                                                                                                      |



 

## <a name="additional-resources"></a>Risorse aggiuntive

-   [**Grafica e giochi DirectX**](/windows/desktop/directx)
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)

 

