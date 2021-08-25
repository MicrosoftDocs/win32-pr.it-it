---
description: Richieste di esecuzione dell'analisi offline con l'origine, il manifesto, i parametri e del frame specificato.
MS-HAID: vspixengine.IOfflineAnalysisRequest\_RequestOfflineAnalysisAsync\_enumOFFLINEANALYSISSOURCE\_BSTR\_BSTR\_DWORD\_BSTR\_DWORD\_BSTR\_IOfflineAnalysisCallback\_ptr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IOfflineAnalysisRequest::RequestOfflineAnalysisAsync
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: C836D9C1-D3E0-4661-9B89-048B61028F53
api_name:
- IOfflineAnalysisRequest.RequestOfflineAnalysisAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2a8a36f65f2158d03650257cf13458d36330e7fd3184210d99c05200e1731231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119981141"
---
# <a name="span-idvspixengineiofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptrspaniofflineanalysisrequestrequestofflineanalysisasync-method"></a><span id="vspixengine.iofflineanalysisrequest_requestofflineanalysisasync_enumofflineanalysissource_bstr_bstr_dword_bstr_dword_bstr_iofflineanalysiscallback_ptr"></span>Metodo IOfflineAnalysisRequest::RequestOfflineAnalysisAsync

Richieste di esecuzione dell'analisi offline con l'origine, il manifesto, i parametri e del frame specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestOfflineAnalysisAsync(
   enum OFFLINEANALYSISSOURCE analysisSource,
   BSTR                       manifestXml,
   BSTR                       parametersXml,
   DWORD                      cookie,
   BSTR                       captureFullFileName,
   DWORD                      frameNumber,
   BSTR                       outputFullFileName,
   IOfflineAnalysisCallback * requestCallback
);
```

## <a name="parameters"></a>Parametri

*analysisSource*   
Specifica dove l'origine dell'analisi deriva da report memorizzati nella cache o dalla riproduzione.

*manifestXml*   
Stringa COM contenente il percorso del file manifesto XML.

*parametersXml*   
Stringa COM contenente il percorso del file di parametri XML.

*Cookie*   
Cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.

*captureFullFileName*   
Stringa COM contenente il percorso assoluto del file di acquisizione (con estensione vsglog).

*frameNumber*   
Frame specificato.

*outputFullFileName*   
Stringa COM contenente il percorso assoluto del file in cui viene scritto l'output.

*requestCallback*   
Indirizzo di un callback utilizzato per inviare una notifica all'host dei risultati.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IOfflineAnalysisRequest**](/windows/desktop/direct3dtools/iofflineanalysisrequest)

 

 
