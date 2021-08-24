---
description: "Metodo IMpeg2PsiParser::GetCountOfElementaryStreams: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API di DirectShow supportata."
ms.assetid: 19ef96a8-3d5b-4da1-8cff-d6a271ad4915
title: Metodo IMpeg2PsiParser::GetCountOfElementaryStreams
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
ms.openlocfilehash: e241697884a4b665c160dc9991e4cb7f02c76f1ba32bc7a0656515faf1117a58
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767381"
---
# <a name="impeg2psiparsergetcountofelementarystreams-method"></a>Metodo IMpeg2PsiParser::GetCountOfElementaryStreams

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API di DirectShow supportata.

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

*wProgramNumber* \[ Pollici\]
</dt> <dd>

Specifica il campo del \_ numero di programma per il programma, come specificato nel campo PAT.

</dd> <dt>

*pwVal* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il numero di flussi elementari nel programma.

</dd> </dl>

## <a name="return-value"></a>Valore restituito

Il metodo restituisce un **valore HRESULT.** I valori possibili includono, ma non solo, i valori illustrati nella tabella seguente.



| Codice restituito                                                                          | Descrizione         |
|--------------------------------------------------------------------------------------|---------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Operazione completata.<br/> |



 

## <a name="remarks"></a>Commenti

Usare il **metodo GetRecordProgramNumber** per ottenere il numero di programma.

## <a name="see-also"></a>Vedi anche

<dl> <dt>

[**Interfaccia IMpeg2PsiParser**](impeg2psiparser.md)
</dt> <dt>

[**IMpeg2PsiParser::GetRecordProgramNumber**](impeg2psiparser-getrecordprogramnumber.md)
</dt> <dt>

[Esempio di filtro del parser PSI](psi-parser-filter-sample.md)
</dt> </dl>

 

 




