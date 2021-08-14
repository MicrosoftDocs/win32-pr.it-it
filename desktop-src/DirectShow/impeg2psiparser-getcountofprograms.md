---
description: "Metodo IMpeg2PsiParser::GetCountOfPrograms: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata."
ms.assetid: 282dd779-9aca-46e3-a791-cb9ea86f637d
title: Metodo IMpeg2PsiParser::GetCountOfPrograms
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
ms.openlocfilehash: c0c5609f82db98caea02e08f1e4fbd3877eeccbae25a5e83da3ac2804577b100
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "118398108"
---
# <a name="impeg2psiparsergetcountofprograms-method"></a>Metodo IMpeg2PsiParser::GetCountOfPrograms

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata.

Il `GetCountOfPrograms` metodo recupera il numero di programmi nel flusso di trasporto.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetCountOfPrograms(
  [out] int *pNumOfPrograms
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pNumOfPrograms* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di programmi.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un valore HRESULT. I valori possibili includono, ma non sono limitati, i valori illustrati nella tabella seguente.



| Codice restituito                                                                          | Descrizione         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Operazione completata.<br/> |



 

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[Esempio di filtro del parser PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




