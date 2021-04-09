---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: 'Metodo IMpeg2PsiParser:: GetCountOfPrograms'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetCountOfPrograms
api_type:
- COM
api_location: ''
ms.openlocfilehash: e4f01b2a360465b9670b52547cff1ff4c312a705
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "103876729"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a>Metodo IMpeg2PsiParser:: GetCountOfPrograms

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.

Il `GetCountOfPrograms` metodo recupera il numero di programmi nel flusso di trasporto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNumOfPrograms* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di programmi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore HRESULT. I valori possibili includono, ma non sono limitati, i valori mostrati nella tabella seguente.



| Codice restituito                                                                          | Descrizione         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**\_OK**</dt> </dl> | Esito positivo.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Esempio di filtro del parser PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




