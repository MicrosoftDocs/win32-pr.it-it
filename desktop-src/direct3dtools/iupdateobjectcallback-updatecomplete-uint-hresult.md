---
description: Callback utilizzato per notificare all'host che un oggetto è stato aggiornato.
MS-HAID: vspixengine.IUpdateObjectCallback\_UpdateComplete\_UINT\_HRESULT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IUpdateObjectCallback:: UpdateComplete'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 7F54DDEC-E595-4615-B9B7-B1213A58B362
api_name:
- IUpdateObjectCallback.UpdateComplete
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: b601d8ac785f65c4400821741b83e76bd6987481
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104124695"
---
# <a name="span-idvspixengineiupdateobjectcallback_updatecomplete_uint_hresultspaniupdateobjectcallbackupdatecomplete-method"></a><span id="vspixengine.iupdateobjectcallback_updatecomplete_uint_hresult"></span>Metodo IUpdateObjectCallback:: UpdateComplete

Callback utilizzato per notificare all'host che un oggetto è stato aggiornato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT UpdateComplete(
   UINT    objectAddress,
   HRESULT result
);
```

## <a name="parameters"></a>Parametri

*objectAddress*   
ID dell'oggetto che è stato aggiornato.

*risultato*   
Indica se l'aggiornamento è stato completato o meno.

## <a name="return-value"></a>Valore restituito

Se questo metodo ha esito positivo, restituisce **S \_ OK**. In caso contrario, restituisce un codice di errore **HRESULT** .

## <a name="requirements"></a>Requisiti

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p>Intestazione</p></td><td>Vspixengine. h</td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span id="see_also"></span>Vedere anche

[**IUpdateObjectCallback**](/windows/desktop/direct3dtools/iupdateobjectcallback)

 

 
