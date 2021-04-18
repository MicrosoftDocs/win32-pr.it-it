---
description: Richiede la restituzione di dati oggetto generici che descrivono un oggetto nel file con estensione vsglog per l'evento specificato e nel formato specificato.
MS-HAID: vspixengine.IGenericBufferDataRequest\_RequestAsync\_DumperType\_EventID\_DWORD\_IGenericBufferDataCallback\_ptr\_DWORD\_DWORD
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: 'Metodo IGenericBufferDataRequest:: RequestAsync'
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 542E20F9-B91D-4A05-AEE8-9DD2E80B76DB
api_name:
- IGenericBufferDataRequest.RequestAsync
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 6d8860b2de7c3dce5c6f8b61467bfe147530ed76
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304353"
---
# <a name="span-idvspixengineigenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dwordspanigenericbufferdatarequestrequestasync-method"></a><span id="vspixengine.igenericbufferdatarequest_requestasync_dumpertype_eventid_dword_igenericbufferdatacallback_ptr_dword_dword"></span>Metodo IGenericBufferDataRequest:: RequestAsync

Richiede la restituzione di dati oggetto generici che descrivono un oggetto nel file con estensione vsglog per l'evento specificato e nel formato specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT RequestAsync(
   DumperType                   dumperType,
   EventID                      eventID,
   DWORD                        RequestedDataUID,
   IGenericBufferDataCallback * requestCallback,
   DWORD                        requestCookie,
   DWORD                        progressIntervalMsecs
);
```

## <a name="parameters"></a>Parametri

*dumperType*   
Formato specificato della rappresentazione testuale dell'oggetto (HTML, XML e così via)

*eventID*   
Evento specificato a cui associare il contenuto del buffer, ad esempio una destinazione di rendering può cambiare nel tempo.

*RequestedDataUID*   
Indirizzo dell'oggetto specificato.

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

[**IGenericBufferDataRequest**](/windows/desktop/direct3dtools/igenericbufferdatarequest)

 

 
