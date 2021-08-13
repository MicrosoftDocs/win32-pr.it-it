---
description: Richieste per indicare che il log di grafica contiene nuovi dati al suo interno.
MS-HAID: vspixengine.IPixEngine2\_OnNewDataAvailable\_BOOL\_BOOL\_INT64\_INT64\_INT32\_BYTE\_arr
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: Metodo IPixEngine2::OnNewDataAvailable
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: B99FC54C-9395-4B14-93D5-B6408D655DC3
api_name:
- IPixEngine2.OnNewDataAvailable
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 1b39587dd96d19eaa82a25396cc2ee563f87e5095eb5492025d09d4091dce076
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118282840"
---
# <a name="span-idvspixengineipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arrspanipixengine2onnewdataavailable-method"></a><span id="vspixengine.ipixengine2_onnewdataavailable_bool_bool_int64_int64_int32_byte_arr"></span>Metodo IPixEngine2::OnNewDataAvailable

Richieste per indicare che il log di grafica contiene nuovi dati al suo interno.

## <a name="syntax"></a>Sintassi


```C++
HRESULT OnNewDataAvailable(
   BOOL    fSessionEnd,
   BOOL    fUnloadCurFrame,
   INT64   i64FilePositionStart,
   INT64   i64FilePositionEnd,
   INT32   iObjectTableDataSize,
   BYTE [] count4_pObjectTableData
);
```

## <a name="parameters"></a>Parametri

*fSessionEnd*   
true se la sessione è stata terminata; in caso contrario, false.

*fUnloadCurFrame*   
Non usato.

*i64FilePositionStart*   
Posizione del file, in byte, in corrispondenza della quale iniziano i nuovi dati.

*i64FilePositionEnd*   
Posizione del file, in byte, in corrispondenza della quale terminano i nuovi dati.

*iObjectTableDataSize*   
Numero di byte contenuti in count4 \_ pObjectTableData.

*count4 \_ pObjectTableData*   
Buffer contenente i dati per la tabella dell'oggetto.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un **codice di errore HRESULT.**

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine.h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IPixEngine2**](/windows/desktop/direct3dtools/ipixengine2)

 

 
