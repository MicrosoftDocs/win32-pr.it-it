---
description: "Metodo IMpeg2PsiParser::GetTransportStreamId: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata."
ms.assetid: 0c35abc0-984f-42df-a2a2-30cd400d4599
title: Metodo IMpeg2PsiParser::GetTransportStreamId
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
ms.openlocfilehash: e78eabce23633029e4ef3dfe6c6777c586a5d74ed28ccfe466c89064851f8197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119791901"
---
# <a name="impeg2psiparsergettransportstreamid-method"></a>Metodo IMpeg2PsiParser::GetTransportStreamId

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata.

Il `GetTransportStreamId` metodo recupera il campo \_ \_ dell'ID del flusso di trasporto da PAT. Questo valore è definito dall'utente e può essere usato per distinguere un flusso di trasporto specifico da altri flussi nella stessa rete. Un flusso di trasporto contiene al massimo un PAT.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetTransportStreamId(
  [out] WORD *pStreamId
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pStreamId* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il campo \_ dell'ID del flusso di \_ trasporto.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non solo, i valori illustrati nella tabella seguente.



| Codice restituito                                                                          | Descrizione         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Operazione completata.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Esempio di filtro del parser PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




