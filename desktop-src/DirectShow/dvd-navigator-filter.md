---
description: Filtro DVD Navigator
ms.assetid: 3b2c01a2-d52c-4497-8fc9-d1113e8507e8
title: Filtro DVD Navigator
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96d248e490201536e92afeb38f520028e29ea9a5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/19/2021
ms.locfileid: "122477298"
---
# <a name="dvd-navigator-filter"></a>Filtro DVD Navigator

Il filtro DVD Navigator è il filtro di origine per un grafico DVD-Video filtro di riproduzione. Apre tutti i file necessari in un volume di DVD-Video, esplora i file DVD-Video lineari con estensione vob e analizza il flusso del programma MPEG-2 risultante, suddividendo il flusso in tre pin di output (video, audio, immagine secondaria).

Il filtro DVD Navigator implementa anche le interfacce [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) e [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) che consentono a un'applicazione di riproduzione DVD di controllare DVD-Video riproduzione.




| | | Interfacce di filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2"><strong>IDvdControl2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvdinfo2"><strong>IDvdInfo2</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter"><strong>IFileSourceFilter</strong></a>, <strong>ISpecifyPropertyPages</strong> | | Tipi di supporti pin di input | MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM | | Interfacce pin di input | Non applicabile. | | Tipi di supporti pin di output | Tipi di base:<br /><ul><li>Video: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li>Audio: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li>Immagine secondaria: <strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>Tipi estesi:<br /> Video:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_MPEG2_VIDEO</strong></li></ul>Audio:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_Audio</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DOLBY_AC3</strong></li></ul>Immagine secondaria:<br /><ul><li><strong>MEDIATYPE_DVD_ENCRYPTED_PACK</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_Video</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li><li><strong>MEDIATYPE_MPEG2_PES</strong>, <strong>MEDIASUBTYPE_DVD_SUBPICTURE</strong></li></ul>Per abilitare i tipi estesi, <a href="/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption"><strong>chiamare IDvdControl2::SetOption</strong></a> e impostare <br /> | | Interfacce pin di output | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Filtrare l'| CLSID CLSID_DVDNavigator | | Pagina delle proprietà CLSID | Nessuna pagina delle proprietà. | | File eseguibili | qdvd.dll | | <a href="merit.md">|</a> MERIT_DO_NOT_USE | | <a href="filter-categories.md">Filtro categoria |</a> CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> <dt>

[Applicazioni DVD](dvd-applications.md)
</dt> </dl>

 

 




