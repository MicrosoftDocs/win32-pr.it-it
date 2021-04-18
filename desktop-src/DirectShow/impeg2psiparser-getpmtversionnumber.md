---
description: L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: 'Metodo IMpeg2PsiParser:: GetPmtVersionNumber'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMpeg2PsiParser.GetPmtVersionNumber
api_type:
- COM
api_location: ''
ms.openlocfilehash: 3af4b20067af52216181848f4cc63ac5a7784ba9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/06/2021
ms.locfileid: "106303816"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a>Metodo IMpeg2PsiParser:: GetPmtVersionNumber

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non si tratta di un'API DirectShow supportata.

Il `GetPmtVersionNumber` metodo recupera il \_ campo del numero di versione da un PMT specificato. Il numero di versione viene incrementato ogni volta che viene modificata la definizione del programma.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wProgramNumber* \[ in\]
</dt> <dd>

Specifica il \_ campo numero di programma del programma, come specificato in Pat.

</dd> <dt>

*pPmtVersion* \[ out\]
</dt> <dd>

Puntatore a una variabile che riceve il campo del numero di versione \_ .

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

 

 




