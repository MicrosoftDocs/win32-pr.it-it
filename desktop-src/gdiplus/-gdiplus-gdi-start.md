---
description: Windows GDI+ è un'API basata su classi per i programmatori C/C++.
ms.assetid: ed1396b2-2fc5-4a77-bea2-7bcc971214ae
title: GDI+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac0dac72d27ba52071797b51573141506d5b0ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129067"
---
# <a name="gdi"></a>GDI+

## <a name="purpose"></a>Scopo

Windows GDI+ è un'API basata su classi per i programmatori C/C++. Consente alle applicazioni di utilizzare grafica e testo formattato sia sullo schermo video che sulla stampante. Le applicazioni basate sull'API Microsoft Win32 non accedono direttamente all'hardware grafico. Diversamente, GDI+ interagisce con i driver di dispositivo per conto delle applicazioni. GDI+ è supportato anche da Win64 Microsoft.

## <a name="where-applicable"></a>Se applicabile

Le funzioni e le classi GDI+ non sono supportate per l'uso in un servizio Windows. Il tentativo di utilizzare queste funzioni e classi da un servizio Windows può produrre problemi imprevisti, ad esempio le prestazioni del servizio diminuite e gli errori o le eccezioni in fase di esecuzione.

> [!Note]  
> Quando si usa l'API GDI+, non è mai necessario consentire all'applicazione di scaricare tipi di carattere arbitrari da origini non attendibili. Il sistema operativo richiede privilegi elevati per assicurarsi che tutti i tipi di carattere installati siano attendibili.

## <a name="developer-audience"></a>Sviluppatori

L'interfaccia basata su classi C++ GDI+ è progettata per l'uso da parte dei programmatori C/C++. È necessaria una certa familiarità con l'interfaccia utente grafica di Windows e l'architettura basata su messaggi.

## <a name="run-time-requirements"></a>Requisiti di runtime

GDI+ può essere utilizzato in tutte le applicazioni basate su Windows. GDI+ è stato introdotto in Windows XP e Windows Server 2003. Per informazioni sui sistemi operativi necessari per usare una classe o un metodo specifico, vedere la sezione altre informazioni della documentazione relativa alla classe o al metodo.

## <a name="in-this-section"></a>Contenuto della sezione

| Argomento                                                    | Descrizione                                           |
|----------------------------------------------------------|-------------------------------------------------------|
| [Overview](-gdiplus-about-gdi--about.md)<br/>     | Informazioni generali su GDI+.<br/>            |
| [Usando](-gdiplus-using-gdi--use.md)<br/>          | Attività ed esempi con GDI+.<br/>             |
| [Riferimento](-gdiplus-class-gdi-reference.md)<br/> | Documentazione dell'API basata su classi di GDI+ C++.<br/> |

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[GDI Windows](../gdi/windows-gdi.md)
</dt> <dt>

[DirectX](/previous-versions/windows/apps/hh452744(v=win.10))
</dt> <dt>

[Acquisizione di immagini Windows](../wia/-wia-startpage.md)
</dt> <dt>

[OpenGL](../opengl/opengl.md)
</dt> <dt>

[Multimedia di Windows](../multimedia/windows-multimedia-start-page.md)
</dt> </dl>
