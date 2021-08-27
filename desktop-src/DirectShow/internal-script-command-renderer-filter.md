---
description: Filtro renderer comandi script interno
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: Filtro renderer comandi script interno
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b70fbcd7dc6347ec93a19558ef2306dffd5fb64
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/26/2021
ms.locfileid: "122982214"
---
# <a name="internal-script-command-renderer-filter"></a>Filtro renderer comandi script interno

Riceve i comandi script e li invia all'applicazione.

Questo filtro accetta i comandi script in uno dei due formati seguenti:

-   Testo \_ MEDIATYPE: ogni esempio di supporto contiene una stringa di testo ANSI.
-   MEDIATYPE ScriptCommand: ogni esempio di supporto contiene due stringhe Unicode con terminazione \_ NULL, concatenate tra loro. La prima stringa descrive il tipo di comando e la seconda è il comando script.

    Quando il filtro riceve un esempio, invia una notifica [**\_ dell'evento EC OLE \_ EVENT.**](ec-ole-event.md) Il primo parametro dell'evento è **un BSTR** con il tipo di comando o se `Text` il formato è MEDIATYPE \_ Text. Il secondo parametro di evento è **un BSTR** con il comando script. L'applicazione può recuperare l'evento e rispondere al comando script.

Per un esempio di come usare questo filtro, vedere [Parser SAMI (CC).](sami--cc--parser-filter.md)




| Etichetta | Valore |
|--------|-------|
| Interfacce di filtro | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter,</strong></a> <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a> | 
| Tipi di supporti pin di input | <ul><li>MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</li><li>MEDIATYPE_Text, MEDIASUBTYPE_NULL</li></ul> | 
| Interfacce pin di input | <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin,</strong></a> <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | 
| Tipi di supporti pin di output | Non applicabile | 
| Interfacce pin di output | Non applicabile | 
| Filtro CLSID | {48025243-2D39-11CE-875D-00608CB78066} | 
| CLSID della pagina delle proprietà | Nessuna pagina delle proprietà | 
| File eseguibile | Quartz.dll | 
| <a href="merit.md">Merito</a> | MERIT_PREFERRED + 1 | 
| <a href="filter-categories.md">Categoria filtro</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[DirectShow Filtri](directshow-filters.md)
</dt> </dl>

 

 



