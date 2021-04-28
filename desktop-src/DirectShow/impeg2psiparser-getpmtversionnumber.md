---
description: "Metodo IMpeg2PsiParser::GetPmtVersionNumber: l'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata."
ms.assetid: 50113d6b-4e10-4dc9-aaef-f67c6918a2de
title: Metodo IMpeg2PsiParser::GetPmtVersionNumber
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
ms.openlocfilehash: 6f4fd8d0eba88ba1df54a1cc058bc0a2951b9a19
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084559"
---
# <a name="impeg2psiparsergetpmtversionnumber-method"></a>Metodo IMpeg2PsiParser::GetPmtVersionNumber

L'implementazione di questo metodo viene fornita come codice di esempio con DirectShow SDK. Non è un'API DirectShow supportata.

Il `GetPmtVersionNumber` metodo recupera il campo del numero di versione da un \_ pmt specificato. Il numero di versione viene incrementato ogni volta che cambia la definizione del programma.

## <a name="syntax"></a>Sintassi


```C++
HRESULT GetPmtVersionNumber(
  [in]  WORD wProgramNumber,
  [out] BYTE *pPmtVersion
);
```



## <a name="parameters"></a>Parametri

<dl> <dt>

*wProgramNumber* \[ Pollici\]
</dt> <dd>

Specifica il campo \_ del numero di programma del programma, come specificato nel campo PAT.

</dd> <dt>

*pPmtVersion* \[ Cambio\]
</dt> <dd>

Puntatore a una variabile che riceve il campo del \_ numero di versione.

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

 

 




