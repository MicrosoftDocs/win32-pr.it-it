---
description: "Metodo IMpeg2PsiParser::GetRecordProgramNumber: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata."
ms.assetid: 3800a0b1-a581-40ed-81ab-3d5f77f442df
title: Metodo IMpeg2PsiParser::GetRecordProgramNumber
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
ms.openlocfilehash: e42e991fc7e288fc36dafcd167fe21ffb4983baeeb34bbb80e1bf67981e24779
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083701"
---
# <a name="impeg2psiparsergetrecordprogramnumber-method"></a>Metodo IMpeg2PsiParser::GetRecordProgramNumber

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata.

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

*dwIndex* \[ Pollici\]
</dt> <dd>

Specifica la voce in PAT che definisce il programma, indicizzata da zero.

</dd> <dt>

*pwVal* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il campo del \_ numero di programma da PAT.

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

 

 




