---
description: Funzione di callback utilizzata per notificare all'host le informazioni sugli eventi nell'elenco degli eventi.
MS-HAID: vspixengine.IFrameEventsCallback\_ResultCallback\_DWORD\_DWORD\_DWORD\_DWORD\_VARIANT\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IFrameEventsCallback:: ResultCallback'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5AB67A11-00C1-47AF-8C8C-8B2FDD095BCF
api_name:
- IFrameEventsCallback.ResultCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: e746c54f2a82adb5042cd479e4ca04299c1b7402
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104225413"
---
# <a name="span-idvspixengineiframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arrspaniframeeventscallbackresultcallback-method"></a><span id="vspixengine.iframeeventscallback_resultcallback_dword_dword_dword_dword_variant_arr"></span>Metodo IFrameEventsCallback:: ResultCallback

Funzione di callback utilizzata per notificare all'host le informazioni sugli eventi nell'elenco degli eventi.

## <a name="syntax"></a>Sintassi


```C++
HRESULT ResultCallback(
   DWORD      frameNumber,
   DWORD      numElements,
   DWORD      numRows,
   DWORD      numColumns,
   VARIANT [] count1_pRowData
);
```

## <a name="parameters"></a>Parametri

*NumeroFrame*   
Numero di frame associato agli eventi.

*numElements*   
Numero totale di campi in tutte le colonne di tutti gli eventi.

*numRows*   
Il numero di eventi nel risultato.

*numColumns*   
Numero di colonne (campi) in ogni riga.

*\_pRowData count1*   
Informazioni sugli eventi; un elemento per ogni campo di ogni evento.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IFrameEventsCallback**](/windows/desktop/direct3dtools/iframeeventscallback)

 

 
