---
title: Informazioni di riferimento su Gestione compressione audio
description: Informazioni di riferimento su Gestione compressione audio
ms.assetid: a4e234c7-4dd3-4269-90a5-5de2c8837c0f
keywords:
- Windows multimediali, informazioni di riferimento su ACM
- multimediali, informazioni di riferimento su ACM
- audio multimediale, informazioni di riferimento su ACM
- audio, informazioni di riferimento su ACM)
- gestione compressione audio(ACM), riferimento
- ACM (gestione compressione audio),riferimento
- Informazioni di riferimento su ACM
- informazioni di riferimento per ACM, informazioni su
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29729fa19e67fb4695d8e6eca986488735d9b4529d9479615665a9ba2b5f3360
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118375798"
---
# <a name="audio-compression-manager-reference"></a>Informazioni di riferimento su Gestione compressione audio

In questa sezione vengono descritte le funzioni, le strutture e i messaggi associati a ACM. Questi elementi sono raggruppati come indicato di seguito.

## <a name="drivers"></a>Driver

-   [**acmDriverAdd**](/windows/desktop/api/Msacm/nf-msacm-acmdriveradd)
-   [**acmDriverClose**](/windows/desktop/api/Msacm/nf-msacm-acmdriverclose)
-   [**ACMDRIVERDETAILS**](/windows/win32/api/msacm/ns-msacm-acmdriverdetails)
-   [**acmDriverEnum**](/windows/desktop/api/Msacm/nf-msacm-acmdriverenum)
-   [**acmDriverEnumCallback**](/windows/win32/api/msacm/nc-msacm-acmdriverenumcb)
-   [**acmDriverID**](/windows/desktop/api/Msacm/nf-msacm-acmdriverid)
-   [**acmDriverMessage**](/windows/desktop/api/Msacm/nf-msacm-acmdrivermessage)
-   [**acmDriverOpen**](/windows/desktop/api/Msacm/nf-msacm-acmdriveropen)
-   [**acmDriverPriority**](/windows/desktop/api/Msacm/nf-msacm-acmdriverpriority)
-   [**acmDriverProc**](/windows/desktop/api/Msacm/nc-msacm-acmdriverproc)
-   [**acmDriverRemove**](/windows/desktop/api/Msacm/nf-msacm-acmdriverremove)

## <a name="filters"></a>Filtri

-   [**ACMFILTERCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmfilterchoose)
-   [**acmFilterChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmfilterchoosehookproc)
-   [**ACMFILTERDETAILS**](/windows/win32/api/msacm/ns-msacm-acmfilterdetails)
-   [**acmFilterEnum**](/windows/desktop/api/Msacm/nf-msacm-acmfilterenum)
-   [**acmFilterEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfilterenumcb)
-   [**ACMFILTERTAGDETAILS**](/windows/win32/api/msacm/ns-msacm-acmfiltertagdetails)
-   [**acmFilterTagEnum**](/windows/desktop/api/Msacm/nf-msacm-acmfiltertagenum)
-   [**acmFilterTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmfiltertagenumcb)

## <a name="formats"></a>Formati

-   [**ACMFORMATCHOOSE**](/windows/win32/api/msacm/ns-msacm-acmformatchoose)
-   [**acmFormatChooseHookProc**](/windows/desktop/api/Msacm/nc-msacm-acmformatchoosehookproc)
-   [**ACMFORMATDETAILS**](/windows/win32/api/msacm/ns-msacm-acmformatdetails)
-   [**acmFormatEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformatenum)
-   [**acmFormatEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformatenumcb)
-   [**acmFormatSuggest**](/windows/desktop/api/Msacm/nf-msacm-acmformatsuggest)
-   [**ACMFORMATTAGDETAILS**](/windows/win32/api/msacm/ns-msacm-acmformattagdetails)
-   [**acmFormatTagEnum**](/windows/desktop/api/Msacm/nf-msacm-acmformattagenum)
-   [**acmFormatTagEnumCallback**](/windows/desktop/api/Msacm/nc-msacm-acmformattagenumcb)

## <a name="messages"></a>Messaggi

-   [**FILTRO \_ ACM \_ MMSCEGLIERE**](mm-acm-filterchoose.md)
-   [**FORMATO \_ ACM \_ MMSCEGLIERE**](mm-acm-formatchoose.md)

## <a name="streams"></a>Flussi

-   [**acmStreamClose**](/windows/desktop/api/Msacm/nf-msacm-acmstreamclose)
-   [**acmStreamConvert**](/windows/desktop/api/Msacm/nf-msacm-acmstreamconvert)
-   [**acmStreamConvertCallback**](/previous-versions//dd742925(v=vs.85))
-   [**ACMSTREAMHEADER**](/windows/win32/api/msacm/ns-msacm-acmstreamheader)
-   [**acmStreamMessage**](/windows/desktop/api/Msacm/nf-msacm-acmstreammessage)
-   [**acmStreamOpen**](/windows/desktop/api/Msacm/nf-msacm-acmstreamopen)
-   [**acmStreamPrepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamprepareheader)
-   [**acmStreamReset**](/windows/desktop/api/Msacm/nf-msacm-acmstreamreset)
-   [**acmStreamSize**](/windows/desktop/api/Msacm/nf-msacm-acmstreamsize)
-   [**acmStreamUnprepareHeader**](/windows/desktop/api/Msacm/nf-msacm-acmstreamunprepareheader)

## <a name="miscellaneous"></a>Varie

-   [**acmGetVersion**](/windows/desktop/api/Msacm/nf-msacm-acmgetversion)
-   [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics)

## <a name="related-topics"></a>Argomenti correlati

<dl> <dt>

[Gestione compressione audio](audio-compression-manager.md)
</dt> </dl>

 

 