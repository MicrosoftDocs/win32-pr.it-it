---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: 'Metodo IMpeg2PsiParser:: GetCountOfElementaryStreams'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfElementaryStreams
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6593b699592c913940b14c2c26aea42057acfa40
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303818"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>Metodo IMpeg2PsiParser:: GetCountOfElementaryStreams

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.

Il `GetCountOfElementaryStreams` metodo recupera il numero di flussi elementari in un programma specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCountOfElementaryStreams(
  [in]  WORD wProgramNumber,
  [out] WORD *pwVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wProgramNumber* \[ in\]
</dt> <dd>

Specifica il \_ campo del numero di programma per il programma, come specificato in Pat.

</dd> <dt>

*pwVal* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di flussi elementari nel programma.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore **HRESULT** . I valori possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.



| Codice restituito                                                                          | Descrizione         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Esito positivo.<br/> |



 

## <a name="remarks"></a>Commenti

Usare il metodo **GetRecordProgramNumber** per ottenere il numero di programma.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[Esempio di filtro del parser PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




