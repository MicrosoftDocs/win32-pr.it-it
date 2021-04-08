---
description: Richiede di ottenere le informazioni specificate dalla tabella degli oggetti per l'evento specificato.
MS-HAID: vspixengine.IObjectTableRequest\_RequestAsync\_DWORD\_DWORD\_DWORD\_arr\_IObjectTableCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IObjectTableRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: EE40F584-CDDE-465D-B4CB-A98B917DD0EE
api_name:
- IObjectTableRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2c9108708475b27a7a1882051c7f0177e14470f9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746727"
---
# <a name="span-idvspixengineiobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dwordspaniobjecttablerequestrequestasync-method"></a><span id="vspixengine.iobjecttablerequest_requestasync_dword_dword_dword_arr_iobjecttablecallback_ptr_dword_dword"></span>Metodo IObjectTableRequest:: RequestAsync

Richiede di ottenere le informazioni specificate dalla tabella degli oggetti per l'evento specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestAsync(
   DWORD                  eventID,
   DWORD                  numColumns,
   DWORD []               count1_columns,
   IObjectTableCallback * requestCallback,
   DWORD                  requestCookie,
   DWORD                  progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*eventID*   
Evento specificato.

*numColumns*   
Numero di colonne (campi) di informazioni da ottenere.

*\_colonne count1*   
Colonne specificate (campi).

*requestCallback*   
Indirizzo del callback utilizzato per notificare all'host i risultati.

*requestCookie*   
Un cookie che identifica in modo univoco la richiesta e può essere usato per segnalare l'annullamento.

*progressIntervalMsecs*   
Non usato.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IObjectTableRequest**](/windows/desktop/direct3dtools/iobjecttablerequest)

 

 
