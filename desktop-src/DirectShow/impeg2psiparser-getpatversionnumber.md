---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 2f5ad9bf-3d70-491a-ab45-15cd922a02d4
title: 'Metodo IMpeg2PsiParser:: GetPatVersionNumber'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPatVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 6117060cf0c8d3c56d03e5838376485244fde8d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "104401123"
---
# <a name="impeg2psiparsergetpatversionnumber-method"></a>Metodo IMpeg2PsiParser:: GetPatVersionNumber

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.

Il `GetPatVersionNumber` metodo recupera il \_ campo del numero di versione da Pat. Un flusso di trasporto contiene al massimo un PAT. Il numero di versione viene incrementato ogni volta che vengono modificate le informazioni nella tabella.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPatVersionNumber(
  [out] BYTE *pPatVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*pPatVersion* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il campo del numero di versione \_ .

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

 

 




