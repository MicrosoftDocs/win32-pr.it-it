---
title: Direct2D
description: Direct2D
ms.assetid: 03b3b91c-9751-4f8d-af24-85067f06930b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d685c62819fe97e7ca52a566a0e2d442f5e4be14d6b7ae0a252b2778c0bae5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "117825422"
---
# <a name="direct2d"></a>Direct2D

## <a name="purpose"></a>Scopo

Direct2D è un'API per la grafica 2D in modalità immediata e con accelerazione hardware che offre prestazioni elevate e rendering di alta qualità per la geometria 2D, le bitmap e il testo. L'API Direct2D è progettata per interagire bene con GDI, GDI+ e Direct3D.

## <a name="developer-audience"></a>Sviluppatori

Direct2D è progettato principalmente per l'uso da parte delle classi di sviluppatori seguenti:

-   Sviluppatori di applicazioni native di grandi dimensioni su scala aziendale.
-   Sviluppatori che creano toolkit e librerie di controllo per l'utilizzo da parte degli sviluppatori downstream.
-   Sviluppatori che richiedono il rendering lato server della grafica 2D.
-   Sviluppatori che usano la grafica Direct3D e necessitano di rendering 2D e testo semplice e ad alte prestazioni per menu, elementi dell'interfaccia utente e huD (Heads-up Display).

## <a name="run-time-requirements"></a>Requisiti di runtime

-   Windows 7 o Windows Vista con Service Pack 2 (SP2) e Aggiornamento della piattaforma per Windows Vista e versioni successive.
-   Windows Server 2008 R2 o Windows Server 2008 con Service Pack 2 (SP2) e Aggiornamento della piattaforma per Windows Server 2008 e versioni successive.

> [!Note]
>
> L'aggiornamento della piattaforma per Windows Vista e l'aggiornamento della piattaforma per Windows Server 2008 sono un set di librerie di runtime che consente agli sviluppatori di scegliere come destinazione le applicazioni Windows 7, Windows Vista, Windows Server 2008 R2 e Windows Server 2008. Questi aggiornamenti saranno disponibili per tutti i clienti Windows Vista e Windows Server 2008 tramite Windows Update. Le applicazioni di terze parti che richiedono l'aggiornamento della piattaforma per Windows Vista o l'aggiornamento della piattaforma per Windows Server 2008 possono fare in modo che Windows Update rilevi se l'aggiornamento richiesto è installato; In caso contrario, l Windows Update lo scariderà e lo installerà in background. Per altre informazioni su entrambi gli aggiornamenti, vedere [Aggiornamento della piattaforma per Windows Vista](https://support.microsoft.com/kb/971644).

 

## <a name="in-this-section"></a>Contenuto della sezione



| Argomento                                                                                          | Descrizione                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Novità di Direct2D](what-s-new-in-direct2d-for-windows-8-consumer-preview.md)<br/> | Ecco alcune delle nuove aggiunte a Direct2D. <br/>                                                                                                                   |
| [Informazioni su Direct2D](direct2d-overview.md)<br/>                                             | Introduce Direct2D, un'API che offre agli sviluppatori Win32 la possibilità di eseguire attività di rendering della grafica 2D con prestazioni superiori e qualità visiva. <br/> |
| [Guida introduttiva a Direct2D per Windows 8](direct2d-quickstart-with-device-context.md)<br/>    | Riepiloga i passaggi necessari per disegnare con Direct2D e fornisce codice di esempio.<br/>                                                                                     |
| [Attività iniziali con Direct2D](getting-started-with-direct2d-nav.md)<br/>              | Viene descritto come iniziare a creare applicazioni Direct2D e viene fornito codice di esempio.<br/>                                                                             |
| [Guida per programmatori](programming-guide.md)<br/>                                          | Questa sezione contiene argomenti di programmazione concettuali che descrivono come usare l'API Direct2D. <br/>                                                                    |
| [Informazioni di riferimento su Direct2D](reference.md)<br/>                                                      | Descrive in dettaglio l'API Direct2D.<br/>                                                                                                                              |
| [Strumenti e utilità](tools-and-utilities.md)<br/>                                      | Strumenti e utilità disponibili per Direct2D.<br/>                                                                                                                         |
| [Esempi](d2d-samples.md)<br/>                                                          | Applicazioni di esempio che illustrano l'API Direct2D.<br/>                                                                                                             |
| [Glossario Direct2D](direct2d-glossary.md)<br/>                                          | Descrive i termini comunemente usati nella documentazione di Direct2D. <br/>                                                                                                      |



 

## <a name="additional-resources"></a>Risorse aggiuntive

-   [**Grafica e giochi DirectX**](/windows/desktop/directx)
-   [DirectWrite](/windows/desktop/DirectWrite/direct-write-portal)

 

