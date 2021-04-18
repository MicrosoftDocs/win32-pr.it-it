---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: 'Metodo IMpeg2PsiParser:: GetRecordProgramNumber'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetRecordProgramNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 2bedc5922ce90fa2fda612f30571f884e75841d6
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303815"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a>Metodo IMpeg2PsiParser:: GetRecordProgramNumber

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.

Il `GetRecordProgramNumber` metodo recupera il numero di programma per un programma specificato.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetRecordProgramNumber(
  [in]  DWORD dwIndex,
  [out] WORD  *pwVal
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*dwIndex* \[ in\]
</dt> <dd>

Specifica la voce del PAT che definisce il programma, indicizzato da zero.

</dd> <dt>

*pwVal* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il \_ campo del numero di programma da Pat.

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

 

 




