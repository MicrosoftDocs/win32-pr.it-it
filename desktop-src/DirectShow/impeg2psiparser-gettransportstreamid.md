---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: 'Metodo IMpeg2PsiParser:: GetTransportStreamId'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetTransportStreamId
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9615c50d8d16aa6d78e3e1b83a3ec0e356c6cb50
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106304180"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a>Metodo IMpeg2PsiParser:: GetTransportStreamId

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.

Il `GetTransportStreamId` metodo recupera il \_ \_ campo ID del flusso di trasporto da Pat. Questo valore è definito dall'utente e può essere usato per distinguere un flusso di trasporto specifico da altri flussi nella stessa rete. Un flusso di trasporto contiene al massimo un PAT.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStreamId* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il \_ campo ID del flusso di trasporto \_ .

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT** . I valori possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.



| Codice restituito                                                                          | Descrizione         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Esito positivo.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Esempio di filtro del parser PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




