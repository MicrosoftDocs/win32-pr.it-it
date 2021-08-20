---
description: Questo argomento elenca le intestazioni e le librerie che definiscono tutte le API Media Foundation personalizzate.
ms.assetid: 69877842-fafe-408f-b55b-d2ff2277c756
title: Media Foundation intestazioni e librerie
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6db7650c98f6491fa6db4010273475b4bd103a2
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467468"
---
# <a name="media-foundation-headers-and-libraries"></a>Media Foundation intestazioni e librerie

Questo argomento elenca le intestazioni e le librerie che definiscono tutte le API Media Foundation personalizzate.

Per trovare l'intestazione e la libreria per un elemento API specifico, vedere le pagine di riferimento nella guida [di riferimento Media Foundation programmazione .](media-foundation-programming-reference.md)

## <a name="headers"></a>Intestazioni

-   codecapi.h
-   d3d11.h
-   d3d9.h
-   d3d9caps.h
-   d3d9types.h
-   dxva.h
-   dxva2api.h
-   dxvahd.h
-   evr.h
-   evr9.h
-   mfapi.h
-   mfcaptureengine.h
-   mferrors.h
-   mfidl.h
-   mfmediacapture.h
-   mfmediaengine.h
-   mfmp2dlna.h
-   mfobjects.h
-   mfplat.lib
-   mfplay.h
-   mfreadwrite.h
-   mftransform.h
-   opmapi.h
-   wmcodecdsp.h
-   wmcontainer.h

## <a name="libraries"></a>Librerie

-   dxva2.lib
-   evr.lib
-   mf.lib
-   mfplat.lib
-   mfplay.lib
-   mfreadwrite.lib
-   mfuuid.lib

## <a name="library-changes-in-windows-7"></a>Modifiche alla libreria in Windows 7

A partire Windows 7, alcune Media Foundation vengono esportate da file DLL diversi rispetto alle versioni precedenti.

Queste modifiche interessano i file con estensione lib seguenti:

-   evr.lib
-   mf.lib
-   mfplat.lib

Un'applicazione che usa una di queste funzioni deve collegarsi a un set diverso di file con estensione lib, a seconda della versione dell'SDK e della piattaforma di destinazione.




| Versione dell'SDK | Librerie | 
|-------------|-----------|
| Windows SDK per Windows Vista<br /> Windows SDK per Windows Server 2008<br /> | evr.lib<br /> mf.lib<br /> mfplat.lib<br /> | 
| Windows SDK per Windows 7 | Se la piattaforma di destinazione Windows Vista o Windows Server 2008, collegare le librerie seguenti:<br /><ul><li>evr_vista.lib</li><li>mf_vista.lib</li><li>mfplat_vista.lib</li></ul>Se la piattaforma di destinazione è Windows 7 o versione successiva, collegare le librerie seguenti:<br /><ul><li>evr.lib</li><li>mf.lib</li><li>mfplat.lib</li></ul> | 




 

## <a name="additional-info-on-helper-functions"></a>Informazioni aggiuntive sulle funzioni helper

Il Windows 8 MFPlat.dll è un componente del sistema operativo Microsoft Windows. Include diverse funzioni incluse nel modulo.

MFPlat implementa la funzionalità helper per l'allocazione di memoria di basso livello, la pianificazione delle operazioni fifo e le astrazioni di accesso ai file win32. Per essere più specifico, fornisce il supporto per gli elementi seguenti:

-   allocazione e inizializzazione di buffer di memoria (noti come "esempi") e helper per semplificarne la gestione della durata
-   funzioni efficienti di copia dei dati per i buffer di memoria
-   allocazione e inizializzazione di operazioni FIFO (note come "eventi")
-   implementazione di un oggetto clock semplice
-   implementazione di un wrapper di file win32
-   allocazione e inizializzazione di matrici di buffer di memoria per CPU e GPU

Se il [**metodo MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) ha esito positivo, MFPlat fornisce la funzionalità della coda di lavoro seguente:

-   supporto interno di elementi di I/O (usati dal wrapper di file win32 e dalle librerie socket)
-   fornendo una matrice di code di lavoro multithreading con supporto della priorità dei thread
-   supporto di elementi di lavoro, elementi timer ed elementi di attesa nelle code di lavoro

MFPlat offre funzionalità helper per la ricerca e la creazione di trasformazioni multimediali e origini multimediali registrate nel sistema e per la creazione e la modifica dei tipi di file multimediali, anche se MFPlat non può creare il contenuto multimediale effettivo né riprodurlo.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 




