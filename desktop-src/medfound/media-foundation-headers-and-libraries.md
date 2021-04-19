---
description: Questo argomento elenca le intestazioni e le librerie che definiscono tutte le API Media Foundation.
ms.assetid: 69877842-fafe-408f-b55b-d2ff2277c756
title: Intestazioni e librerie Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3d5412f3f306c6e0d7327c1da1eb4c48bb109a8
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 03/03/2021
ms.locfileid: "106320497"
---
# <a name="media-foundation-headers-and-libraries"></a>Intestazioni e librerie Media Foundation

Questo argomento elenca le intestazioni e le librerie che definiscono tutte le API Media Foundation.

Per trovare l'intestazione e la libreria per un elemento API specifico, vedere le pagine di riferimento nel [riferimento alla programmazione Media Foundation](media-foundation-programming-reference.md).

## <a name="headers"></a>Intestazioni

-   codecapis. h
-   d3d11. h
-   d3d9. h
-   d3d9caps. h
-   d3d9types. h
-   DXVA. h
-   dxva2api. h
-   dxvahd. h
-   EVR. h
-   evr9. h
-   mfapi. h
-   mfcaptureengine. h
-   mferrors. h
-   mfidl. h
-   mfmediacapture. h
-   mfmediaengine. h
-   mfmp2dlna. h
-   mfobjects. h
-   mfplat. lib
-   mfplay. h
-   mfreadwrite. h
-   mftransform. h
-   opmapi. h
-   wmcodecdsp. h
-   wmcontainer. h

## <a name="libraries"></a>Librerie

-   dxva2. lib
-   EVR. lib
-   MF. lib
-   mfplat. lib
-   mfplay. lib
-   mfreadwrite. lib
-   mfuuid. lib

## <a name="library-changes-in-windows-7"></a>Modifiche della libreria in Windows 7

A partire da Windows 7, alcune funzioni di Media Foundation vengono esportate da file DLL diversi rispetto alle versioni precedenti.

Queste modifiche interessano i file lib seguenti:

-   EVR. lib
-   MF. lib
-   mfplat. lib

Un'applicazione che usa una di queste funzioni deve essere collegata a un set diverso di file con estensione LIB, a seconda della versione dell'SDK e della piattaforma di destinazione.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Versione dell'SDK</th>
<th>Librerie</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Windows SDK per Windows Vista<br/> Windows SDK per Windows Server 2008<br/></td>
<td>EVR. lib<br/> MF. lib<br/> mfplat. lib<br/></td>
</tr>
<tr class="even">
<td>Windows SDK per Windows 7</td>
<td>Se la piattaforma di destinazione è Windows Vista o Windows Server 2008, collegare le librerie seguenti:<br/>
<ul>
<li>evr_vista. lib</li>
<li>mf_vista. lib</li>
<li>mfplat_vista. lib</li>
</ul>
Se la piattaforma di destinazione è Windows 7 o versione successiva, collegare le librerie seguenti:<br/>
<ul>
<li>EVR. lib</li>
<li>MF. lib</li>
<li>mfplat. lib</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="additional-info-on-helper-functions"></a>Informazioni aggiuntive sulle funzioni helper

Windows 8 MFPlat.dll è un componente del sistema operativo Microsoft Windows. Contiene diverse funzioni incluse nel modulo.

MFPlat implementa la funzionalità helper per l'allocazione di memoria di basso livello, la pianificazione delle operazioni FIFO e le astrazioni di accesso ai file Win32. Per essere più specifici, fornisce il supporto per gli elementi seguenti:

-   allocazione e inizializzazione di buffer di memoria (noti come "Samples") e helper per semplificare la gestione della durata
-   funzioni di copia dei dati efficienti per i buffer di memoria
-   allocazione e inizializzazione di operazioni FIFO (note come ' eventi ')
-   implementazione di un oggetto Clock semplice
-   implementazione di un wrapper di file Win32
-   allocazione e inizializzazione di matrici di buffer di memoria per CPU e GPU

Se il metodo [**MFStartup**](/windows/desktop/api/mfapi/nf-mfapi-mfstartup) ha esito positivo, MFPlat fornisce la seguente funzionalità della coda di lavoro:

-   supporto interno di elementi I/O (come usato dalle librerie di wrapper e socket di file Win32)
-   fornire una matrice di code di lavoro multithreading con supporto per priorità dei thread
-   supporto di elementi di lavoro, elementi timer e elementi Wait attraverso le code di lavoro

MFPlat offre funzionalità di supporto per l'individuazione e la creazione di trasformazioni di supporti e origini multimediali registrate nel sistema, nonché per la creazione e la manipolazione di tipi di supporto, sebbene MFPlat non sia in grado di creare i supporti effettivi né riprodurli nuovamente.

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Informazioni su Media Foundation](about-the-media-foundation-sdk.md)
</dt> </dl>

 

 




